# F.E.A.R. VR v1.7.6 - SteamVR startup and holster hotfix

- **SteamVR launcher edge case:** if the launcher inherits a selection of
  SteamVR's 64-bit OpenXR runtime, it now checks and selects the valid 32-bit
  counterpart required by F.E.A.R. VR. Invalid or missing counterparts produce
  a repair message before the game starts. Valid custom 32-bit overrides remain
  selected; global runtime settings and normal automatic routing are unchanged.
- **Stable weapon holsters:** existing weapons keep their body slots across
  unrelated pickups, inventory reordering and weapon selection. Compatible swaps
  inherit the outgoing weapon's slot, including physical drop-then-pickup swaps.
  Layouts persist in saves. The existing heavy-weapon/three-long-gun back-slot
  rule still applies and only moves the weapons involved.

Close the game, extract the complete ZIP, keep setup-files beside
**F.E.A.R. VR Setup.exe**, and choose **Upgrade**. Saves, calibration, language
backups and tutorial progress are preserved; no reset is required. Old saves
without a remembered holster layout use the normal default arrangement.

The holster fix received owner headset acceptance. The launcher fix is implemented
and passed GOG/Steam diagnostic checks, but confirmation from affected headset
users is still pending. This is a targeted startup fix, not a claim that every
SteamVR startup problem is resolved. No fresh assembled-ZIP headset run is claimed.

All v1.7.5 features remain included. See the [launcher/OBS guide](INSTALLATION.md#recording-with-obs),
[controls](CONTROLS.md), and [known limitations](KNOWN-LIMITATIONS.md).
