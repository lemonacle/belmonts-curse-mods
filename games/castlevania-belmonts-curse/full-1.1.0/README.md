# Belmont's Curse Mods — full game 1.1.0

One patch-only collection with independently selectable mod folders. No game files, RomFS overrides, builders, keys, saves, or additional runtime dependencies are included.

**Compatibility:** Switch full game **1.1.0**, title ID `0100BA4026E94000`, executable build ID `0F1169AA7D0FA4529C861F96ADEC306E`. Requires emulator `.pchtxt` support; testing focused on Eden and Retroid Pocket Nova. Native Switch hardware is not validated. These patches are not for the demo or other updates.

## Installation and updates

1. Back up saves before using NG+ or Relic Toggle.
2. Extract the ZIP. Copy only your chosen named mod folders into the game's mod directory. Each named folder must directly contain `exefs`. Keep this README and LICENSE on your computer.
3. Disable superseded versions. For NG+, disable all older NG+ executable patches **and their RomFS menu overrides**. Disable old credits, fast-travel, video, and RenderScale add-ons when using their integrated replacements.
4. Enable your chosen mods and fully restart. Set the emulator aspect ratio to 4:3 only when using the 4:3 mod. If using a folder importer, import each named mod folder separately, not the whole collection.

The six normal components below have no overlapping patch ranges and may be selected independently, except Manual Zoom requires 4:3. **Relic Restore Three is a recovery tool, not a seventh mod to enable alongside everything. Never enable it with Relic Toggle.**

| Folder | Behavior | Requirements / notes |
| --- | --- | --- |
| `4x3 v5 (1.1.0)` | Expanded 1280x960 framing; menu, camera, title/loading, video, fast-travel and credits fixes | Emulator aspect ratio 4:3; added vertical view can reveal unfinished scenery |
| `RenderScale Fix v3 (1.1.0)` | Keeps internal render scale at 1.0 at startup and through runtime scale changes | Independent of aspect ratio; higher GPU load; does not change the emulator's resolution multiplier |
| `Manual-Zoom v3 (1.1.0)` | R3 toggles expanded framing and a closer, original-height view on tracking cameras | Requires 4:3; excludes static/fixed and rail cameras; existing R3 game actions remain active |
| `NGPlus-v15` | True-ending-gated NG+ with carryover/reset rules and a runtime-created R prompt and destination menu | Executable-only version approved after Test 2; choose an empty destination |
| `Speed-v1` | Doubles Rose's normal locomotion speed | Player movement only; enemy speed and global timing unchanged; speed bonuses apply before the multiplier |
| `Relic-Toggle-v1` | Toggle owned relics individually in the collection grid; up to 45 active | Native confirm/equip button; see save and uninstall requirements below |
| `Relic-Restore-Three` | Recovery/uninstall companion for expanded relic saves | Use only with Relic Toggle disabled; see procedure below |

## NG+ details

Highlight a save that has reached the **true ending**, press **R**, choose an **empty destination**, and confirm. Eligibility uses the selected save's true-ending record, not its displayed collection percentage or profile-wide unlocks. Ordinary X Duplicate remains available. The source save is retained.

NG+ keeps retained equipment, permanent upgrades, other purchased talents, collection pickup records, tutorial/codex knowledge, and elapsed time. Cleanup keeps one copy of each retained item ID; different weapon tiers remain separate. Level, traversal, story, map exploration, and other world state reset. Story quest pickups reset so they can be obtained again.

Cursed Flame replaces Absolution, starts equipped, and resets its purchased Big Fireball upgrade and Works of Mercy progress. Other Works of Mercy carry over. The intro startup path is retained. NG-only guards suppress repeated health/mana upgrade grants and force-duplicate equipment grants.

Creating NG+ enables custom balance: **0.5x damage dealt, 3x enemy/trap damage received, and 3x XP**. These settings are shared across the profile and remain editable in-game. Installation itself does not edit saves or preferences. Disabling NG+ does not automatically revert previously selected profile-wide balance settings or remove saves already created.

## Relic Toggle and safe removal

Select an owned relic in the collection grid and press the normal confirm/equip button to toggle it on or off. Up to 45 relics can be active. The grid's equipped marker is authoritative: the original three header slots remain visible and show only the first three positions. There is no equip-all shortcut or automatic equipment. Normal relic effects and restrictions still apply.

Extra equipped selections are stored in the existing `equippedCharmItems` save list. This differs from the PC reference's separate configuration and vanilla-compatible three-entry saves. **Do not simply disable Relic Toggle and load an expanded-relic save in the unmodified game.** Keep a backup.

To uninstall safely:

1. Disable Relic Toggle and enable **Relic-Restore-Three** instead.
2. Fully restart, load each affected save, and save normally.
3. Quit, then disable Restore Three.

Recovery keeps the first three equipped positions and removes extra equipped selections; owned relics remain in inventory. It supports normal three-entry saves and Relic Toggle's 45-entry saves. Recovery has passed static checks but has not been confirmed in-game. Never enable both relic patches together.

Some relic combinations may expose base-game effect-cleanup bugs. The PC reference documents an Eldritch Talisman/defense-relic black-screen issue and a fix; that PC fix is **not** included here. In-game validation of this Switch relic implementation is not recorded, so its behavior should not be treated as covered by the completed playthroughs.

## Testing, known reports, and support

I've completed a playthrough and an NG+ playthrough, using Speed as a testing utility to expedite progress. The executable-only NG+ Test 2 was approved for release after testing. This does not mean every component, relic combination, room, cutscene, or device has been exhaustively tested.

This is probably my last planned mod update for this game. I'm still open to feedback and may be able to fix issues, but I won't be playing more of the game or playtesting further mods for the foreseeable future. Further fixes and testing are not guaranteed.

One doppelganger post-fight progression lock was reported: the boss dissolved but no absorption orb appeared, and pressing R did nothing. A replay test **did not reproduce it**; the cause remains unconfirmed and is not established as a mod defect. The workaround that resolved the original occurrence was to exit fully, temporarily disable the mods, replay the fight, save after progressing, then exit, re-enable the mods, and restart. This is a reported workaround, not a confirmed underlying fix.

Some large rooms may have performance hiccups. Expanded framing may expose unfinished scenery. Credits/menu letterboxing can retain the game's background color. Manual Zoom may need further testing on script-controlled cameras.

Please report issues at https://github.com/lemonacle/belmonts-curse-mods/issues with the game/build ID, emulator/device, enabled mods, exact location or menu sequence, reproduction steps and screenshots. Where practical, compare with the relevant mod disabled. Do not upload game dumps, keys or private saves. NG+ and relic saves require the precautions above when changing enabled mods.

## Credits and license

The relic mod used **Charms Unlimited by kkyleeb21** as a behavioral reference:
https://www.nexusmods.com/castlevaniabelmontscurse/mods/37

This is an independent Switch implementation, not a redistribution or binary port of the PC plugin. No PC reference DLL code or assets are included. The Switch implementation uses native expanded relic/save arrays; it does not reproduce the PC mod's configuration-file persistence, equip-all shortcuts, automatic equipment, or PC-specific bug fixes. Credit for the PC mod remains with kkyleeb21; its files retain their own permissions and are not covered by this collection's MIT license.

Original patches and documentation in this collection: copyright 2026 lemonacle, MIT licensed; see the single root LICENSE. Game names identify compatibility; this project is not affiliated with the developers or publishers.

Repository: https://github.com/lemonacle/belmonts-curse-mods
The demo patch remains in the historical demo release and must not be used with these full-game mods.
