## How to install Sessions on Mac OS Mojave+ 

Even though Safari extensions have been deprecated, the last version of Sessions still work on Mojave and Higher.

It's installation is a little bit trickier than before, but you'll be just fine 😄

> **PREREQUISITE** **:** Enable Develop Menu in Safari
>
> *Go to* `Safari → Preferences → Advanced` *and select*  `Show Develop menu in menu bar.` 

**Steps**

1. Download Session at this address <https://sessions-extension.github.io/Sessions/>

2. Rename `Sessions.safariextz` into `Sessions.xar` 

3. Inside a terminal (`cmd` + `space` keys, then search for `terminal`)

   1. Enter the command : `cd Downloads`
   2. Extract the file using :
      `xar -xf path` where `path` is the result from the drag-on-drop of the `Sessions.xar` file from the download folder to the terminal window.

   >  The result should be something like : `xar -xf /Users/home/Downloads/Sessions.xar` 

4. This should  create a folder named `Sessions.safariextension` in your Downloads directory

5. Open `Develop` menu and select `Show Extension Builder`

   1. Click on the `+` button at the bottom left corner of the page
   2. Select `Add Extension`
   3. Select the folder `Sessions.safariextension`in your Downloads folder

6. Sessions should now appear in the `Extension Builder`window, click on `run`

Yeeeaah, it's now running. However, we need to make the database persistent, because otherwise, when we'll close Safari, it will clear our database 😭

**In order to do so**

1. Return on your terminal
2. Enter this command : `cd ~/Library/Safari`
3. Then `open .`
4. In the window that will appear, find the `Databases` folder and right-click on the only folder inside. It should look like `safari-extension_yoo.david.sessions-0000000000_0` or any weird combinations after the `sessions-`
5. Lock the folder
   1. On the menu that appeared because of the right-click, select the `Get infos` option
   2. Check the box labelled `Lock`



You finally have a working Sessions extension. Every time you will restart Safari, you will have to `run` the extension again, directly from the `Extension Builder`

**Careful though** - You cannot stop the extension and run it again right after, from the `Extension builder` menu, if you already have `Locked` the database folder. This will corrupt entireley the db ! (Doesn't corrupt on Safari kill or shutdown however)
