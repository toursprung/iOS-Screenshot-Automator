iOS-Screenshot-Automator
========================

Batch-creates screenshots for all iOS devices in every language you define, ready for immediate upload in iTunes Connect. Uses and integrates with UIAutomation from Apple. Also great for unit testing.

Follow the developer on Twitter: [KrauseFx](http://twitter.com/krausefx) (Felix Krause)

The script is based on UIAutomation to navigate the app and take the screenshots.

Define which languages and simulator types you want to use in the "run"-file. 

#Run the script:#
```shell
./run ../TestScript.js AppName
```

To take screenshots with UIAutomation use captureLocalizedScreenshot. It will automatically name the file properly and put it in the Results folder. (Don't forget to import Helper.js in your javascript UIAutomation script)


If you want to set the carrier name manually, take a look at the "changeCarrierName" file

You can use tuneup_js to start your scripts and define tests. It's a really great library that helps you develop unit tests faster. You can also use these scripts to do unit testing.

To fetch the tuneup_js submodule, use the following git command.
      git submodule update --init


Example of TestScript.js
```javascript
#import "iOS-Screenshot-Automator/Helper.js"


test("Login Test", loginTest);
test("Route Test", routeDetailsTest);
...

function loginTest(target, app)
{
	var window = app.mainWindow();
	var navBar = window.navigationBar();
	
	...
	
	captureLocalizedScreenshot("Login");
	
	....
}
```

If you want to add the orientation of the iDevice in your screenshot names as well, configure it in the Helper.js file.

#Open Todos:#
* Put all resulting screenshots in one folder (or more meaningful folders)
* Raise AppleScript exception when UIAutomation script fails
* If possible: Automate uploading screenshots to iTunesConnect directly

![iOS Screenshot Automator](http://www.toursprung.com/wp-content/uploads/2013/01/ScreenshotToolImage.png)