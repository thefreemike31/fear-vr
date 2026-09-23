# Known limitations

[Main guide](README.md) · [Troubleshooting](TROUBLESHOOTING.md)

- This release targets verified GOG and original Steam base-game single-player
  campaigns. Other executable variants, expansions, multiplayer and Linux/Proton
  are outside its supported scope.
- Steam level loading can take several minutes. GOG remains recommended.
  Other mod loaders and hook suites are not validated together with this mod.
- Steam memory preparation enables up to 4 GB of address space on 64-bit Windows;
  it does not eliminate memory pressure or prove every out-of-memory report fixed.
  Point of Entry passed owner tests with Virtual Desktop and SteamVR. An existing
  native cleanup crash after selecting Quit remains unresolved.
- Language preservation and Cyrillic menu-font fallback are experimental.
  The automatic correction was owner-tested with Russian menus on GOG; other
  languages, Steam automatic-font coverage, non-menu fonts and full campaigns
  are not comprehensively verified. VR-specific text may remain English.
- Steam's included input fix filters legacy gamepad/joystick enumeration;
  keyboard, mouse and OpenXR controllers remain available. This also applies
  to flat launches from that installation while the fix is enabled. See
  [Troubleshooting](TROUBLESHOOTING.md#steam-input-fix) for the optional off switch.
- Some small props still sit slightly away from the hand. Ladder completion
  improved in repeated owner testing; broader affected-player coverage remains.
- Compact underwater collision is included, but the reported Blindside tunnel
  has not yet been reproduced and verified in a headset.
- Quest 3 with Touch controllers is the physical validation baseline. Other
  headsets, controller profiles, and wide/canted-headset display adjustments
  remain experimental. A listed mapping is not a guarantee of hardware coverage.
- Meta Quest Link and Air Link are unsupported, even through SteamVR.
- Optional **Flashlight Shadows** is experimental and off by default. Detached
  hands do not cast those flashlight shadows. Other optional visual/body
  features may have imperfect alignment or scene-dependent artifacts.
- The game remains a 32-bit application. High per-eye resolutions can create
  memory/GPU pressure even on a PC with plentiful system RAM. Start with the
  supported display defaults and adjust one setting at a time.
- Capture safeguards improve handling of a delayed GPU, but recurring stalls
  reported on some systems have not been conclusively diagnosed or universally
  resolved. Driver calls, runtime waits, loading, and streaming can still stall.
- A runtime shutdown or lost OpenXR session may require quitting and relaunching
  the game after restoring the headset connection.
- Existing save/profile data and native game behavior still matter. Keep save
  backups and report specific levels/actions for repeatable campaign problems.
- Releases are unsigned. Local download verification is not a guarantee that
  every antivirus or reputation service will accept the same archive.

- Windowed mirror controls were tested on GOG at 720p with VirtualDesktopXR;
  Steam memory startup was tested with Virtual Desktop and SteamVR. These tests
  do not establish every display mode or OBS/minimized capture behavior.
  Do not assume recording continues while the mirror is minimized.
- Small held props can still sit farther from the hand than ideal.

Read the latest release notes and open issues before assuming an old workaround
still applies. Development tools and the local Level Select menu are not shipped.

## v1.4.1 hotfix scope

The resized-magazine, shotgun shell ownership, lingering calibration-card and
reload-lesson fixes are owner accepted. Automated checks cover the scale range
and production state transitions; headset coverage was not enumerated for every
weapon, size, controller or edition. Upgrade v1.4.0 rather than resetting profiles.

## v1.4 additions

Launcher translations have offline layout/catalog checks and owner UI review,
but native-speaker review and automatic selection on non-English Windows remain
open to feedback. They do not change the installed game's language; logs and the
Controls guide remain English.

Joystick climbing and the latest entry correction are owner accepted, but all
campaign ladders and previously reported top-out pushback cases are not verified.
Cinema aspect correction is owner accepted; confirmation of the affected player's
exact scene/resolution is still pending. Older custom weapon grip alignments may
need recalibration with the new native support-hand poses.
