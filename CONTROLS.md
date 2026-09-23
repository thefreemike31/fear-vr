# Controls and weapon handling

[Main guide](README.md) | [Calibration](CALIBRATION.md) | [Troubleshooting](TROUBLESHOOTING.md)

Open **Controller Layouts.html** from the downloaded ZIP or the installed
**FEAR-VR-Install** folder for the default buttons for your controller profile.
The runtime may report an emulated profile; use the detected profile rather
than relying solely on the controller's product name. Non-Touch profiles remain
experimental.

## Menus and pause

Use the controller pointer and trigger to select menu items. Runtime/system
dashboard buttons are owned by the headset software and may never reach the game.
For SteamVR Touch, press **Right A + Left X together** to pause. The suggested
Index mapping uses **Right A + Left A together**. Press simultaneously; holding
one button first can perform its normal action.

## Handedness and remapping

Open **Options > VR Settings > Controls & Layout**:

- **Weapon Hand** selects your weapon hand.
- **Movement Stick** selects the locomotion stick.
- **Tap to Walk** controls the optional utility-button run/walk toggle.
- **Weapon Button Tap** selects the tap behavior used in Classic Sticky.
- **Button Layout / Remap** reassigns gameplay button roles. Assigning an
  occupied button exchanges the two roles; menu controls remain fixed.

Layouts are saved per reported controller profile and weapon hand. Use
**Restore This Layout** on the remap page, or **Restore Defaults for This Hand**
on the controls page, to undo changes. Check the displayed role labels after
changing handedness; references to left/right defaults may no longer apply.

## Movement and comfort

You start in run mode. With default Touch controls and **Tap to Walk** enabled,
tap the left stick to walk, and tap again to run. **Hold** that utility control
for a medkit; tapping and holding are different actions.

Use **Options > VR Settings > Comfort & Movement** for play position, turning, turn speed, and comfort
options. Smooth turning defaults to 180 degrees/second; lower it or choose snap
turning to suit you. Review vignette and camera-driven-scene options before play.

**Movement Direction** on this page defaults to **Head**. Choose **Controller**
to follow the hand assigned to your movement stick. If that hand loses tracking
or points almost vertically, movement falls back to the head direction.

Jump needs a deliberate upward stick push. After stick-crouching, briefly return
the stick to center before pushing up to jump. A double tap is not required.

**Damage Camera Motion** and **Explosion / Effects Shake** are independent.
Keep explosion shake while disabling damage motion, or turn each off separately.
The effects option also controls authored environmental camera shake.

## Choose a weapon-handling mode

**Grip & Holsters:** reach to a body slot and use Grip to draw a weapon. Weapon-
button taps and the selection wheel are intentionally unavailable. Reload acts
on a held firearm; pressing it while the gun is stowed does nothing. Adjust the
slot locations in calibration if reaching a holster is uncomfortable.

**Classic Sticky:** keeps conventional tap switching and hold-to-open weapon
selection, according to the selected layout. Locomotion is blocked while the
world-anchored weapon selector is open. Release the selector to resume movement.

Under **Immersion & Interaction**, **Visible Holstered Weapons** controls passive
body weapon/belt models. Setting it to No hides their presentation; the body
draw/reload locations still work. Calibration references remain visible.

**Wrist HUD** on the same page hides or shows the wrist display. It defaults
to Yes and is saved independently; immersion presets do not change it.

## Subtitles

For dialogue subtitles, open **Options > VR Settings > Guidance Cards** and
set **Subtitles** to **Yes**. **Subtitle Size** adjusts readability from 75% to
150% (default 100%). This uses the same setting as the game's subtitle option.
Long captions scroll within the panel.

## Reloading and interactions

At the post-loading continue prompt, release and press either trigger; you do
not need to point at the panel. Holding a trigger through loading does not skip
the prompt. Normal readiness delays still apply.

The new **Slow Motion** tutorial card displays your mapped button once the
ability is available and charged. Activate it normally to complete the lesson.
Existing tutorial progress is preserved; the usual Tutorial Cards setting and
reset action apply.

For ASP and G2A2, a tactical magazine change with a round still chambered does
not need another bolt pull. Empty reloads still need racking. Keep the ASP scope
close to your selected eye to acquire the view; it remains usable while tilting.

Support hands now use native weapon grip poses. If an older custom alignment
feels wrong, revisit grip calibration. The shotgun support hand follows the moving
fore-end during pumping. [Weapon Size Calibration](CALIBRATION.md#weapon-size-calibration)
adjusts the size of individual guns separately from grip and sight alignment.

For the shotgun, reach toward the ammo pouch to reveal a shell and use Grip to
pick it up, without pressing Reload. This also works when passive holster models
are hidden. The shell hides when the tube is full. Load at the underside opening.

To put a grenade back, release it near its calibrated holster. The return region
is more forgiving than the grab region; move away from the holster to throw.

After throwing a remote charge, its detonator returns to your dominant hand
while a charge is active. You can still draw a firearm with that hand: the
detonator hides while the firearm is held and returns when you release it.
This also works across repeated grabs and releases.

Nearby eligible pickups take priority over hip holsters. Release Grip and reach
away from the pickup to draw from a body slot deliberately. A weapon can be
carried even with full inventory; storing it still requires the normal exchange.

Manual reload uses weapon-specific actions and contextual cards. Hold the gun,
use the reload/ammo-pouch interactions shown by the current lesson, and complete
any required chambering/racking step. Different weapons do not all reload in
the same way. For a rack or bolt pull, keep the support grip engaged and pull
along the mechanism relative to the gun, not relative to your head. A release
or tracking loss cancels an incomplete pull. Use the reload-mode option if you
prefer button reloads.

If a reload seems stuck, check the held weapon, reserve ammo, chamber/racking
state, and selected reload mode before repeatedly pressing buttons. Recalibrate
the pouch if its position is the problem. See [Troubleshooting](TROUBLESHOOTING.md#weapon-reload-holster-or-interaction-problem).

Empty-hand melee works with either an open hand or a closed fist on enemies
and breakable glass/planks. Keep the striking hand free: holding a prop,
supporting a weapon, reloading, or climbing takes priority. Firing a held gun
does not also add physical weapon-strike damage.

Physical pickups, weapon exchange, melee, and ladders depend on eligible objects
and free hands. A decorative prop is not necessarily grabbable. Clear held
objects/weapons when an interaction requires an empty hand.

## Ladder modes

Under **Comfort & Movement**, choose **Ladder Mode**:

- **Manual** (default): hold Grip at the ladder and move your hand to climb; releasing lets go.
- **Auto (Both Grips)**: engage both grips for automatic climbing.
- **Joystick**: use the assigned movement stick. Approach from below with forward input, or from the upper platform with backward input. Forward climbs up, backward climbs down and neutral holds position. Jump releases the ladder; return the stick to neutral before engaging again.

Joystick entry supports straight, off-center and angled approaches within the
ladder's normal reach and obstruction checks. Top-out suppresses immediate
re-grabs. Not every campaign ladder or reported pushback case has been verified.

## Interaction hints

Tutorial hints can be enabled in VR settings. **New Game** resets tutorial
progress; Continue and loading retain it. Reload cards wait until a reload is
actionable and withdraw when the weapon is full, stowed, or lacks reserve ammo.

## Aiming

**VR Aiming** provides aim-indicator and brightness options. **Dual Pistol Colors**
defaults to On to distinguish the two pistols; Off uses the shared main color.
Use **Weapon Grip Calibration** to change how the gun sits in your hand, and
**Advanced Sight Alignment** only when its aiming direction needs adjustment.
These are different calibrations with separate resets.
