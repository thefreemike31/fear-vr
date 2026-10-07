# F.E.A.R. VR v1.7.5 - Better interactions, tutorials and capture

- **Simpler launcher and OBS setup:** one desktop mirror with three choices:
  **16:9 - fill screen**, **Native - full view**, or **Off - headset only**.
  Fill uses a centered crop without stretching; Native keeps the complete right
  eye. Neither changes your headset view. OBS captures the same mirror window.
  Alt-Tab works freely, and the hidden original game window stays hidden on exit.
- **Tutorials that finish and stay finished:** cards retire when their action
  succeeds or after ten seconds of visible gameplay. Progress is saved correctly,
  so completed movement/holster lessons no longer cycle back. No lesson requires
  spending a grenade, medkit or ammunition. Added kick/slide and option-aware
  pickup guidance follows your current controls.
- **Better physical grabbing:** supported pickups and belt magazines seat at
  your visible hand contact, preserving close grabs and saved hand fitting.
- **Kick doors open:** the existing flying kick can activate a closed door when
  the boot makes contact. Locks and scripted progression still apply.
- **Switch weapons during an unfinished reload:** weapon selection no longer
  gets stuck waiting for the reload to finish.

Close the game, extract the complete ZIP and choose **Setup > Upgrade**. Keep
setup-files beside Setup. Saves, calibration and language backups are preserved;
no reset is required. Previous mirror preferences migrate automatically. New
installations default to Fill. See the [launcher and OBS tutorial](INSTALLATION.md#recording-with-obs)
and [tutorial guidance](CONTROLS.md#interaction-hints).

The ladder fixes, grounded body fitting, either-hand flashlight, full-body IK,
kick/slide and language import remain included. Original language media plus its
matching-language 1.08 patch are intended to work across languages in theory;
only Spanish has official real-media testing.

These changes received owner acceptance on the installed development build.
Separate Steam coverage, every capture mode/door/weapon and a new headset run of
the assembled public ZIP are not claimed. The mirror-window exit correction
does not claim to fix the previously observed native crash during game shutdown.
See [known limitations](KNOWN-LIMITATIONS.md).
