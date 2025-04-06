# Accessible
Dive deeper into your iPhone; Extract Protected System Files, Launch Hidden Applications, and More. iOS 17.0 - iOS 18.3.1. 
<p align="left">
  <strong><a href="https://github.com/lunginspector/Accessible/releases">Download</a></strong>
  •
  <strong><a href="https://discord.gg/nocturna-team-1144047674614616135">Discord Server</a></strong>
</p>

### Browse Files
Accessible uses a special method to read & export files that are usually hiden from the user.

### Open & Extract Internal Apps
Apps that are usually not Accessible on the Home Screen or App Library can now be opened & extracted. 
> [!IMPORTANT]
> Since these apps are on the /Application directory, no user-installed or uninstallable apps will be shown. Do not ask for this as it is not possible.

### Get Deeper Device Information
Accessible can translate MobileGestalt into a user-readable report telling you what tweaks you have enabled from SparseRestore tools like [Nugget](https://github.com/leminlimez/Nugget).

## How about Apple Watches?
No problem! Extract files from your Apple Watch by path, or directly save MobileGestalt. 

## Features (iOS and iPadOS)
* File Browser
    * Extract Files
    * Read Plists
    * Run Files in Apps
    * Search by Path
    * Favorite Directories
* Internal Apps Manager (Gets Applications from `/Applications`, which means that there are no user-installed apps in the folder.)
    * Open Application
    * Save Application Bundle
    * View Application Bundle
* MobileGestalt Tweaks
    * View MobileGestalt Tweaks commonly applied with [Nugget](https://github.com/leminlimez/Nugget)
    * Download Report
* Extra Tools
    * Save MobileGestalt - Saves the file `com.apple.MobileGestalt.plist`, which may be good for SparseRestore tools.
    * Extractor Playground - Extract files (by path) with Accessible's Entitlement Method or the Share Sheet Bug.

## Features (watchOS)
* Extract MobileGestalt
* Extract by path

## How does it work?
* It's very simple! Accessible uses the `file:///` extension and parses it as a URL with the requested directory attached the end. From this extension, we can return readable files.
    * Example: `file:///Applications` would return all the files found in the `/Applications` directory.
* An app may be able return these files (I haven't tried, and I have no programming knowledge), but I decided to use Shortcuts as it has been the most reliable method.
* On Apple Watches, the `file:///` extension is used as well. However, Apple Watches cannot return folders, so only specific plists can be read unfourtantely. 

## Readable Directories
* /System - Can read almost everything in this directory and contains a lot of important system files.
* /Applications - The most *accessible* directory here. Contains only non user-installed apps (I call them "Internal" apps).
* /var - Here, you can only read `/preboot`. No other files can be read. 
