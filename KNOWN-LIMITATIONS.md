# Known limitations

Current scope for **v1.8.0**. [Release notes](RELEASE-NOTES.md) cover what changed;
[development history](https://github.com/thefreemike31/fear-vr/blob/main/HISTORY.md)
holds earlier milestones. These limits apply even when installation checks pass.

## Game, headset and runtime support

- Supported game copies are the verified GOG and original Steam base-game
  single-player campaigns on Windows 10/11. Other executable variants,
  expansions, multiplayer and Linux/Proton are outside the supported scope.
- **Quest 3 with Touch controllers** is the physical validation baseline.
  Other headsets, controller profiles and wide/canted displays are experimental.
  A listed mapping is not evidence that the hardware has been tested.
- Use Virtual Desktop + VDXR or Steam Link/SteamVR with Win32 OpenXR support.
  Meta Quest Link and Air Link are unsupported, including through SteamVR.
- Other mod loaders, graphics/audio replacements and hook suites are not
  validated together with this release. A lost OpenXR session can require a
  game restart after restoring the headset connection.

## Performance, loading and exit

- Steam level loads can take several minutes; GOG remains recommended.
- The game is 32-bit. Steam memory preparation enables up to 4 GB of address
  space on 64-bit Windows; it does not eliminate memory pressure. High per-eye
  resolution can still exhaust resources on a PC with plenty of system RAM.
- Residual hitches and recurring stalls are not universally resolved. Runtime,
  driver, loading and streaming waits can still stall; report timing and settings.
- A pre-existing native cleanup crash after Quit remains unresolved. Windows
  may record it after the visible window closes normally. It is distinct from
  an in-game crash or a stuck leftover window.
- Desktop/OBS capture needs a short recording check on your own setup, including
  audio. Headset rendering and recording are separate checks.

## Weapons, body and interaction

- **Physical Weapons (Prototype)** is optional. Its nine firearm types use
  hold-Grip and release-to-store/drop rules. Mixed firearm dual wielding is not
  supported. See [handling modes](CONTROLS.md#choose-a-weapon-handling-mode).
- Body pose is inferred from the headset/controllers, not full-body trackers.
  Feet/elbows and holster placement may need personal fitting; occasional
  hip/arm snaps, small-prop offsets and scene-dependent clipping can remain.
- Not every ladder endpoint, vent, door, weapon/hand combination or campaign
  transition has been individually verified. Native locks/scripts still apply.
  The reported Blindside underwater tunnel has not been reproduced and verified
  in a headset. Keep save backups and report the exact location/action.
- Improved Sights by Eskess cover seven weapon types and are off by default.
  Sight alignment is shared between Stock/Improved; recalibrate after switching.
- Optional Flashlight Shadows is experimental and off by default. Detached
  hands do not cast those shadows. Optional View Width is experimental framing;
  native headset projection is retained. Start at 100% View Width.

## Wearables, languages and other limits

- bHaptics support covers **TactSuit Pro, TactSleeve and TactVisor**; a partial
  kit works. Other device models are not claimed supported. Environmental
  feedback follows specific supported events, not every sound, video or scare.
- Language import needs original language media and a matching official 1.08
  patch. Only Spanish import has official real-media/GOG VR testing; other
  languages and Steam Spanish VR remain unverified. Russian menu-font fallback
  was tested on GOG; non-menu fonts and full campaigns remain experimental.
- An existing Polish archive can be mounted, but Polish fonts/subtitles still
  need in-game confirmation. No translation data or original game archives ship.
  Launcher language is separate; VR-specific text, logs and guides may stay English.
- Steam’s input fix also filters legacy gamepads in flat launches while enabled.
  Keyboard, mouse and OpenXR remain available; see the
  [optional off switch](TROUBLESHOOTING.md#steam-input-fix).
- Files are unsigned. SHA-256 confirms identity, not universal antivirus approval.
  Developer Level Select, SDK tools, symbols and personal credentials do not ship.

## Validation scope

Owner testing accepted key-free bHaptics feedback and the close-door fix on the
Steam development installation, alongside earlier accepted gameplay work.
Automated checks cover the exact release ZIP, original GOG/Steam startup files,
fresh installs, supported upgrade paths, recovery and launcher preflight.
Those checks do not constitute a new headset run of the assembled shipping ZIP,
nor proof for every scene, device, controller or disconnected-network setup.

[Main guide](README.md) · [Troubleshooting](TROUBLESHOOTING.md)
