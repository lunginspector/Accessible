# Accessible
**A jailed file viewer & extractor for iOS 16.0 - iOS 18.1.x, using shortcuts**

## How does it work?
* With Shortcuts, it uses the `file:///` extension to return system files.
* This allows us to read & extract files from certain directories.

## Readable Directories
* /System - Some access to view, most notably `PrivateFrameworks`.
* /Applications - Full access to view, with all app containers for non user-installed system Applications.
* /preboot - Very limited access, only files that shows are ones stored in `/private/preboot/`

## Features
* File Browser (no duh)
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

## Why don't you make an app?
1. I do not have a lot of programming knowledge nor do I have enough time to learn.
2. I don't feel like having to sideload an app when a Shortcut can achieve almost the exact same result.
3. For my use case, I don't need some of the advantages that an app would give me.
