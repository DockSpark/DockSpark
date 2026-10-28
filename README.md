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
- Use the app in English, Simplified Chinese, Traditional Chinese, Japanese,
  Korean, German, French, or Spanish
- Scale hover popovers with the Dock icon size, including magnification
- Turn off anonymous usage analytics in General settings

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

Safari, Google Chrome, and Firefox are enabled by default when installed.
The Free plan allows one enabled browser and three named profiles per browser;
Private Browsing and Incognito entries do not count toward the profile limit.
Pro removes these limits. Add other installed browsers from the app list.

## Install

### Homebrew

```sh
brew trust --cask dockspark/tap/dockspark && \
  brew install --cask dockspark/tap/dockspark
```

### Manual download

1. Open the [latest release](https://github.com/DockSpark/DockSpark/releases/latest).
2. Download `DockSpark-0.5.0.dmg`. Do not download GitHub's automatically
   generated source code archives.
3. Open the disk image and drag `DockSpark.app` to the Applications folder.
4. Launch DockSpark and grant the requested macOS permissions.

The `DockSpark-0.5.0.zip` asset is also available for manual installation.

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

## AI assistant skill

The [DockSpark skill](skills/dockspark/SKILL.md) helps an AI assistant explain
what DockSpark does and when it is useful, guide installation and everyday
use, find official documentation, and troubleshoot common problems.
Skill version **0.5.0** follows the App version; its bundled guidance was
reviewed against DockSpark 0.5.0. The assistant answers in your language.

Install it with the [Skills CLI](https://github.com/vercel-labs/skills)
(requires Node.js; see its documentation for current requirements):

```sh
npx skills add DockSpark/DockSpark --skill dockspark
```

Choose your AI assistant when prompted. Installation is for the current project
by default; add `-g` for global installation. The GitHub command requires the
skill to have been published to this repository. From a local checkout, use:

```sh
npx skills add . --skill dockspark
```

For [manual installation in Codex](https://developers.openai.com/codex/skills/),
copy the entire `skills/dockspark` directory,
including `references/` and `agents/`, into `~/.agents/skills/dockspark` (or
`.agents/skills/dockspark` in your project). Other assistants may use different
skill directories. Reload your assistant's skills or start a new session if
the skill does not appear.

Example prompts:

- `Use $dockspark to explain what DockSpark can help me do.`
- `Use $dockspark to help me configure Chrome profiles.`
- `Use $dockspark to troubleshoot why hovering over a Dock icon does nothing.`

You can ask the same questions in Chinese or another language. The skill
provides guidance; install DockSpark separately to use the app. For each new
App release, review the skill's guidance and official links and update its
version and reviewed baseline together.

## Screenshot

![DockSpark profile management window](Assets/img_dockspark.jpg)

> The screenshot previews the DockSpark interface. Version 0.5.0 supports Dock
> profile switching for Safari, Firefox, Chrome, and other Chromium-based
> browsers listed above.

## Updates

DockSpark uses Sparkle for in-app updates. You can also download releases
manually from the [Releases](https://github.com/DockSpark/DockSpark/releases)
page.

## Release integrity

The SHA-256 checksums are:

```text
DockSpark-0.5.0.dmg  90c0f9369d67eb33e6939b1cac008ec70277f7c176c0f2a1aa0e50fb08e85eff
DockSpark-0.5.0.zip  1d7eb10b9ce7736f2a1e5f1fd790eebb399675fadb95702a6032f329f65db129
```

Verify it after downloading:

```sh
shasum -a 256 DockSpark-0.5.0.dmg DockSpark-0.5.0.zip
```

## Feedback

Please use [GitHub Issues](https://github.com/DockSpark/DockSpark/issues) to
report bugs or suggest improvements. Include your macOS version, browser
version, and steps to reproduce the problem when reporting a bug.

This repository contains DockSpark's public release materials. Application
source code is not included.
