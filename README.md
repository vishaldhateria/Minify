Minify Package for Sublime Text
===============================

Overview
--------
The `Minify Package` for Sublime Text can create a minified version of the currently open JavaScript or CSS file.

The plugin generates new files with the extensions `.min.js` or `.min.css`.

This Package has been tested with both Sublime Text 2 and Sublime Text 3 and should work fine on all platforms.

It uses the excellent [UglifyJS 2](https://github.com/mishoo/UglifyJS2) program to minify JavaScript files.
While `YUI Compressor` is utilized to minify CSS files. (`YUI Compressor` is used for CSS file minification only.)

It can also create a beautified version of the currently open JavaScript file. This can be useful in case you're
looking at a file which was previously minified and the original / uncompressed version of the file is unavailable.

Requirements
------------
You need to have Sublime Text 2 or Sublime Text 3 installed, obviously.

Since this Package uses UglifyJS 2 and UglifyJS runs in Node, you must have [Nodejs](http://nodejs.org/) installed on your system.
Once you have Nodejs installed, you should install UglifyJS 2. It is recommended to install it globally with the following command:

`npm install uglify-js -g`

After this the `uglifyjs` command should be available in your system PATH.

For CSS file minification, this package uses `YUI Compressor` and it is running in Java so you must have Java installed on your system
and it is recommended to have the `java` command available in your system PATH.

If you do not have these commands available in your system PATH then alternatively, you can specify custom locations for both
the `uglifyjs` and `java` commands in the User Settings of this Package.

Installation
------------
You may install the `Minify` Sublime Text Package via the excellent [Package Control](https://sublime.wbond.net/) package manager
and this is the recommended way to install it.

Alternatively, you may install the `Minify Package` by using git:

*MacOSX*

    git clone git://github.com/tssajo/Minify.git ~/Library/Application\ Support/Sublime\ Text\ 2/Packages/Minify

Note: Replace "Sublime\ Text\ 2" with "Sublime\ Text\ 3" in the above command if you are using Sublime Text 3

*Windows*

    git clone git://github.com/tssajo/Minify.git %APPDATA%\Sublime Text 2\Packages\Minify

Note: Replace "Sublime Text 2" with "Sublime Text 3" in the above command if you are using Sublime Text 3

How to use
----------
Open a `.js` or `.css` file in your Sublime Text editor, then you can:

A.  Use the Context Menu inside the Sublime Text editor window; or

B.  Access the `Minify file` or `Beautify file` commands under the Tools / Minify menu in Sublime Text.

C.  The following keyboard shortcuts are also available:

`ctrl + alt + m` - attempts to minify the current buffer and save the minified version into the same directory with the
    appropriate .min.js or .min.css file extension. It also opens the minified file on success in a new editor window.

`ctrl + alt + b` - attempts to beautify the current buffer and save the beautified version into the same directory with the
    appropriate .beautified.js file extension. It also opens the beautified file on success in a new editor window.

TODO
----
Beautifying of CSS files are not supported at this time. (Pull requests are welcome!)

License
-------
See [LICENSE.md](https://github.com/tssajo/Minify/blob/master/LICENSE.md) file for licensing information.
