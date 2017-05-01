SwiftDefaultApps
========

This Preference pane is chiefly intended to be a modern replacement for the amazing RCDefaultApp developed way back when by Carl Lindberg, which stopped working in 10.12 due to deprecation of ObjC Garbage collection.
Additionally, I guess it was a good way to teach myself Swift.

Feel free to contribute, comment or report issues at https://github.com/Lord-Kamina/SwiftDefaultApps.

## Installing & Uninstalling
	
	To install, double click on the .prefpane, and you will be prompted to install it.
	To uninstall, simply Ctrl+Click on the Prefpane icon and remove it, or move the .prefpane file to the Trash.

## Usage Notes

This Preference pane will let you view and change default application associations for basically any URL Scheme and/or filetype in macOS.
The user-interface should be pretty self-explanatory; but, there are some things that might require an explanation:
	
- Selecting any URL Scheme or File type (always represented by a UTI), will give you a list of all valid applications for each LaunchServices role. This data is generated by LaunchServices itself.
  - There's two additional options: 
    - One of them is **"Do Nothing"**, what this does is register the item to be handled by a dummy application that lives inside the prefpane bundle which basically does nothing. Its only function is being able to open any URL Scheme or UTI whatsoever, printing a line to the console (specifying whatever it was that launched it) and immediately quitting.
    - The second is **"Other..."**, which obviously will allow you to select an application not in the list; with a caveat. In recent versions of macOS, the LaunchServices have become quite a bit smarter under the hood than they used to be. In practice, what this means is that although you can choose *any* application to handle anything, only valid associations will be preserved, as the LaunchServices is permanently looking for invalid or stale associations and removing them.
  - One final note: In the URL Schemes tab, you have the option of adding a custom URL Scheme (Removing them on demand is neither possible nor necessary, due to the same thing explained above). This options is provided for completeness' sake; you should virtually never need to use it, since Launch Services should be able to properly detect any valid URL Handlers. As a further cautionary note: If you add a custom URL Scheme when it is not needed, you may not be able to remove it except by uninstalling and reinstalling SwiftDefaultApps. Why? Because new schemes are by default associated to *"Do Nothing", which means Launch Services will always find a valid handler as long as SwiftDefaultApps is installed.

## Acknowledgments & Attributions

- Using jakeheis' SwiftCLI 2.0 as a base for the CLI version located inside the bundle. (https://github.com/jakeheis/SwiftCLI)
- Using AMTourky's DRYView canned views system (https://github.com/AMTourky/CocoaBindingDryView-ReusableViews/)
- Using merrickluo's SynchronizedArray (https://github.com/merrickluo/SynchronizedArray)
- Icon made using the following resources:
	- Brush, Ruler and Pencil designed by Freepik. (http://www.freepik.com/free-vector/background-of-back-to-school_769298.htm)
	- Magnifying glass frame designed by Balintseby / Freepik (http://www.freepik.com/free-vector/realistic-magnifying-glass_789215.htm)
	- Magnifying glass crystal designed by Freepik (http://www.freepik.com/free-vector/crystal-frames-collection_724172.htm)
	- Gears designed by Freepik (http://www.freepik.com/free-vector/gray-background-of-gear_956712.htm)

## Current Version
    - Version: No releases yet.
    - Date: 2017-MM-DD

## Known Issues
- 

## TO DO
- Localizations

# Release Notes

## [1.0.0] - 2017-MM-DD
  + ### Added
    + Initial release!
  + ### Changed
  + ### Fixed
  
  