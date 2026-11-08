# DockSpark troubleshooting

Baseline: DockSpark 0.5.1, reviewed 2026-11-08. Find authoritative sources in
[SKILL.md](../SKILL.md); see [Usage](usage.md) for setup and permission details.

## Start with the symptom

Distinguish a missing hover panel, a missing profile, and an action that opens
the wrong profile. Ask only for details needed by that branch: DockSpark and
macOS versions, exact browser name/version, what happens, and what was expected.
For placement problems also ask about Dock orientation, auto-hide, displays,
and other Dock utilities. Do not start by asking for logs or reinstalling.

After each relevant correction, retry the failing interaction. If documented
checks do not resolve it, collect a report rather than repeating resets.

## No hover panel

1. Open DockSpark from Applications; closing its main window is fine, quitting
   it stops hover access. If both app icons are hidden, use Applications or
   Launchpad to reopen it.
2. Confirm the exact browser edition is supported, installed, configured and
   enabled in DockSpark, and its icon is kept in the Dock. Check Free limits if
   a browser is marked unavailable.
3. Check DockSpark's Accessibility permission in System Settings > Privacy &
   Security. After enabling it, reopen DockSpark and hover again.
4. With auto-hide, reveal the Dock fully before hovering. On older releases,
   update and retry if the panel appears slowly, closes too soon, or lingers
   after the pointer moves away. 0.5.1 improved hover and dismissal for bottom,
   left, and right Docks. For persistent issues, record Dock/display layout and
   any Dock utilities.

If the panel appears but clicking an entry fails, inspect any macOS Automation
prompt or the browser-specific permission under Privacy & Security, then retry
the action. Full Disk Access addresses profile reads; it is not a general fix
for hover detection.

## Browser or profile missing

1. Confirm the browser is installed. Add other supported browsers through the
   app list in the lower-left corner; they are not all added by default.
2. Confirm the actual profile exists and works in the browser. Refresh the
   corresponding browser's profiles in DockSpark where available.
3. If Chromium/Firefox metadata cannot be read, follow the app's Full Disk
   Access guidance, reopen DockSpark, then refresh. A permission grant does not
   create a profile or make an unsupported browser edition supported.
4. If it exists in the main window but is absent from the hover menu, check
   **Show in Dock** and whether Free plan limits mark it unavailable.

For Firefox, confirm it is the standard release, not Developer Edition or
Nightly. Discovery can use `profiles.ini` or newer Profile Group metadata;
refresh after granting needed access. Do not rewrite those files, invent a
Chromium-style profile directory, or delete Firefox data as a repair.

## Wrong browser identity opens

For Chrome, open the intended profile directly in Chrome and visit
`chrome://version`. Compare the last directory in Profile Path with the
directory configured/detected by DockSpark. `Work` is a display label, while
`Default` or `Profile 1` can be the actual directory. Refresh discovery and
correct the mapping before testing again. Do not infer a directory from the
label or rename a browser folder to match it. Check equivalent official
browser information for other Chromium browsers instead of assuming all use
Chrome's internal URL.

For Safari, compare the order of named entries with Safari's Profiles menu.
If switching fails only while Safari is starting, update from older versions
and compare with a retry after Safari is fully open. 0.5.1 improves cold-start
switching and reports timeouts separately from denied Automation access.
Check the Safari and System Events entries under **Privacy & Security >
Automation** when DockSpark reports denied access. Include the exact error and
whether Safari was already running if the issue persists.

For Firefox, verify the selected entry is bound to the intended profile in the
detected list. If a Chromium directory edit appears unsaved, move focus out of
the field and check that the value matches an actual profile directory.

## Permission or update problems

- Check the relevant permission on the Applications copy of DockSpark and
  reopen it after changes. Tell the user which capability needs that permission.
- For update failures, record the installed version and exact message, then
  check the official release page and app update action. A manual official app
  asset is an alternative if the updater remains unavailable.
- If macOS blocks installation, capture the exact message and confirm the
  package came from official Releases. Do not prescribe removing quarantine,
  disabling Gatekeeper, or accepting a checksum from another version.
- Do not offer `tccutil` resets, Keychain removal, or Application Support/browser
  data deletion as routine recovery. A failure to fetch documentation is not
  evidence that the user's app or network is broken.

## License or limit problems

Check whether the behavior is a Free limit or an activation error. Free allows
one enabled browser and three named profiles; private entries are excluded.
Existing over-limit entries remain configured. Disabling another item or
activating Pro can restore availability without deleting profiles.

For activation, refresh, or deactivation, check connectivity and the message
shown in **Settings > License**. Use the app's purchase or recovery links when
needed.

- On 0.5.0, upgrading from older license storage required one online
  verification. On 0.5.1, a valid local license issued before 0.5.0 can migrate
  offline on the same Mac if the installation has never established the newer
  verification baseline. The existing activation carries over automatically.
- If DockSpark asks to verify the license or system clock, check the Mac's
  date and time, connect to the internet, and reopen DockSpark so it can check
  the existing activation. Use **Refresh License** in **Settings > License**
  when that button is available. Online verification is required when an
  established baseline is missing or damaged, or the system clock was set back
  substantially.
- A connection failure leaves a verified Pro license usable through its
  signed validity and offline grace periods. On 0.5.1, DockSpark retries a
  pending refresh when connectivity returns. If the warning persists, capture
  the exact message. Use **Recover License** if you need to retrieve your key.

## Escalate unresolved problems

Use **Help > Send Feedback…** or
[GitHub Issues](https://github.com/DockSpark/DockSpark/issues). Search existing
reports for the same symptom/version when possible, and distinguish reported
workarounds from officially confirmed fixes. Prepare a concise draft with:

- DockSpark version/build if available, macOS version, exact browser/version.
- Reproduction steps, expected result, actual result, and exact error text.
- Relevant permission status and the checks already attempted.
- Dock/display details for placement issues; a cropped/redacted screenshot if
  it helps explain the problem.

Do not request license keys, refresh tokens, Keychain contents, full browser
profile folders, or browsing data. Redact account names, emails, and personal
paths from screenshots/errors before a public report. Prepare the report for
the user; submit or send it only when the user explicitly asks.
