# Accessible
**A jailed filesystem viewer & extractor for iOS 15+.**

## How does it work?
* It's very simple! Accessible uses the `file:///` extension and parses it as a URL with the requested directory attached the end. From this extension, we can return readable files.
    * Example: `file:///Applications` would return all the files found in the `/Applications` directory.
* An app may be able return these files (I haven't tried, and I have no programming knowledge), but I decided to use Shortcuts as it has been the most reliable method.

## Readable Directories
* /System - Can read almost everything in this directory and contains a lot of important system files.
* /Applications - The most *accessible* directory here. Contains only non user-installed apps (I call them "Internal" apps).
* /var/ - Here, you can only read `/preboot` and nothing else that you'd usually find in this directory.

## Features (subject to change)
* File Browser
    * Extract Files
    * Read Plists
    * Run Files in Apps
    * Search by Path
* Apps Manager (Gets Applications from `/Applications`, which means that there are no user-installed apps in the folder.)
    * Open Application
    * Save Application Bundle
    * View Application Bundle
* Other Tools
    * Favorites - Add & Remove Paths to save for later.
    * Save MobileGestaltCache - Saves the file `com.apple.MobileGestalt.plist`, which may be good for SparseRestore tools.
    * Extractor Playground - Extract files with Accessible's Entitlement Method or the Share Sheet Bug.
