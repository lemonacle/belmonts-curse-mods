# Contributing to Belmont's Curse Mods

This repository contains the Switch mods for Castlevania: Belmont's Curse documented in the [main README](../README.md). Contributions should address these mods, their supported builds, or their documentation. Feedback is welcome, but the maintainer is not planning further playthroughs or ongoing mod testing; review and fixes may be limited.

## Report or describe the change

Check existing issues and the [full-game collection README](../games/castlevania-belmonts-curse/full-1.1.0/README.md) for known behavior and installation requirements. Explain the problem, the affected component, the steps that reproduce it, and the expected result. Include the emulator/device and enabled mods. For a proposed fix, distinguish static checks from results observed in-game.

## Match the supported build

The current full-game patches target game **1.1.0**, title ID `0100BA4026E94000`, executable build ID `0F1169AA7D0FA4529C861F96ADEC306E`. The demo **1.0.0** is a separate build with different title and executable IDs, documented in the [version notes](../games/castlevania-belmonts-curse/README.md).

Changing a build-ID header does not port a patch. For a new game update, re-identify the affected functions, original instructions, branch targets, and any reused code regions. Record hashes for local inputs and keep original game files private. Existing entries in `builds.json` describe particular patches or legacy builder inputs; the collection README is the complete guide to the released components.

## Validate the affected behavior

- **4:3 and camera changes:** compare the same position with the patch disabled. Check gameplay tracking, room transitions, fixed/rail cameras, menus, videos, credits, and return to title. The 4:3 mod preserves horizontal coverage and adds vertical view, which can expose unfinished scenery. A global zoom change can introduce tracking problems elsewhere.
- **RenderScale:** check cold launch and transitions between gameplay, save menus, and the main menu. Runtime settings can overwrite an initial scale value.
- **Manual Zoom:** check R3 toggling, excluded camera types, transitions, and restart behavior alongside 4:3.
- **NG+:** check true-ending eligibility, R prompts, destination selection, cancel, ordinary Duplicate, source-save preservation, and the documented carryover/reset rules. Confirm that older NG+ RomFS overrides are disabled when testing the executable-only version.
- **Speed:** check player locomotion and confirm that enemy movement and global timing are unaffected.
- **Relics:** use backed-up saves to check toggling, effects, saving/loading, death, mirrors, and travel. Preserve the documented distinction between expanded-relic saves and normal three-entry saves. Test recovery separately; never combine Relic Toggle and Restore Three.

Check executable patch ranges against all supported normal components. Restore Three deliberately replaces relic behavior and is mutually exclusive with Relic Toggle. No-overlap checks alone do not prove runtime compatibility.

## Keep contributions reproducible

Describe what changed, why, the exact build, and what was tested. Preserve unrelated patch bytes. Provide installation and rollback instructions if behavior changes, including any persistent save or profile-setting effects. Do not describe untested behavior as confirmed.

The full-game release uses executable patches only. Share patch definitions and original supporting code/documentation; do not commit game dumps, original executables, asset bundles (including modified bundles), extracted metadata, firmware, keys, or private saves. The demo's legacy RenderScale builder produces a local modified bundle from a matching original dump; generated game data stays private.

Credit any prior work and link the exact source. Relic Toggle's behavioral reference is [Charms Unlimited by kkyleeb21](https://www.nexusmods.com/castlevaniabelmontscurse/mods/37); the PC plugin is not included or covered by this repository's MIT license. Respect the reference project's permissions when proposing changes.

## Tools used for investigation

[Ghidra](https://github.com/NationalSecurityAgency/ghidra) and [Capstone](https://github.com/capstone-engine/capstone) can support executable inspection. [UnityPy](https://github.com/K0lb3/UnityPy) was used for local Unity asset inspection and the legacy demo builder. These are development references, not dependencies required to install the full-game mods.
