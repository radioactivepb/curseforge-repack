# CurseForge AppImage Repackager

This repository automatically repackages the CurseForge AppImage from the official distribution. The official CurseForge Linux client is distributed as an AppImage inside a zip file, which is inconvenient for direct download and use.

## What this does

- **Monitors** the official CurseForge download link for updates
- **Downloads** the latest zip file containing the AppImage
- **Extracts** the AppImage from the zip
- **Creates** GitHub releases with just the AppImage file
- **Checks** for version changes to avoid duplicate releases

## Download

Go to the [Releases](../../releases) page to download the latest CurseForge AppImage.

## Why Does Repo This Exist?

### GearLever Integration
I did this mainly so I could use GearLever's update functionality with the CurseForge AppImage.
Since CurseForge only offers a zipped version with the AppImage inside, I can't use the automatic update functionality of GearLever.

With this repo, you can now set a GitHub update source for CurseForge in GearLever to this link:

```
https://github.com/radioactivepb/curseforge-repack/releases/download/*/CurseForge-*.AppImage
```

This allows GearLever to automatically detect and update to new versions of CurseForge as they're released.

## Original Source

The original CurseForge client can be found at:
- Official website: https://www.curseforge.com/
- Direct download: https://curseforge.overwolf.com/downloads/curseforge-latest-linux.zip

## License

This repository only repackages the official CurseForge client. All rights belong to Overwolf/CurseForge. This is provided for convenience only.
