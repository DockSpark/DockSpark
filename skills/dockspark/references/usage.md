# DockSpark usage

Baseline: DockSpark 0.5.1, reviewed 2026-11-08. Use the official source table in
[SKILL.md](../SKILL.md) to check later releases or exact UI instructions.

## Requirements and browsers

- macOS 14.0 or later, on Apple silicon or Intel.
- A supported browser installed and kept in the Dock.
- Supported browsers: Safari, Firefox (standard release), Google Chrome,
  Chromium, Microsoft Edge, Brave Browser, Vivaldi, Opera, Opera GX, and Arc.
  Firefox Developer Edition and Nightly are not supported in this baseline.
- Safari, Chrome, and Firefox are enabled by default when installed, subject
  to the current plan. To switch browsers on Free, disable the active browser
  in the app list in the lower-left corner, then enable the one you want.

## Install and update

For Homebrew installation, the public README provides:

```sh
brew trust --cask dockspark/tap/dockspark && \
  brew install --cask dockspark/tap/dockspark
```

For manual installation, open the official latest release, choose the
`DockSpark-<version>.dmg` app asset, open it, and drag `DockSpark.app` into
Applications. Launch that installed copy. A versioned ZIP app asset is also
available. GitHub's generated source archives are not installable app packages.

The [0.5.1 release](https://github.com/DockSpark/DockSpark/releases/tag/v0.5.1)
is build `20261107.1`. The app and DMG are Developer ID signed and Apple
notarized. Compare a download's SHA-256 with the checksum for its exact version
and filename on the release page.

Use **Check for Updates…** in the app, or download the desired release
manually. DockSpark uses Sparkle for in-app updates. The 0.5.1 in-app release
notes are available in Simplified Chinese and English. Other app languages
show the English notes for this release.

## Permissions

Review permissions under **System Settings > Privacy & Security**:

| Permission | Why it is used | When to check it |
| --- | --- | --- |
| Accessibility | Detect the hovered Dock icon and its position | The hover panel does not appear |
| Automation | Control Safari and System Events when switching profiles or opening a private window in Safari | macOS requests consent or a Safari action reports denied access |
| Full Disk Access | Read Chromium/Firefox profile metadata when access is needed | Profile discovery cannot read the browser's metadata |

Full Disk Access is optional, not a requirement for every feature. Follow the
app's explanation when it is needed. Automation authorization can first appear
when the relevant browser action is attempted. After changing permissions,
reopen DockSpark and retry; refresh profiles for discovery problems.

## Configure and use profiles

1. Create the desired profile in the browser and confirm it works there.
2. Open DockSpark, select or add the installed browser, and configure its
   profiles. Use discovery/refresh where available.
3. For Chromium browsers, keep the actual directory separate from the display
   label: a profile called `Work` can live in `Profile 1`. Use the detected
   directory, not a guessed sequence. In Chrome, `chrome://version` in the
   intended profile shows its Profile Path; the final directory identifies it.
4. Customize the display name and color as needed. In 0.5.1, changes to the
   name and manually entered Chromium directory are validated and saved when
   you submit the field or move focus away. Turn on **Show in Dock** for each
   named profile you want in the hover menu.
5. Keep that browser's icon in the Dock, hover over it, move into the panel,
   and select the profile. Confirm the intended browser identity opens.

Example: create work and personal Chrome profiles in Chrome, refresh their
entries in DockSpark, give them recognizable labels, then select either one
from Chrome's Dock icon. Changing a DockSpark label does not rename its real
browser directory or move browser data.

For Safari, arrange named entries in the same order as Safari's Profiles menu.
Hidden named entries still occupy a shortcut position. The Private entry uses
its own shortcut. For Firefox, bind each named entry to a profile from the
detected list. Discovery reads Profile Group metadata or `profiles.ini`.
Chromium also supports entering the real profile directory manually when
discovery is unavailable.

Choose the panel's **Private Browsing** or **Incognito** entry for a private
window. These entries do not count as named profiles for Free limits. Do not
describe private browsing as anonymity or as another saved account profile.

## Dock and general settings

- Bottom, left, and right Dock layouts are supported, including auto-hide in
  typical setups. Unusual display arrangements or Dock utilities can affect
  positioning.
- Move from the browser icon toward the panel. In 0.5.1, hover response and
  dismissal work more reliably across Dock positions. The panel dismisses
  after the pointer leaves the icon and panel. Press Esc or Command-W to
  close it immediately.
- Closing the main window leaves DockSpark running for hover access. Use
  **Quit DockSpark** to stop it.
- General settings can show or hide its menu bar and Dock icons. If both are
  hidden, reopen DockSpark from Applications or Launchpad.
- Liquid Glass is available on macOS 26 or later and is off by default.
- DockSpark follows the app language selected in macOS. Version 0.5.1 improves
  contrast on light profile labels and corrects several translations.
- Anonymous usage analytics can be disabled in General settings.
  Local profile configuration has no cloud sync; this is separate from browser
  sync and from app analytics, updates, and license verification.

## Free and Pro

Free allows one enabled browser and up to three named profiles per browser.
Built-in Private Browsing/Incognito entries do not count. Pro removes these
browser and profile limits. Over-limit configurations are preserved; disable
another item or activate Pro to make room rather than deleting browser data.

Manage activation, refresh, or deactivation under **Settings > License**.
These operations need internet access. A verified license can continue within
its validity and offline grace periods; do not promise indefinite offline use
or an undocumented grace duration. Use the official website or in-app links
for current purchase and recovery information instead of hardcoding prices.
For offline upgrades and verification errors, see
[license troubleshooting](troubleshooting.md#license-or-limit-problems).
