# Known limitations

## v1.7.6 launcher and holster scope

The inherited SteamVR win64-to-win32 selection repair passed unit tests and
diagnostic checks of both edition launchers. Confirmation from affected headset
users is still pending. It does not claim complete Steam Frame compatibility or
resolution of unrelated SteamVR launch problems. Valid custom 32-bit overrides
remain selected; other invalid explicit overrides fail with a repair message.
Registry/global runtime settings are unchanged.

The remembered-holster behavior received overall owner headset acceptance.
Separate editions, every weapon/handedness combination and every save/load path
were not individually enumerated. Save compatibility has source/fixture coverage;
old or invalid layout data falls back to the default. The existing heavy/back-slot
rule can still move the involved weapons. No assembled-ZIP headset run is claimed.

## v1.7.5 interactions, tutorials and mirror scope

The owner accepted visible-contact grabbing, door kicks, reload switching,
tutorial persistence/lifetime and the single mirror with Alt-Tab and window
shutdown. Separate Steam headset coverage, every object/door/weapon, every mirror
mode, a new complete OBS recording matrix and an assembled-ZIP headset run are
not claimed. Supported pickup geometry has improved contact; unsupported models
and finger closure can still differ from the visible surface. Door kicks retain
locks and scripts.

Fill crops the right eye to 16:9; Native preserves the complete eye and may leave
side bars on a widescreen canvas. Off is headset-only. A brief bootstrap window
may appear before VR is ready; mirror failure can restore the original window
as a fallback. The blank-window-on-exit issue is fixed. A previously observed
native game-shutdown crash remains a separate, unresolved follow-up.
See the [current OBS guide](INSTALLATION.md#recording-with-obs).

## v1.7.2 ladder, body and flashlight scope

The reported tall ladder's actual top-platform exit, grounded body-height fit,
mirror head, arm/support improvements, hand shadows and either-hand flashlight
received owner headset acceptance. No every-ladder, every-weapon, separate Steam
or newly assembled-ZIP headset acceptance is claimed. A minor occasional hip/arm
snap remains open. The grenade hand-sample timing correction is included;
the slow-motion feel investigation closed without a demonstrated extra drag fix.

## Retained v1.7.1 ladder scope

The reproduced water-to-ladder climb and standing platform exit were owner-headset
accepted after the body-update regression. Every ladder mode, campaign ladder,
separate Steam headset run and the assembled public ZIP are not claimed tested.
The body remains visible in water. Earlier untested red-ladder cases are separate.

The old separate OBS checkbox and window/borderless capture workflow were
replaced by the single-mirror choices in v1.7.5. Historical recordings from that
older workflow do not establish a complete new-mode or Steam recording matrix.

## v1.7 body and interaction coverage

Full body/calibration, kick/slide, selected weapon weight, room-scale recovery and
campaign door/padlock/glass changes received owner or affected-player acceptance.
Separate Steam headset coverage of these combined changes and a new assembled-ZIP
headset run are not claimed. The calibration mirror head is restored in v1.7.2. Body pose is
inferred from headset/controllers, not full-body trackers. Perfect frame pacing
and every weapon's weight feel are not established; Cannon feel remains untested.
Auto Pickup and red-ladder follow-ups ship with offline coverage and no focused
headset acceptance. Existing slow Steam loading and Quit cleanup issues remain.

## v1.6 language import and shortcut coverage

v1.6.1 removes the Spanish-only import restriction. Original language DVD/ISOs
with matching-language 1.08 patches are intended to work across all languages
in theory; **only Spanish has official real-media/gameplay testing**. Other
languages remain unverified. The native reader requires the original supported
InstallShield cabinet layout; split, incomplete or different-format releases may
be refused. The user must match disc and patch language. Synthetic metadata
regressions do not establish real-language or native-speaker acceptance.
Steam Spanish VR, original retail startup and full-campaign playback are not
established. See the [tutorial](INSTALLATION.md#import-game-text-and-voices).
No game data is redistributed; existing Spanish recovery records remain valid.
Mission open/close, quick save and quick load were owner-accepted on GOG; separate
Steam headset coverage and non-Touch physical combinations remain unclaimed.

## v1.5 validation scope

The owner accepted save-stutter improvement at two GOG hotspots, corrected slow-
motion particles, small stone-impact appearance and left-handed turret aiming.
Ladder landing was accepted on internal regression evidence; synthetic collision
tests do not establish every campaign landing or physical comfort. Separate Steam
headset coverage, a new right-handed turret run and an assembled-ZIP headset run
are not claimed. Save buffering does not eliminate every possible loading hitch.

## v1.4.2 validation scope

The owner accepted the moving-head level-load height test and prompt vent breaking.
Full per-edition, every-vent, both-hand/pose and scripted-return matrices remain
unreported. Package checks do not substitute for those headset tests.

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

- The desktop and OBS use the same mirror. Check a short recording before
  relying on a minimized configuration; the headset and recording need separate
  checks on your own setup.

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
