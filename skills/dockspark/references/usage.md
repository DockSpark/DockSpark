# DockSpark usage

Baseline: DockSpark 0.5.0, reviewed 2026-10-28. Use the official source table in
[SKILL.md](../SKILL.md) to check later releases or exact UI instructions.

## Requirements and browsers

- macOS 14.0 or later, on Apple silicon or Intel.
- A supported browser installed and kept in the Dock.
- Supported browsers: Safari, Firefox (standard release), Google Chrome,
  Chromium, Microsoft Edge, Brave Browser, Vivaldi, Opera, Opera GX, and Arc.
  Firefox Developer Edition and Nightly are not supported in this baseline.
- Safari, Chrome, and Firefox are listed by default when installed. Add other
  installed browsers from the app list in the lower-left corner, and check
  which browser is enabled under the current plan.

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

The 0.5.0 release is Developer ID signed and Apple notarized. If verifying a
download, compare its SHA-256 with the official checksum for that exact version
and filename; do not reuse a checksum from another release.

Use **Check for Updates…** in the app (including its menu bar menu), or download
the desired release manually. DockSpark uses Sparkle for in-app updates.

## Permissions

Review permissions under **System Settings > Privacy & Security**:

| Permission | Why it is used | When to check it |
| --- | --- | --- |
| Accessibility | Detect the hovered Dock icon and its position | The hover panel does not appear |
| Automation | Ask a browser to perform an action when required | macOS requests consent or switching is blocked |
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
4. Customize the display name and color as needed. A named profile must have
   **Show in Dock** enabled to appear in the hover menu. Hiding it is different
   from deleting it.
5. Keep that browser's icon in the Dock, hover over it, move into the panel,
   and select the profile. Confirm the intended browser identity opens.

Example: create work and personal Chrome profiles in Chrome, refresh their
entries in DockSpark, give them recognizable labels, then select either one
from Chrome's Dock icon. Changing a DockSpark label does not rename its real
browser directory or move browser data.

Safari and Firefox have their own profile workflows; do not apply Chromium
directory names to them. Firefox discovery reads `profiles.ini` or Profile
Group metadata. Use the official docs for browser-specific steps rather than
inventing a profile creation feature in DockSpark.

Choose the panel's **Private Browsing** or **Incognito** entry for a private
window. These entries do not count as named profiles for Free limits. Do not
describe private browsing as anonymity or as another saved account profile.

## Dock and general settings

- Bottom, left, and right Dock layouts are supported, including auto-hide in
  typical setups. Unusual display arrangements or Dock utilities can affect
  positioning.
- Move toward the panel from the browser icon; it dismisses when the pointer
  leaves the icon and panel. Esc or Command-W dismisses it in 0.5.0.
- Closing the main window leaves DockSpark running for hover access. Use
  **Quit DockSpark** to stop it.
- General settings can show or hide its menu bar and Dock icons. If both are
  hidden, reopen DockSpark from Applications or Launchpad.
- Liquid Glass is available on macOS 26 or later and is off by default.
- Anonymous usage analytics can be disabled in General settings in 0.5.0.
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
