# Calibration and body fit

## Full-body IK and Fit Visible Body

**New in v1.7:** articulated arms, torso, legs and feet follow your headset and
hands, with procedural walking, crouching, landing and body shadows. No additional
body trackers are required. This is an estimated pose, not measured full-body tracking.
**Visible Body** is under **Options > VR Settings > Immersion & Interaction**.
It defaults to On; a previously saved Off stays Off. Turning it off restores
floating hands. The old experimental rigid-arms option has been retired.

1. Set your seated/standing Play Position and calibrate height first.
2. Open **Options > VR Settings > Calibration & Body Fit > Fit Visible Body**.
   From the main menu this uses the calibration room; during play it uses your level.
3. Use the mirror to adjust **height, reach, shoulder width, forward position and
   fullness**. On Touch: **A** selects the previous field; **B or Y** selects the
   next; flick either stick left/right to adjust, or down to reset the selected
   field. Return the stick toward center between changes. **X** exits.
4. Check relaxed arms, full reach, looking down and crouching. Changes save to
   your profile. The fitter temporarily selects Unarmed and restores your prior
   weapon/ammo selection on exit.
5. Use **Reset Visible Body Fit** for the body fit alone. Existing hand, holster,
   weapon-grip and sight tools remain separate. Avoid Reset All Calibration unless
   you intend to clear the rest of your fitting too.

**Updated in v1.7.2:** Body Height adjusts vertical upper-body fit while keeping
the feet grounded and the legs moving. It no longer rescales boots, legs or arm
reach; use the separate Reach and Fullness settings for those aspects of fit.
New profiles and **Reset Visible Body Fit** start Body Height at **115%**.
Upgrading preserves your saved percentage; reset only if you want the new default.
The mirror now displays the head. Resting arms, support cuffs and hand shadows
are improved, though a minor occasional hip/arm snap remains under investigation.
Feet/elbows are inferred and can need personal fitting. Existing profiles and
calibration are preserved during upgrade; no blanket reset is required.

## Language and shortcut settings in v1.6

Language import/reset preserves VR calibration. The launcher language selector
changes launcher text; game text/voices use the separate [import/reset tutorial](INSTALLATION.md#import-game-text-and-voices).
Mission **Y+B**, quick-save **Y+A (2 seconds)** and quick-load **X+B (2 seconds)**
are physical combinations, unchanged by handedness or remapping. Save/load is
disabled during calibration; see [shortcut behavior](CONTROLS.md#mission-screen-quick-save-and-quick-load).

## v1.4.2 height preservation

Automatic recentering during level loads and scripted transitions keeps the
established vertical reference. Explicit recenter remains available. The fix
does not reset or change saved calibration values.

[Main guide](README.md) · [Controls](CONTROLS.md) · [Troubleshooting](TROUBLESHOOTING.md)

Open **Options > VR Settings > Calibration & Body Fit**. From the main menu,
calibration opens the included room. During a campaign it uses your current
level. Calibration settings belong to your profile; use the same profile when
returning to the game. The calibration room does not replace campaign progress
saves or Continue.

## Suggested order

1. Set your intended seated/standing **Play Position** under **Comfort & Movement**.
   Confirm that the headset runtime's floor and tracking look correct.
2. Use **Calibrate Standing Height** when applicable. Follow the displayed pose
   and confirmation instructions; do not crouch or stretch upward during capture.
3. Open **Fit Hands to Controllers** and align the visible hand/reference with
   the physical controller you are holding. Keep a normal, comfortable grip.
4. Use **Adjust Holsters & Pouches** to put draws and reload locations within
   comfortable reach. Use the displayed body/mirror references and test both sides.
5. Adjust **Weapon Grip Calibration** if a particular gun sits incorrectly.
6. Use **Advanced Sight Alignment** only after the grip is comfortable and you
   have identified an aiming offset. Follow that page's target/capture instructions.

Start with one adjustment at a time and follow the in-headset prompts for
capture, confirmation, and exit; they reflect your selected controller layout.
You do not need every advanced calibration to begin playing.

## What each adjustment changes

| Adjustment | Purpose |
| --- | --- |
| Height | Player height fit for the selected play setup |
| Holsters & pouches | Physical draw and reload locations |
| Fit Hands to Controllers | Hand/controller reference fit, also used by held hands |
| Weapon Grip Calibration | Weapon placement and orientation in the hand |
| Weapon Size Calibration | Per-weapon visual size, from 50% to 150% |
| Advanced Sight Alignment | Aim direction; it does not move the weapon model |

Changing controller hand fitting can affect how an older per-weapon grip
alignment feels. Revisit the affected grip instead of repeatedly changing
unrelated sight settings. Passive holster visibility can be off during play;
calibration still shows its references.

## Weapon size calibration

Open **Weapon Size Calibration** under **Calibration & Body Fit**. It works in
the calibration room from the main menu, or in your current campaign level.
Use **A** for the previous weapon, **B/Y** for the next, and **X** to exit.
Wait for a weapon switch to finish before adjusting it.

Flick either stick left/right for 5% steps between **50% and 150%**, or down to
reset the selected weapon to **100%**. Center the stick between steps. The held
weapon changes size immediately and the profile saves each weapon separately;
both copies of a dual weapon share that weapon's setting. Stick locomotion,
turning and jumping are suppressed in this calibration mode; physical tracking
still works. Exiting calibration clears its temporary instructions and preserves
your normal tutorial progress. v1.4.1 also keeps manual-reload magazines and
reserve visuals aligned with resized weapons; upgrade v1.4.0 if magazines vanish.

100% uses the established weapon size. Held hands keep their existing scaling
with the gun. This does not change ammunition, damage or inventory. Grip and
sight alignment remain separate adjustments. Their individual resets leave
weapon size intact; **Reset All Calibration** also resets all weapon sizes.

The new native support-hand poses may change how older custom grip alignments
feel. Revisit the affected weapon's grip if necessary.

## Undo a bad adjustment

The same menu includes **Reset Height**, **Reset Holsters & Pouches**,
**Reset Grip Alignments**, **Reset Sight Alignments**, and **Reset All Calibration**.
Prefer the individual reset for the feature you changed. **Reset All Calibration**
discards your calibration adjustments; it is not a troubleshooting requirement
for unrelated startup or performance problems.

For view distortion, use **Headset Display > Restore Display Defaults** or
restore **Centered (Recommended)** projection and **100% View Width**. This is
a display adjustment, not weapon calibration. Render-resolution changes apply
on the next launch.

If the room does not load, use Setup to repair/upgrade from the complete official
package. Do not fetch loose room files or a developer launcher from an old beta.
For persistent problems, report the calibration page, headset/controller,
play position, and exact adjustment in [GitHub Issues](https://github.com/thefreemike31/fear-vr/issues).

## Hand fit while holding objects

v1.7.5 keeps saved hand fitting active for held props and the manual-reload
utility hand. Supported pickups and belt magazines seat against visible hand
contact. Existing calibration is preserved; no reset is needed.
