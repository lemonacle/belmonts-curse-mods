# Belmont's Curse Mods

Nintendo Switch mods and practical notes for Castlevania: Belmont's Curse, with testing focused on the Retroid Pocket Nova and Eden. **Patches and tools only: no games, extracted assets, firmware, keys, or saves.**

## Downloads

Download the **[full-game mod collection](https://github.com/lemonacle/belmonts-curse-mods/releases/latest)**: one ZIP, one README, one LICENSE, and separate folders for 4:3, RenderScale, Manual Zoom, NG+, Speed, Relic Toggle and its Restore Three recovery companion. Install only the folders you want; never combine Relic Toggle and Restore Three.

See the [collection README](games/castlevania-belmonts-curse/full-1.1.0/README.md) for compatibility, installation, NG+ rules, relic save handling, PC reference credit, testing limits, known issues and support status.

The author has completed a playthrough and an NG+ playthrough, using Speed to expedite testing. This is probably the last planned update. Feedback is welcome and fixes may be possible, but further playtesting is not planned for the foreseeable future.

The [demo 1.0.0 patch](https://github.com/lemonacle/belmonts-curse-mods/releases/tag/belmonts-curse-v1) remains in its historical release. Do not mix demo and full-game patches.

## Find an existing mod first

This is a small collection, not a complete Switch mod index. Before requesting or developing a new fix, check these projects:

| Project | What to look for |
| --- | --- |
| [pakrett / Aspect-Ratio-Mods](https://github.com/pakrett/Aspect-Ratio-Mods) | A collection focused on 4:3 displays; start with its Switch section. |
| [StevensND / switch-port-mods](https://github.com/StevensND/switch-port-mods) | Per-game Switch emulator mods, including aspect-ratio and performance work. Read each game's supported versions. |
| [pacoa-kdbg / Switch-Emulator-Ultrawide-FPS-Mods](https://github.com/pacoa-kdbg/Switch-Emulator-Ultrawide-FPS-Mods) | Another place to search for game-specific aspect-ratio and FPS work. Check the actual ratios offered. |
| [yuzu-mirror / yuzu-mod-archive](https://github.com/yuzu-mirror/yuzu-mod-archive) | Historical mod listings with version and author information. This is a mirror, not the original emulator organization. |

These links are discovery resources, **not compatibility endorsements**. Not every mod in them supports 4:3, Eden, or your game update. Prefer the original author's release and instructions, and link upstream rather than copying their work here.

## Want to make or update a mod?

Start with the **[contributor guide and resources](docs/CONTRIBUTING.md)**. It covers finding prior work, matching builds, distinguishing stretching from cropping, UI and camera pitfalls, and publishing patches without game data.

Useful starting points:

- [StevensND's Ghidra/IDA and aspect-ratio porting guide](https://github.com/StevensND/ghidra-port-mods-guide)
- [Ghidra](https://github.com/NationalSecurityAgency/ghidra)
- [UnityPy](https://github.com/K0lb3/UnityPy), for inspecting Unity assets from your own dumps
- [Capstone](https://github.com/capstone-engine/capstone), for instruction inspection

I've also worked on 4:3 fixes for PC gamesâ€”you can find those on [my GitHub profile](https://github.com/lemonacle).

## Reporting an issue

Include the title ID, game version/build ID, emulator version, device, enabled mods, aspect-ratio setting, and the room or menu where it happens. A comparison from the same position with the mod disabled is especially useful. Redact personal paths from logs. Do not upload dumps, keys, saves, or extracted game bundles.

Original scripts, documentation, and patch contributions here are MIT licensed. Linked projects retain their own authorship and licenses. Game names identify compatibility; this repository is not affiliated with the developers or publishers.
