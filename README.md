iOS-Screenshot-Automator
========================

Batch-creates screenshots for all iOS devices in every language you define, ready for immediate upload in iTunes Connect. Uses and integrates with UIAutomation from Apple. Also great for unit testing.

The script is based on UIAutomation to navigate the app and take the screenshots.

Define which languages and simulator types you want to use in the "run"-file. 

#To run the UIAutomation script to take screenshots use the following command:#
```shell
./run TestScript.js 564E26A0-....-....-....-............/AppName.app/
```
The TestScript has to be located outside of the iOS-Screenshot-Automator. To take screenshots with UIAutomation use captureLocalizedScreenshot. It will automatically name the file properly and put it in the Results folder.
Don't forget to import Helper.js in your javascript UIAutomation file. 

If you want to set the carrier name manually, take a look at the "changeCarrierName" file