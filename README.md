# Example: convert bookmarklet to chrome extension package

It is my first training for making chrome extension.

The example uses "jash" javascript shell bookmarklet.

- http://billyreisinger.com/jash/

This technique could be applied for converting any bookmarklet 
to chrome "browserAction" button (right side of the url bar).

## build with crxmake

install crxmake:

    gem install crxmake

build:

    sh gencrx.sh --pack-extension=jash

## build with chrome.exe (on Windows7/Vista with cygwin)

build:

    export PATH=/cygdrive/c/Users/$USER/AppData/Local/Google/Chrome/Application/:"$PATH"
    chrome.exe --pack-extension=jash



## Resource

- http://code.google.com/chrome/extensions/packaging.html
- http://dev.chromium.org/developers/design-documents/extensions/packaging
