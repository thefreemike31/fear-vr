# F.E.A.R. VR v1.6.1 - Language import hotfix

- **Removes the accidental Spanish-only import restriction.** Use your original
  language DVD/ISO and the official 1.08 patch in the same language.
- **All language editions are intended to work in theory; only Spanish has been
  officially tested.** Other real-language media and gameplay remain unverified.
- Reads archive locations and checksums from the supplied media, instead of
  using fixed Spanish offsets and hashes. Damaged or incomplete data is refused.
- **Reset language still restores existing v1.6 Spanish backups.** Keep the
  FEAR-VR-Language folder; saves, calibration and game executables are preserved.
- Import/reset prompts and the tutorial now explain the general language workflow.

Close the game, extract the full ZIP and choose **Setup > Upgrade**. Keep
setup-files beside Setup. No calibration reset is needed. Mount one language ISO,
then select its matching 1.08 updater when Import language asks for it. The updater
is read, never executed. Reset before importing a different language.

[Import/reset tutorial](INSTALLATION.md#import-game-text-and-voices).
The reader requires the original supported InstallShield cabinet layout; split
or different-format media may be refused. The launcher does not identify the
spoken language, so make sure the ISO and patch match. Gameplay modules and
v1.6 controller shortcuts are unchanged. No new headset run is claimed.
