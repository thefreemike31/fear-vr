# F.E.A.R. VR v1.4.1 — Reload and calibration hotfix

**Everyone using v1.4.0 should update**, especially if you have changed weapon sizes.

- Fixes magazines disappearing or moving away during manual reloads on resized
  pistols and dual pistols. Reserve magazines now also follow live size changes
  correctly, including pistol and SMG belt visuals.
- Fixes the shotgun support grip interrupting shell loading, particularly on
  smaller weapons. Shell handling keeps control until you release Grip; a fresh
  fore-end grab still lets you pump and finish a partial reload.
- Clears temporary calibration instructions when leaving calibration, so they
  cannot linger in normal tutorial cards. Existing lesson progress is preserved.
- Shows magazine/cell and charging lessons at the correct reload stage.
  G2A2/ASP tactical reloads finish on insertion without an unnecessary bolt prompt;
  Type-7 uses its existing cell-and-hammer sequence.

Thanks to Jarilo for finding the bug so quickly and helping with the fix!

## Updating

Close the game, extract **fear-vr-v1.4.1.zip** into a fresh folder, keep
**setup-files** beside **F.E.A.R. VR Setup.exe**, and choose **Upgrade**.
No uninstall, calibration reset or tutorial reset is needed; saves and profiles
are preserved. All v1.4 features remain included for GOG and Steam.

Until you update, setting the affected weapon back to **100%** is a workaround
for the reported scaled-magazine problem; it does not fix the other issues above.

## Validation and limits

The owner confirmed these fixes in the headset. Exact per-edition and all-weapon
headset coverage was not enumerated. Production-code regression checks cover
scale transforms, shell/card ownership and staged lessons; final installer and
exact-ZIP upgrade checks are separate from headset acceptance.
The launcher and other runtime components are unchanged from v1.4.0.
The existing Quit cleanup crash and broader language/hardware limitations remain.
