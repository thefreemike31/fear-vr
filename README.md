# F.E.A.R. VR Mod by TheFreeMike

**v1.8.0 · GOG and Steam · Free, unofficial PC VR mod**

Play the original F.E.A.R. campaign with tracked hands, physical weapon handling,
manual reloads, body calibration and configurable comfort options. You need a
legitimate supported copy of the game and a Windows PC capable of PC VR. The
game is not included; this is not a standalone Quest app.

[Download v1.8.0](https://github.com/thefreemike31/fear-vr/releases/tag/v1.8.0) ·
[Installation](INSTALLATION.md) · [Controls](CONTROLS.md) ·
[Calibration](CALIBRATION.md) · [Troubleshooting](TROUBLESHOOTING.md)

<img src="assets/alma.png" alt="Alma, F.E.A.R. VR artwork" width="240">

## Start here

1. Confirm the unmodified GOG or Steam base game works on your PC.
2. From the release's **Assets** list, download `fear-vr-v1.8.0.zip` and its
   `.sha256` file. GitHub's automatic **Source code** downloads are not the mod.
3. Verify and extract the complete ZIP. Keep **setup-files** beside
   **F.E.A.R. VR Setup.exe**.
4. Close F.E.A.R., open Setup, select the base game's folder, then install or
   upgrade. Setup keeps saves and backs up replaced files.
5. Connect your headset and controllers through one supported route below.
6. Run **F.E.A.R. VR.exe** in the installed game folder, choose your desktop display mode, and select **Play in VR**.

Follow the [step-by-step installation guide](INSTALLATION.md) for runtime setup,
checksum verification, shortcuts, upgrading, uninstalling, and recovery.

## Supported setup

| Requirement | What to use |
| --- | --- |
| Game | Verified GOG or original Steam base game; Setup checks the exact executable |
| PC | Windows 10/11; this is a PC VR mod, not a standalone headset app |
| Quest connection | Virtual Desktop + VDXR, or Steam Link + SteamVR with Win32 OpenXR support |
| Other PC VR headsets | SteamVR with Win32 OpenXR support; hardware coverage remains experimental |
| Physically validated hardware | Quest 3 with Touch controllers |

Meta Quest Link and Air Link are unsupported, including through SteamVR.
Other retail executable variants, Extraction Point, Perseus Mandate, multiplayer, and
Linux/Proton are outside this release's supported scope. A controller mapping
does not mean that hardware has been physically tested.

## What is new in 1.8

- **Redesigned wrist HUD:** larger native-art display with clearer ammo, health,
  armor, medkit/grenade counts and a slow-motion charge/readiness meter.
- **Sticky & Holsters:** tap Grip at a holster to draw, relax your hand while
  carrying, and tap Grip again to return the gun. Each dual pistol toggles separately.
- **Physical Weapons (Prototype):** optional grip-held firearms, release to
  holster/drop/throw, supported catches and either-hand use. A temporary borrowed
  gun can be used with three weapons stored; mixed firearm dual wielding is not
  supported. [Handling modes](CONTROLS.md#choose-a-weapon-handling-mode).
- **bHaptics:** optional TactSuit Pro, TactSleeve and TactVisor feedback through
  bHaptics Player. Device/effect strengths are independent; no developer account
  or API key is required. [Wearable setup](INSTALLATION.md#bhaptics-wearables).
- **Controls and interactions:** Jump/Crouch remaps, controller-vibration strength,
  per-weapon weight/lag, reload/body/holster refinements and more reliable
  close-range door touches. Fixes also cover close-contact vents, jump/body
  clipping, sleeve twisting and physical-weapon ammo/save edge cases; slow-motion
  ragdoll presentation is improved. Normal-play diagnostics are quieter.

Saves and calibration are preserved; no blanket reset is required. Earlier
features remain included. Improved Sights by **Eskess (`.eskess`)** are optional
and off by default; recalibrate after switching sight versions.
[Release notes](RELEASE-NOTES.md) · [Known limitations](KNOWN-LIMITATIONS.md).

## Player guides

| Guide | Find out how to… |
| --- | --- |
| [Installation](INSTALLATION.md) | Install, connect the runtime, launch, update, remove, or recover the mod |
| [Controls](CONTROLS.md) | Navigate menus, choose weapon handling, reload, remap, and use comfort settings |
| [Calibration](CALIBRATION.md) | Set height, fit hands, move holsters, and reset individual adjustments |
| [Troubleshooting](TROUBLESHOOTING.md) | Work through startup, graphics, controllers, performance, audio, and save issues |
| [Known limitations](KNOWN-LIMITATIONS.md) | Check hardware coverage and experimental features |
| [Release notes](RELEASE-NOTES.md) | See the latest fixes and update instructions |
| [Security and privacy](SECURITY.md) | Understand installation, unsigned files, and diagnostic privacy |
| [Third-party notices](THIRD-PARTY-NOTICES.md) | Read component notices and licenses |

The ZIP also includes **Controller Layouts.html**, with diagrams/tables for the
supported mapping profiles. Download and open it in your browser; GitHub may
show its HTML source instead of rendering it. These guides are also installed
under **FEAR-VR-Install**, so you can read them without joining Discord.

## Calibration & settings video guide

[![Watch TheFreeMike’s full F.E.A.R. VR calibration and settings guide](https://i.ytimg.com/vi/BUJLpW-l5yI/hqdefault.jpg)](https://www.youtube.com/watch?v=BUJLpW-l5yI)

**[Watch the full calibration & settings guide by TheFreeMike](https://www.youtube.com/watch?v=BUJLpW-l5yI)** — an in-depth, roughly 40-minute walkthrough. Use the YouTube chapters to jump to the setting or calibration you need.

Keep the written [calibration guide](CALIBRATION.md) and [controls guide](CONTROLS.md) handy alongside the video. You can also [watch it on the website](https://thefreemike.com/fear-vr/#settings-guide).

## Watch the F.E.A.R. VR trailer

[![Watch the F.E.A.R. VR trailer by WunderbarVR](https://i.ytimg.com/vi/pRqdUyzCBeI/hqdefault.jpg)](https://www.youtube.com/watch?v=pRqdUyzCBeI)

Trailer created by **[WunderbarVR](https://www.youtube.com/@WunderbarVR)**.
Click the image to watch on the creator’s YouTube channel, or watch the embedded
trailer on the [F.E.A.R. VR website](https://thefreemike.com/fear-vr/#trailer).

## Make sure you have the right mod

This is **TheFreeMike's F.E.A.R. VR**, distributed by **thefreemike31**.
The separate [DR-89/fear-vr project](https://github.com/DR-89/fear-vr) has its own
releases and instructions. TheFreeMike does not maintain or provide support
for that project's builds or other F.E.A.R. VR mods.

For support here, use a release downloaded from
[thefreemike31/fear-vr](https://github.com/thefreemike31/fear-vr/releases) and
include its version and download URL in your report. Do not combine installers
or files from different VR mods.

## Help and support

Start with [Troubleshooting](TROUBLESHOOTING.md). If the problem remains, use
[GitHub Issues](https://github.com/thefreemike31/fear-vr/issues) and the report
template at the end of that guide. Search existing issues first. Review logs
before posting; keep personal paths and crash dumps private.

[Join the Discord community](https://discord.gg/NtAnbK6z9B) ·
[Support TheFreeMike on Ko-fi](https://ko-fi.com/thefreemike)

The mod is free. Donations are optional and do not purchase support, access,
or a response deadline.

## Credits and AI transparency

**F.E.A.R. VR was built through a collaboration between TheFreeMike and Codex,
OpenAI's AI coding assistant.** AI was a substantial part of the engineering
process, and we want to be transparent about that contribution.

- **TheFreeMike (Mike):** project direction, gameplay and comfort decisions,
  hands-on headset testing, feedback that guided repeated revisions, and
  community and release stewardship.
- **Codex (OpenAI):** substantial engineering assistance across code
  implementation, debugging, code review, automated checks, build and installer
  tooling, release packaging, and player documentation, working iteratively
  with Mike's direction and test results.
- **Private-beta testers:** hardware reports, reproduction steps, and gameplay
  feedback that helped uncover issues beyond the development setup.

The collaboration combined AI-assisted engineering with human judgment and
real headset testing. Mike maintains the project and makes the final release
decisions; AI-generated changes still need review and validation. This is an
independent community project, not an OpenAI product or endorsement.

## About this repository

This is the **distribution and documentation repository**. It contains player
guides and release downloads; the mod's development source is not published.
It is not an open-source release. Third-party components retain their own
licenses. F.E.A.R. belongs to its respective rights holders; this unofficial
mod is not endorsed by them and includes no standalone copy of the game.

Earlier releases and private-beta milestones are documented separately in
[development history](https://github.com/thefreemike31/fear-vr/blob/main/HISTORY.md).
Use the current guides above for installation and play.
