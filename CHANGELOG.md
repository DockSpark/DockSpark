# Changelog

All notable changes to DockSpark are documented in this file.

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

[0.0.8]: https://github.com/DockSpark/DockSpark/releases/tag/v0.0.8
[0.0.7]: https://github.com/DockSpark/DockSpark/releases/tag/v0.0.7
[0.0.6]: https://github.com/DockSpark/DockSpark/releases/tag/v0.0.6
[0.0.5]: https://github.com/DockSpark/DockSpark/releases/tag/v0.0.5
