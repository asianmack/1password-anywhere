1Password Anywhere for Chromebook
=============

<img src="http://asianmack.com/github/01-1Password.png" alt="1Password Anywhere for Chromebook" />

##What is it?##

Do you use a Chromebook? Were you saddened to find out that your 1Password Chrome Extension doesn't work on the Chromebook? I was.

1Password Anywhere for Chromebook uses the [1Password Anywhere](http://help.agilebits.com/1Password3/1passwordanywhere.html) feature. The gist is if your 1Password keychain lives in Dropbox, you can open an HTML file that will give you access to your 1Password data.

**This DOES NOT replace the 1Password extension you already have.** 1Password Anywhere for Chromebook lives in parallel (and separate to) the official 1Password extension.


##OK, how does it work?##

There are 4 files that make 1Password Anywhere for Chromebook work.

* manifest.json
* /img/icon-128.png
* /img/icon-48.png
* /img/icon-16.png

The important file is ```manifest.json```. This file contains the URL for your 1Password Anywhere page on Dropbox. You need to be authenticated into Dropbox in order to access this file.

##I mean...how do I make it work on my Chromebook?##

####1. Download files####
Save these files to your desktop. You will need to edit 2 lines in the ```manifest.json``` file.

####2. Get your 1Password Anywhere URL from Dropbox####
Browse to your Dropbox account in your web browser, and open the folder called **1Password.agilekeychain**. Click on the file called ```1Password.html```. Note the URL in the browser.

####3. Add your URL to manifest.json####
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

####4. Copy these files to your Chromebook####
Open the Files app, and browse to the Downloads folder. Inside Downloads, create a folder named EXTENSIONS.

<img src="http://asianmack.com/github/02-1Password.jpg" />

Open the EXTENSIONS folder, and create another folder inside of it named 1Password-Anywhere.

<img src="http://asianmack.com/github/03-1Password.jpg" />

Put the ```manifest.json``` and the ```img``` folder with the images in the 1Password-Anywhere folder.

<img src="http://asianmack.com/github/04-1Password.jpg" />

####5. Tell your Chromebook to use the 1Password Anywhere extension####
It's important to note that these files need to remain where they are – in the EXTENSIONS folder. They should not be moved or removed.

Open your Extensions page, either from the settings or by typing chrome://extensions/ in the address bar. On the Extensions page you need to turn on Developer mode.

Now click the "Load unpacked extension ..." button.

A file browser window will open. Browse to the **Downloads/EXTENSIONS/1Password-Anywhere/ folder and click the Open button.

1Password Anywhere will appear at the top of the list.

It's also in the App drawer.

You can pin 1Password Anywhere to your launcher for easy access.
