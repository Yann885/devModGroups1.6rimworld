# Mod Groups

A RimWorld mod that adds custom, collapsible **groups** to the mod list — so you can
organize a long mod list into your own categories instead of scrolling through one
flat list.

![RimWorld version](https://img.shields.io/badge/RimWorld-1.6-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)

## Features

- A **"Mod Groups"** button injected into the vanilla mod list screen
- Create your own named groups (e.g. "Core", "Graphics", "Combat overhaul")
- Assign any installed mod to a group via **Move to..**
- **Multi-select**: tick several mods at once and move them all to a group in one action
- Expand/collapse each group independently to keep long lists manageable
- Toggle every mod in a group on/off at once from the group's own checkbox
- Groups persist across every save/playthrough (stored in your RimWorld config folder,
  not tied to a specific mod list or save file)

## Installation

**Steam Workshop:** *(add your Workshop link here once published)*

**Manual:** download the latest release, or clone this repo, and drop the folder into
your RimWorld `Mods` folder. Requires the [Harmony](https://steamcommunity.com/sharedfiles/filedetails/?id=2009463077)
mod as a dependency (RimWorld will prompt for it automatically via Workshop).

## Known limitations / roadmap

- No drag-and-drop yet — moving mods between groups goes through a dropdown menu
  (with multi-select for moving several at once).
- No color-tagging for groups yet.
- No export/import of a group layout to share with others.
- The Harmony patch targets `Page_ModsConfig.DoWindowContents` positionally (via
  Harmony's `__0` binding) so it survives internal parameter renames, but a RimWorld
  update that changes the method's parameter type/order/count — most likely on a
  major version bump (e.g. 1.6 → 1.7) — could still break it. If that happens, the
  mod logs a clear `[Mod Groups] Failed to apply Harmony patches` error instead of
  crashing, and the fix is usually a one-line update to the patch.

## Contributing

Issues and PRs welcome. If you're adding a feature from the roadmap above, a quick
issue first is appreciated so effort doesn't overlap.

## License

MIT — see `LICENSE`.
