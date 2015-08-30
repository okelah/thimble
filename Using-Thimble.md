# Using Thimble

## Introduction

The following animations demonstrate some of the less-obvious ways.  Because Thimble uses a forked version
of Brackets, much of what you can do is the same as for [using the desktop Brackets editor](https://github.com/adobe/brackets/wiki/How-to-Use-Brackets).  However, some features are unique to the browser.

## Inline Docs

You can get HTML and CSS documentation by using `CTRL+K` or `CMD+K` (OS X) while your cursor is on top of an element or property:

![Inline Docs Example](https://raw.githubusercontent.com/wiki/mozilla/thimble.webmaker.org/inline-docs.gif)

## Inline Editors

You can view and edit other parts of your project (i.e., linked content from other files) by using Inline Editors.  Place your cursor over the keyword you want to apply the editor to, and press `CTRL+E` or `CMD+E` (OS X).  Inline Editors work differently depending on what you select:
* **HTML** - you'll see all the CSS that applies to the given element, across any number of CSS files
* **CSS** - you can use a graphical color picker when you place your cursor on a CSS color value
* **JS** - you'll the definition of whatever method, variable, etc you have selected.  HINT: you can use `CTRL+J` or `CMD+J` (OS X) to jump to its definition instead

![Inline Docs Example](https://raw.githubusercontent.com/wiki/mozilla/thimble.webmaker.org/inline-editors.gif)

## File Tree Operations

You can create, delete, and rename files and folders by **right-clicking** the file tree:

![Inline Docs Example](https://raw.githubusercontent.com/wiki/mozilla/thimble.webmaker.org/filetree.gif)

## Upload Images (or other individual files)

You can upload one ore more files (you can't upload a folder, but see below for how to work with `.zip` files), and have them get added to your current project's filesystem.  Drag a file or files to the file tree or editor and drop.  NOTE: the preview area is *not* a drag-and-drop target for uploading files.  You can also use the `Upload Files` dialog box.  Uploaded file size is capped, currently at 3M.

![Inline Docs Example](https://raw.githubusercontent.com/wiki/mozilla/thimble.webmaker.org/upload-images.gif)

## Upload Archives

In addition to uploading a file or files, you can also upload a `.zip` archive.  Thimble will automatically
extract the archive into the current project, replacing any files that already exist with the same name.
If the archive's files are contained with a folder, the same directory structure will be created.  This is
a convenient way to seed a new project with existing files and folders.

![Inline Docs Example](https://raw.githubusercontent.com/wiki/mozilla/thimble.webmaker.org/upload-archives.gif)