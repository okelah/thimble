Thimble is a collection of various services, that all need to be run simulteanously. This document serves as an abbreviated guide to getting it all set up.

**You'll need**
* Thimble
* Brackets
* Webmaker ID server
* Webmaker Login Server
* Webmaker Publishing Server
* Postgres Database

## Installing the Parts

**Thimble**
* Fork and clone https://github.com/mozilla/thimble.webmaker.org
* Make sure you're on the ``bramble`` branch
* Run ``npm install`` to install dependencies
* Run ``cp env.dist .env`` to create an environment file
* Run ``node app`` to start the server

**Brackets**
* Fork and clone https://github.com/humphd/brackets
* Make sure you're on the ``bramble`` branch
* git submodule update --init
* Run ``grunt build-browser``
* Run ``python -m SimpleHTTPServer 8000`` to start the server on localhost:8000

**id.webmaker.org**
* Clone https://github.com/mozilla/id.webmaker.org
* Run ``cp sample.env .env`` to create an environment file
* Run ``npm install`` to install dependencies
* Run ``npm run`` to start the server

**login.webmaker.org**
* Clone https://github.com/mozilla/login.webmaker.org
* Run ``npm install`` to install dependencies
* Run ``cp env.sample .env`` to create an environment file
* Run ``npm start`` the server

**publish.webmaker.org**
* Clone https://github.com/mozilla/publish.webmaker.org
* Run ``npm install`` to install dependencies
* Run ``npm run env``
* Run ``npm install knex -g`` to install knex
* Run ``npm run knex`` to run knex
* Run ``npm start`` to run the server

**PostgreSQL**
* Install Postgres with via Homebrew
  * Get Homebrew - http://brew.sh/
  * Run `` brew install postgresql`` to install PostgreSQL once Homebrew is installed
* Run ``initdb -D /usr/local/var/postgres`` to initialize PostreSQL
* Run ``postgres -D /usr/local/var/postgres`` to start the PostgreSQL server
* Run ``createdb publish`` to create the Publish database

## Getting Ready to Publish
To publish locally, id.webmaker.org needs to learn about publish.webmaker.org

* Run ``createdb webmaker_oauth_test`` to create a test database
* In the **id.webmaker.org** folder
  * Run ``node scripts/create-tables.js``
  * Edit ``scripts/test-data.sql`` and replace it's contents with http://pastebin.com/DUXMjjwF
  * Run ``node scripts/test-data.js``

Instead of publishing to Amazon AWS, we'll be publishing to a local folder. Perform the following steps to set this up.
* Run ``npm install -g http-server && mkdir /tmp/mox && cd /tmp/mox && http-server -p 8001``
* Run ``cd /tmp/mox && http-server -p 8001`` to start the server

* In your **publish.webmaker.org** folder
  * Open the ``publish.env`` file
  * Make sure that ``PUBLIC_PROJECT_ENDPOINT="localhost:8001/test"``` is set as shown here
  * Restart publish server


 



