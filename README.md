1Password Anywhere for Chromebook
=============

##What is it?##

Do you use a Chromebook? Were you saddened to find out that your 1Password Chrome Extension doesn't work on the Chromebook? I was.

1Password Anywhere for Chromebook uses the [1Password Anywhere](http://help.agilebits.com/1Password3/1passwordanywhere.html) feature. The gist is if your 1Password keychain lives in Dropbox, you can open an HTML file that will give you access to your 1Password data.


##How does it work?##

There are 4 files that make 1Password Anywhere for Chromebook work.

* manifest.json
* /img/icon-128.png
* /img/icon-48.png
* /img/icon-16.png

The important file is ```manifest.json```. This file contains the URL for your 1Password Anywhere page on Dropbox. You need to be authenticated into Dropbox in order to access this file.
