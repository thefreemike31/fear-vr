# F.E.A.R. VR v1.4.2 - Height and vent hotfix

- Preserves your established height reference during automatic recentering after
  level loads and scripted transitions. Moving your head while loading no longer
  silently changes your standing reference. Explicit recenter still works normally.
- Fixes unreliable physical melee against scripted vent covers, including their
  bent stage. Validated hits now reach the vent's native damage script instead of
  being discarded or redirected by its invisible collision surface.
- Includes all v1.4.1 reload and calibration fixes.

Close the game, extract the complete ZIP, keep setup-files beside Setup, and choose
**Upgrade**. Saves, calibration settings and tutorial progress are preserved.
No profile reset or uninstall is required.

The owner confirmed height preservation while moving their head during a level
load, and that the tested vent now breaks promptly with a punch. Exact edition,
all vent layouts and a full hand-pose regression matrix were not enumerated.
Offline package checks are separate from headset acceptance; the assembled ZIP
has not received a new headset run. Existing controller/runtime and translation
limitations remain. See KNOWN-LIMITATIONS.md.
