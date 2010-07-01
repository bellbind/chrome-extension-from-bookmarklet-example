# Example: convert bookmarklet to chrome extension package

It is my first training for making chrome extension.

The example uses "jash" javascript shell bookmarklet.

- http://billyreisinger.com/jash/

This technique could be applied for converting any bookmarklet 
to chrome "browserAction" button (right side of the url bar).

## Artcitecture

Files:

- /manifest.json : descrition for browserAction extension
- /loader.html : generic background-page HTML
- /bookmarklet.js : javascript code from bookmarklet code
- /images/icon.png : required icon image
- /images/gen.sh : generating icon with "convert" (ImageMagick) command

Steps:

1. modify manifest.json: "name" and "description" entry
2. modify icon.png (or modify label and color in gen.sh, then run it)
3. modify bookmarklet.js : convert bookmarklet js code into pure js code
4. build package crx and release it


## build with crxmake

install crxmake:

    gem install crxmake

build:

    sh gencrx.sh --pack-extension=jash

## build with chrome.exe (on Windows7/Vista with cygwin)

build:

    export PATH=/cygdrive/c/Users/$USER/AppData/Local/Google/Chrome/Application/:"$PATH"
    chrome.exe --pack-extension=jash


## Resources

for packaging:

- http://code.google.com/chrome/extensions/packaging.html
- http://dev.chromium.org/developers/design-documents/extensions/packaging

for extension specifications:

- http://code.google.com/chrome/extensions/manifest.html
- http://code.google.com/chrome/extensions/browserAction.html
- http://code.google.com/chrome/extensions/background_pages.html
- http://code.google.com/chrome/extensions/tabs.html

