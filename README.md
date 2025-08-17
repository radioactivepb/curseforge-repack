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

## How it works

The GitHub Action runs periodically and:

1. Downloads the zip file from `https://curseforge.overwolf.com/downloads/curseforge-latest-linux.zip`
2. Extracts the AppImage (format: `CurseForge-X.X.X-XXXXX.AppImage`)
3. Parses the version number from the filename
4. Checks if a release for this version already exists
5. If it's a new version, creates a new GitHub release with the AppImage

## Usage

### Direct Download
1. Download the AppImage from the releases page
2. Make it executable: `chmod +x CurseForge-*.AppImage`
3. Run it: `./CurseForge-*.AppImage`

### GearLever Integration
I did this mainly so I could use GearLever's update functionality with the CurseForge AppImage.
Hopefully others can get some use out of it too.

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
