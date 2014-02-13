1Password Anywhere for Chromebook
=============

##What is it?##

Do you use a Chromebook? Were you saddened to find out that your 1Password Chrome Extension doesn't work on the Chromebook? I was.

1Password Anywhere for Chromebook uses the [1Password Anywhere](http://help.agilebits.com/1Password3/1passwordanywhere.html) feature. The gist is if your 1Password keychain lives in Dropbox, you can open an HTML file that will give you access to your 1Password data.

**It DOES NOT replace the 1Password extension you already have.** It lives in parallel (and separate to) that extension.


##OK, how does it work?##

There are 4 files that make 1Password Anywhere for Chromebook work.

* manifest.json
* /img/icon-128.png
* /img/icon-48.png
* /img/icon-16.png

The important file is ```manifest.json```. This file contains the URL for your 1Password Anywhere page on Dropbox. You need to be authenticated into Dropbox in order to access this file.

##I mean...how do I make it work on my Chromebook?##

####Step 1####

Download these repo files to your desktop.

####Step 2####

Browse to your Dropbox account in your web browser, and open the folder called **1Password.agilekeychain**. Click on the file called ```1Password.html```. Note the URL in the browser.

####Step 3####

Open the ```manifest.json``` file in your text editor. Look for the the following block:

```
"app": {
  "urls": [
    "YOUR-DROPBOX-URL-HERE"
  ],
  "launch": {
    "web_url": "YOUR-DROPBOX-URL-HERE"
  }
},
```

Replace YOUR-DROPBOX-URL-HERE with the URL from your ```1Password.html``` file that you got from Step 2. The quotation marks are important. Don't remove them. Save the file.
