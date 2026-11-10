# Belmont's Curse Mods

Optional Nintendo Switch mods for **Castlevania: Belmont's Curse**: 4:3 framing, internal render-scale correction, manual camera zoom, New Game+, movement speed, and expanded relic equipment. Testing focused on Eden and the Retroid Pocket Nova.

## Download and compatibility

Get the **[full-game mod collection](https://github.com/lemonacle/belmonts-curse-mods/releases/latest)** for game **1.1.0**. The ZIP contains one README, one LICENSE, and a separate folder for each mod. All components are executable `.pchtxt` patches; no game files, RomFS overrides, builders, or extra runtime dependencies are needed for the full-game collection.

Match title ID `0100BA4026E94000` and executable build ID `0F1169AA7D0FA4529C861F96ADEC306E`. Emulator `.pchtxt` support is required; native Switch hardware is not validated.

Install only the mod folders you want. Manual Zoom requires the 4:3 mod. **Relic Restore Three is an uninstall/recovery companion: never enable it alongside Relic Toggle.** Read the [collection README](games/castlevania-belmonts-curse/full-1.1.0/README.md) for installation, NG+ carryover rules, relic save handling, known issues, and removal instructions.

## Demo files

The demo **1.0.0** 4:3 patch remains in the [historical release](https://github.com/lemonacle/belmonts-curse-mods/releases/tag/belmonts-curse-v1). Its title and build IDs differ from the full game; see the [version notes](games/castlevania-belmonts-curse/README.md). The legacy demo RenderScale builder is retained under `tools/` for users with their own matching dump. It is not needed for the full-game collection.

## Testing and support

I've completed a playthrough and an NG+ playthrough, using Speed as a testing utility to expedite progress. The executable-only NG+ version was approved after Test 2. This does not establish coverage of every optional component, relic combination, room, or device; see the collection README for testing limits.

This is probably my last planned mod update for this game. Feedback is welcome and I may be able to fix issues, but I won't be playing more of the game or playtesting further mods for the foreseeable future.

Please [report issues](https://github.com/lemonacle/belmonts-curse-mods/issues) with the game/build ID, emulator version, device, enabled mods, and exact room or menu sequence. Include screenshots and reproduction steps where possible. For display issues, include the aspect-ratio and resolution settings. Follow the NG+ and relic save precautions in the collection README before changing enabled mods. Redact personal paths from logs and keep private saves, dumps, and keys out of reports.

## Credits and development notes

Relic Toggle used **[Charms Unlimited by kkyleeb21](https://www.nexusmods.com/castlevaniabelmontscurse/mods/37)** as a behavioral reference. The Switch version is an independent implementation with different save handling; it includes no PC plugin code or assets. The collection README explains the differences and credits.

For proposed fixes or build adaptations, see the [contributor notes](docs/CONTRIBUTING.md). Camera inspection reports remain alongside the full-game patches; internal scene names may contain spoilers.

Original patches, scripts, and documentation are MIT licensed; see [LICENSE](LICENSE). Referenced projects retain their own licenses. This repository is not affiliated with the game's developers or publishers.
