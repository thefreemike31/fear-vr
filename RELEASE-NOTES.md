# F.E.A.R. VR v1.5 - Smoother saves and gameplay fixes

- Reduces save/checkpoint stutter by buffering native save writes. The owner
  reported a large improvement at the tested door and ceiling-drop locations.
  Save format, triggers, mission state and existing saves remain compatible.
- Fixes wall-impact particles freezing or lingering during slow motion,
  especially at high refresh rates, and prevents timing markers being rendered.
- Fixes small stone impact marks appearing to float off walls while preserving
  the depth of large craters.
- Corrects remote turret pitch mapping, including the reported inverted aiming
  in left-handed mode. Wrist roll no longer steers pitch or yaw.
- Improves the camera handoff at verified ladder landings to address a reproduced
  snap-back mechanism while retaining body-clearance and collision checks.
- Includes all v1.4.2 height, vent, reload and calibration fixes.

Close the game, extract the complete ZIP, keep setup-files beside Setup, and
choose **Upgrade**. Your saves and calibration are kept; no reset is needed.

The save, particle, small-impact and left-handed turret fixes received owner
headset acceptance. Ladder landing was accepted on internal regression evidence;
affected-player confirmation and physical comfort testing remain open. Separate
Steam headset coverage and a new assembled-ZIP headset run are not claimed.
This does not promise to eliminate every loading hitch or fix every ladder.
See KNOWN-LIMITATIONS.md for remaining limitations. Package version: 1.5.0.
