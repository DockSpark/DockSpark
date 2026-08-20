# Changelog

All notable changes to DockSpark are documented in this file.

## [0.1.0] - 2026-08-21

### Added

- Firefox profile switching and global Private Browsing from the Dock hover
  popover
- Firefox profile detection from legacy `profiles.ini` and current Profile Group
  metadata, with custom display names kept separate from the real profile path
- New installations show Safari plus installed copies of Google Chrome and
  Firefox in the sidebar by default

### Fixed

- Content changes unexpectedly resizing the main window
- Development and Release builds running at the same time and competing for Dock
  hover events

### Improved

- Refreshed sidebar and browser list with clearer selection states, rounded app
  icons, subtle borders, and installed browsers shown first
- Chromium profile selection now defaults to the first available profile,
  removes the empty selection, and preserves customized display names when
  profile metadata is refreshed
- Browsers that are not running now use their system app icon consistently in
  the hover popover
- Simplified Chinese and English profile labels and guidance

### Notes

- Firefox support currently targets the standard Firefox release, not Firefox
  Developer Edition or Nightly
- Firefox profile discovery may require Full Disk Access; if no profile metadata
  can be read, refresh after granting access and reopening DockSpark
- Other supported Chromium browsers are not enabled in the sidebar by default;
  add installed browsers from the app list in the lower-left corner
- If both the menu bar and Dock icons are hidden, reopen DockSpark from Launchpad
  or Applications after closing its window

## [0.0.9] - 2026-08-17

### Added

- **Menu Bar Icon** and **Dock Icon** toggles in General settings
- Website, release notes, documentation, and **Send Feedback…** actions in the
  Help menu, including a localized, prefilled feedback form
- Website and X/Twitter links on the About page, plus a version badge
- A notarized DMG for drag-to-Applications installation

### Fixed

- Incognito label movement when switching profiles

### Improved

- Grouped General settings layout and a Settings window that resizes for the
  current page
- Simplified Chinese and English localization coverage
- Settings window behavior when the Dock icon is hidden

### Notes

- The main-window sidebar currently lists only Safari and Google Chrome; other
  supported browsers remain available via Dock hover
- If both the menu bar and Dock icons are hidden, reopen DockSpark from Launchpad
  or Applications after closing its window

## [0.0.8] - 2026-08-13

### Added

- **Check for Updates…** on the menu bar status item, so updates can be checked
  without opening Settings
- Confirmation before deleting a profile, with restore if deletion fails
- An explanation before opening System Settings when Full Disk Access is needed
  to read Chromium profiles

### Fixed

- Leftover hover popovers after the mouse leaves a Dock icon

### Improved

- Error messages when Chromium profile refresh fails
- Simplified Chinese localization coverage
- Distinct Debug and Release app icons so development builds are easier to tell
  apart from the installed release app

### Notes

- The main-window sidebar currently lists only Safari and Google Chrome; other
  supported browsers remain available via Dock hover

## [0.0.7] - 2026-08-12

### Added

- Dock profile switching for Chromium, Microsoft Edge, Brave, Vivaldi, Opera,
  Opera GX, and Arc
- Manual **Check for Updates…** action in Settings

### Improved

- Chrome profile detection and sync, including directory vs display names and
  renamed-profile caching
- Accessibility permission recovery and Dock hover observation rebuild
- Lower latency from Dock hover to popover presentation
- Separate Debug and Release app identities so development builds do not
  interfere with the installed release app

### Notes

- The main-window sidebar currently lists only Safari and Google Chrome; other
  supported browsers remain available via Dock hover

## [0.0.6] - 2026-08-10

### Fixed

- Corrected Safari installation-status detection for more accurate browser-list
  results

### Changed

- Completed missing Simplified Chinese and English interface translations
- Removed obsolete Firefox translation entries

## [0.0.5] - 2026-08-07

### Added

- Dock hover popover for switching browser profiles
- Profile switching support for Safari and Google Chrome
- Browser and profile management interface
- English and Simplified Chinese localization
- Permission onboarding for Accessibility and Automation
- Sparkle-based in-app update checks

### Distribution

- Signed with a Developer ID Application certificate
- Notarized by Apple with a stapled ticket
- Supports macOS 14.0 or later on Apple silicon and Intel Macs

[0.1.0]: https://github.com/DockSpark/DockSpark/releases/tag/v0.1.0
[0.0.9]: https://github.com/DockSpark/DockSpark/releases/tag/v0.0.9
[0.0.8]: https://github.com/DockSpark/DockSpark/releases/tag/v0.0.8
[0.0.7]: https://github.com/DockSpark/DockSpark/releases/tag/v0.0.7
[0.0.6]: https://github.com/DockSpark/DockSpark/releases/tag/v0.0.6
[0.0.5]: https://github.com/DockSpark/DockSpark/releases/tag/v0.0.5
