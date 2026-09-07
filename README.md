# DockSpark

DockSpark lets you switch browser profiles directly from the macOS Dock. Hover
over a supported browser icon, then choose the profile you want without opening
the browser's profile menu.

[Download the latest release](https://github.com/DockSpark/DockSpark/releases/latest)
· [Website](https://dockspark.app)
· [Changelog](CHANGELOG.md)
· [Report an issue](https://github.com/DockSpark/DockSpark/issues)

## Features

- Switch profiles from a popover attached to the browser's Dock icon
- Manage browser profiles from a native macOS app
- Use custom names and colors to identify profiles quickly
- Choose which named profiles appear in the Dock hover menu
- Use DockSpark Free, or unlock unlimited browsers and profiles with Pro
- Show or hide the menu bar and Dock icons
- Check for updates in the app
- Open documentation or send structured feedback from the Help menu
- Use the app in English or Simplified Chinese

## Requirements

- macOS 14.0 or later
- Apple silicon or Intel Mac
- A supported browser kept in the Dock

### Supported browsers

| Browser | Dock profile switching |
| --- | --- |
| Safari | Supported |
| Firefox | Supported |
| Google Chrome | Supported |
| Chromium | Supported |
| Microsoft Edge | Supported |
| Brave Browser | Supported |
| Vivaldi | Supported |
| Opera | Supported |
| Opera GX | Supported |
| Arc | Supported |

New installations show Safari plus installed copies of Google Chrome and Firefox
in the sidebar. Other supported browsers remain available via Dock hover, or can
be added from the app list.

## Install

### Homebrew

```sh
brew trust --cask dockspark/tap/dockspark && \
  brew install --cask dockspark/tap/dockspark
```

### Manual download

1. Open the [latest release](https://github.com/DockSpark/DockSpark/releases/latest).
2. Download `DockSpark-0.3.2.dmg`. Do not download GitHub's automatically
   generated source code archives.
3. Open the disk image and drag `DockSpark.app` to the Applications folder.
4. Launch DockSpark and grant the requested macOS permissions.

The `DockSpark-0.3.2.zip` asset is also available for manual installation.

DockSpark is signed with a Developer ID certificate and notarized by Apple.

## Permissions

DockSpark requests only the system permissions needed for profile switching:

- **Accessibility** detects pointer interaction with supported browser icons in
  the Dock.
- **Automation** lets DockSpark ask the selected browser to switch profiles.
- **Full Disk Access** is optional. DockSpark uses it only to discover Chromium
  and Firefox profile metadata.

You can review or revoke these permissions at any time in **System Settings >
Privacy & Security**.

## Usage

1. Add a supported browser to the Dock.
2. Configure the browser and its profiles in DockSpark.
3. Hover over the browser's Dock icon.
4. Select a profile from the popover.

## Screenshot

![DockSpark profile management window](Assets/img_dockspark.jpg)

> The screenshot previews the DockSpark interface. Version 0.3.2 supports Dock
> profile switching for Safari, Firefox, Chrome, and other Chromium-based
> browsers listed above.

## Updates

DockSpark uses Sparkle for in-app updates. You can also download releases
manually from the [Releases](https://github.com/DockSpark/DockSpark/releases)
page.

## Release integrity

The SHA-256 checksums are:

```text
DockSpark-0.3.2.dmg  d923c20ab61d0858a7c1d232e0583830bf4fe55315960507d0d8ace6e67efb91
DockSpark-0.3.2.zip  02489596d318b7390a25b6bef22ba680cbfa34f878bf47a366b1de3ec538d854
```

Verify it after downloading:

```sh
shasum -a 256 DockSpark-0.3.2.dmg DockSpark-0.3.2.zip
```

## Feedback

Please use [GitHub Issues](https://github.com/DockSpark/DockSpark/issues) to
report bugs or suggest improvements. Include your macOS version, browser
version, and steps to reproduce the problem when reporting a bug.

This repository contains DockSpark's public release materials. Application
source code is not included.
