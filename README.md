# Accessible
A jailed filesystem viewer & extractor for iOS 15.0 - iOS 18.3.2. Made by lunginspector for [jailbreak.party.](https://github.com/jailbreakdotparty)

[Release Tab](https://github.com/lunginspector/Accessible/releases) • [Support Server](https://discord.gg/XPj66zZ4gT)

**Disclaimer:** This shortcut CANNOT read or extract user data, which is usually stored in /var. 

## Browse Partitions
With the power of a special method, files that Apple would usually not allow you to read, such as stuff in /Applications, can be read. Browse the filesystem, read & export files, and get details on them. Use search to get to directories quicker than ever. 

## Open & Extract System Applications
Thanks to the ability to read /Applications, you can open & extract internal system applications, which are usually never available on SpringBoard or anywhere else in the operating system. 
>[!IMPORTANT]
> Since user-installed applications are NOT stored on /Applications, it is  **impossible** to fetch applications that you have installed yourself. 

## Device Reports
Accessible can parse MobileGestalt into a report, giving you details about your device not usually available in settings. These include details on whether tweaks enabled by SparseRestore tools, such as Nugget, have been enabled/disabled.

## The Method
Accessible uses the syntax `file:///[Directory Path]`, interpreted as a URL, in order to get the contents of the filesystem. Apple has unfortunately *partially* patched this in iOS 18.4, by restricting the ability to interpret anything from the URL as a folder (throws the Restricted Folder error).

## Readable Partitions
* /System - Usual system files, which are already readable with any application.
* /Applications - Application containers for system applications, which for some weird reason are only readable with this shortcut.
* /var - MAJOR exception: You can only read stuff from /var/preboot, which means no user data can be read with this shortcut. 
