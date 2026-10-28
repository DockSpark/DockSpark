---
name: dockspark
description: Explain what DockSpark does, help users install and use its macOS Dock browser profile switcher, find official documentation, and troubleshoot permissions, profiles, updates, or licensing. Use for DockSpark product and user-support questions.
metadata:
  version: "0.5.0"
---

# DockSpark

## Explain the product

DockSpark is a native macOS utility that puts browser profiles in a popover next
to the browser's Dock icon. Hover over the icon, then choose a profile or open a
private/incognito window. It reduces repeated trips through browser profile
menus when moving between work, personal, development, or client environments.

It is useful for people who regularly switch browser identities. Create the
actual profiles in the browser first; DockSpark configures their shortcuts,
display names, colors, and visibility. It does not create browser accounts or
provide account or configuration cloud sync. Configuration stays on the Mac;
this does not mean the app never connects to the internet (updates, licensing,
and optional anonymous usage analytics have separate roles).

Explain these benefits with an example suited to the user's task. Answer in the
user's language and distinguish browser profiles from macOS user accounts.

## Choose the guidance

- For product questions, use the explanation above; avoid loading setup or
  diagnostics unless the user needs them.
- For installation, permissions, supported browsers, profile configuration,
  everyday use, updates, or Free/Pro limits, read
  [Usage](references/usage.md).
- For a failure or unexpected behavior, read
  [Troubleshooting](references/troubleshooting.md), then only the relevant
  usage section. Ask for missing details that change the diagnosis.

## Find official information

| Source | Use it for |
| --- | --- |
| [Official documentation](https://dockspark.app/en/docs) | Quick start, installation, permissions, profile management, private windows, Dock behavior, browser support, and troubleshooting; use its navigation or search to reach the relevant topic |
| [Chrome profiles guide](https://dockspark.app/en/guide/chrome-profiles) | Profile directories versus friendly names and Chrome setup |
| [Public README](https://github.com/DockSpark/DockSpark/blob/main/README.md) | Current public requirements, installation, supported browsers, and release integrity |
| [Changelog](https://github.com/DockSpark/DockSpark/blob/main/CHANGELOG.md) | Which version introduced or changed a behavior, plus upgrade notes |
| [Releases](https://github.com/DockSpark/DockSpark/releases) | Version-specific notes and downloadable app assets; use [latest release](https://github.com/DockSpark/DockSpark/releases/latest) for a new install |
| [Official website](https://dockspark.app/en) | Product overview, current plans, purchase/recovery links, and privacy notice |
| [GitHub Issues](https://github.com/DockSpark/DockSpark/issues) | Existing reports and unresolved problems; reports are evidence, not confirmed product guarantees |

For a version-sensitive question, identify the installed DockSpark version and
consult the relevant official page or release notes. A website page can lag
behind a release. Resolve conflicts using the release information for the
user's version, and say when evidence is incomplete. Do not call 0.5.0 the
latest version without checking Releases, or assume every newer feature exists
in an older installation. Include the relevant official link in the answer.

The bundled references were reviewed against DockSpark 0.5.0 on 2026-10-28.
When online sources cannot be reached, use those references as that version's
baseline and disclose that current behavior could not be verified. Do not
invent documentation URLs, UI labels, download hashes, prices, or fixes.

## Support boundaries and maintenance

This public repository distributes release materials and this skill; it does
not contain the application source. Do not assume access to a private checkout,
a DockSpark CLI, or a dedicated automation API. Guide users through the actual
app; use available UI tools only when the task calls for operating it.

Prefer settings and permission checks before invasive remedies. Do not delete
browser data, reset macOS permissions, remove Keychain entries, bypass macOS
security checks, or submit feedback as an implied troubleshooting step.

The skill version follows the App version. For each App release, review the
entrypoint, bundled references, official links, and README examples together,
then update `metadata.version` and the reviewed baseline/date to that release.
