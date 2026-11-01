# F.E.A.R. VR v1.8.2 — physical weapon fixes and bHaptics polish

## Physical weapon fixes

- Held pistols no longer disappear when collecting ammo or selecting another
  weapon. Stow or release a held physical gun before switching.
- Chest ammo intake works while the matching owned gun is held, including the
  SMG. Full reserves preserve the pickup; partial intake leaves unused rounds.
- Pair a found pistol with your holstered pistol. With two originals already
  stored, borrow a third and draw either original while the unused one stays
  holstered. You can swap which original you use without losing the third gun.
- Individual magazines survive stowing, switching and save/load. Rapid drops,
  delayed replies, failed pickups and ammo-cap transitions preserve ownership
  and ammunition. Release a borrowed pistol before reloading or switching.

## bHaptics improvements

- Helicopter feedback, corrected effect maps and improved Player position
  compatibility.
- A gentle heartbeat starts at **40 displayed health**, grows stronger as health
  falls and stops above 40. Health upgrades do not change the threshold.
- Experimental Tactosy hand/foot and TactGlove DK2/DK3 effects are included:
  **software-tested, physically untested, expected to work**. Hands/gloves share
  Sleeve controls and feet share Vest controls. Physical feel/orientation remains
  unverified; no finger tracking, new footstep/grabbing feedback or recorder
  overlay display of these extra outputs is added.

The weapon fixes and heartbeat/helicopter feel have owner headset acceptance;
this is not an exhaustive edition, scene or wearable-device matrix. Physical
Weapons remains a prototype. Existing loading/performance/Quit limitations remain.

## Update

Download **fear-vr-v1.8.2.zip** and its checksum from Assets, extract the complete
ZIP, keep **setup-files** beside Setup, and choose **Setup > Upgrade**. Saves,
calibration and wearable strengths are preserved. v1.8.1 remains available as
rollback. GitHub's automatic Source code archives are not the mod.

See [installation](INSTALLATION.md), [controls](CONTROLS.md),
[wearable setup](INSTALLATION.md#bhaptics-wearables) and
[known limitations](KNOWN-LIMITATIONS.md).

## Included v1.8.1 compatibility fixes


- Adds software support for TactSuit X40, X16, Air and legacy Tactot vests, plus
  legacy Tactosy arm and Tactal head devices alongside the existing kit.
- Fixes connected models being excluded by the Pro-only vest filter. An old,
  disconnected pairing no longer hides a connected replacement.
- Adapts effects to the supported command layouts and improves connection and
  device diagnostics. Existing Pro, TactSleeve and TactVisor effects are retained.
- These compatibility fixes from v1.8.1 remain included.

The additional devices passed software and real SDK packet checks, but were
not physically tested by the author. See [wearable setup](INSTALLATION.md#bhaptics-wearables).

## Included v1.8.0 features — new wrist HUD, weapon handling and bHaptics

## New features

- **Redesigned wrist HUD.** A larger, clearer display sits closer to your hand and uses F.E.A.R.'s own artwork and digits. Ammo is prominent, with health, armor, grenade and medkit counts together. The new slow-motion meter shows your remaining charge, when it is ready to use, and when it is actively being consumed.
- **Sticky & Holsters handling mode.** Tap Grip at a body holster to draw, then relax your grip while carrying the gun. Tap that hand's Grip again to return it from any position. Each dual pistol has its own toggle; the free hand still handles support grips, reloads, ladders, grenades and props. Classic Sticky and Grip & Holsters remain available.
- **Physical Weapons (Prototype).** This separate optional mode supports all nine firearms: hold Grip to retain a gun, release at a compatible free holster to store, or release elsewhere to drop/throw. Catch and use supported guns in either hand. With three weapons stored, you can temporarily borrow a world/enemy gun without replacing one. Mixed firearm dual wielding remains unsupported.
- **Optional bHaptics wearables.** Feel directional hits, gun recoil, melee impacts and nearby explosions through TactSuit Pro, TactSleeve and TactVisor. Low-health heartbeat, healing/armor cues and slow-motion feedback add to the experience, with independent device and effect strengths in bHaptics settings.
- **More control over feel.** Remap Jump and Crouch, set Controller Vibration from 0–200%, and adjust individual Weapon Weight & Lag settings from 0–200%, with separate resets.

## Handling, reloads and body improvements

- **More flexible holsters.** Either pistol can crossdraw or return to either free hip socket. Long guns can use compatible empty shoulder/back sockets, with occupancy and holster feedback kept consistent.
- **Pistol reloads and discarding.** An empty single pistol now needs a slide pull after the magazine; dual pistols retain hip reloads. In nonphysical modes, hold Reload for 1.25 seconds to discard one pistol. Physical mode uses Grip release. Tutorials explain the selected mode's gestures.
- **Body fit and sleeves.** Improved physical body fitting, arm/leg extension, sleeve seating and body/holster alignment. More natural near-face arm placement and wrist bending make checking your wrist HUD more comfortable visually.
- **Weapon presentation and audio.** Refined either-hand firing/support/reload poses, dropped-weapon presentation, and shotgun shell/pump sounds. Native headset projection is retained; optional View Width remains an experimental framing control.

## Important fixes

- **Doors at close range:** touching the same door with a second hand no longer immediately reverses the first hand's opening action. A stopped door can still be retried by withdrawing and pushing again.
- **Close-contact vents:** corrected a grounding-state rejection that could make the Bishop vent ignore punches when standing right next to it. Native locks, collision and scripted interactions remain authoritative.
- **Jump/body clipping:** body, hands and holsters now follow the same collision-resolved eye height, correcting the chest rising into view during the reported jump/railing case.
- **Sleeve twisting:** corrected the unnecessary sleeve unwind during small turns with your hands held near your chest or hips.
- **Slow-motion ragdolls:** improved interpolation and turn handling to reduce snapping during rotating-body motion; this is not a guarantee that every spin or hitch is eliminated.
- **Physical-weapon edge cases:** corrected first-pickup firing, duplicate/borrowed-gun ammunition accounting and dropped-weapon save/presentation behavior. Excess ammunition stays in its source magazine rather than disappearing at the cap.
- **Cleaner normal play and support:** diagnostic timing/trace collection is disabled during normal play, launcher errors identify the actual log-folder action, and player guides have been consolidated around the current setup and controls.

## Updating

Download **fear-vr-v1.8.2.zip** from Assets below, verify its `.sha256`, extract the complete ZIP and use **Setup > Upgrade**. Keep **setup-files** beside Setup. Saves and calibration are preserved; no blanket profile reset is required. GitHub's automatic Source code downloads are not the mod.

Improved Sights by **Eskess** remain optional and off by default; recalibrate sight alignment after switching.

See [installation](INSTALLATION.md), [controls](CONTROLS.md), and [known limitations](KNOWN-LIMITATIONS.md). Residual hitches, slow Steam loading and the pre-existing late Quit cleanup fault remain open; the latter can be recorded by Windows after the game window closes normally. Physical Weapons remains a prototype, and not every headset, weapon/scene combination or bHaptics device model has been tested.
