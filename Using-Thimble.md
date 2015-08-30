# Using Thimble

## Introduction

The following animations demonstrate some of the less-obvious ways.  Because Thimble uses a forked version
of Brackets, much of what you can do is the same as for [using the desktop Brackets editor](https://github.com/adobe/brackets/wiki/How-to-Use-Brackets).  However, some features are unique to the browser.

*NOTE: if you find the following animations too small to ready, you can open all of the images below in full-size by right-clicking and viewing them on their own.*

## Inline Docs

You can get HTML and CSS documentation by using `CTRL+K` or `CMD+K` (OS X) while your cursor is on top of an element or property:

![Inline Docs](https://raw.githubusercontent.com/wiki/mozilla/thimble.webmaker.org/inline-docs.gif)

## Inline Editors

You can view and edit other parts of your project (i.e., linked content from other files) by using Inline Editors.  Place your cursor over the keyword you want to apply the editor to, and press `CTRL+E` or `CMD+E` (OS X).  Inline Editors work differently depending on what you select:
* **HTML** - you'll see all the CSS that applies to the given element, across any number of CSS files
* **CSS** - you can use a graphical color picker when you place your cursor on a CSS color value
* **JS** - you'll the definition of whatever method, variable, etc you have selected.  HINT: you can use `CTRL+J` or `CMD+J` (OS X) to jump to its definition instead

![Inline Editors](https://raw.githubusercontent.com/wiki/mozilla/thimble.webmaker.org/inline-editors.gif)

## File Tree Operations

You can create, delete, and rename files and folders by **right-clicking** the file tree:

![File Tree](https://raw.githubusercontent.com/wiki/mozilla/thimble.webmaker.org/filetree.gif)

## Upload Images (or other individual files)

You can upload one ore more files (you can't upload a folder, but see below for how to work with `.zip` files), and have them get added to your current project's filesystem.  Drag a file or files to the file tree or editor and drop.  NOTE: the preview area is *not* a drag-and-drop target for uploading files.  You can also use the `Upload Files` dialog box.  Uploaded file size is capped, currently at 3M.

*TIP: if you need to use a secure (i.e., `https://`) version of a resource (script, image, stylesheet, font, ...) and can't find one, you can drag it into your project and host it from securely as part of your published project.

![Upload Images](https://raw.githubusercontent.com/wiki/mozilla/thimble.webmaker.org/upload-images.gif)

## Upload Archives

In addition to uploading a file or files, you can also upload a `.zip` archive.  Thimble will automatically
extract the archive into the current project, replacing any files that already exist with the same name.
If the archive's files are contained with a folder, the same directory structure will be created.  This is
a convenient way to seed a new project with existing files and folders.

![Upload .zip Archives](https://raw.githubusercontent.com/wiki/mozilla/thimble.webmaker.org/upload-archives.gif)

## Export a Project

Importing `*.zip` archives is nice because it allows you to bring pre-made content into your current project.  The same is true in reverse: you can export your current project as a `project.zip` file, and use it elsewhere.  To do so, log in and choose the `Export (.zip)` option.

![Export project.zip](https://raw.githubusercontent.com/wiki/mozilla/thimble.webmaker.org/export.gif) 