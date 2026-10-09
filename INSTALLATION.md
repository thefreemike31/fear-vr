# Installation, updates, and recovery

## Upgrading to v1.7.6

Close the game, extract the complete v1.7.6 ZIP, keep setup-files beside Setup,
and choose **Upgrade**. Install the complete launcher, mirror helper and gameplay
files together; do not copy only a DLL. Saves, language backups, calibration and
tutorial progress are preserved. No profile or calibration reset is required.
The simpler launcher/OBS workflow is explained [below](#recording-with-obs).

v1.7.6 also handles an inherited SteamVR 64-bit runtime selection automatically
when a valid 32-bit counterpart is present. Start through **F.E.A.R. VR.exe**.
No global runtime change is required. If the launcher reports a missing or invalid
counterpart, see [SteamVR startup repair](TROUBLESHOOTING.md#steamvr-runtime-selection-edge-case).
Confirmation from affected headset users is still pending.

<a id="import-spanish-game-text-and-voices"></a>
## Import game text and voices

**Updated in v1.6.1:** use the launcher's **Import language** button with your
original language DVD/ISO and the official **1.08 patch in that same language**.
All original language editions are intended to work in theory; **only Spanish
has been officially tested with real media and VR gameplay**. Other languages
remain unverified. v1.6.1 removes the accidental Spanish-only media restriction.
The reader supports the original InstallShield cabinet layout; incomplete,
modified, split or different-format media can be refused. No language whitelist
is imposed. You supply the ISO and patch; no game-language data is included.

1. Close F.E.A.R. and install/upgrade the VR mod to **v1.6.1 or later**.
2. Insert your original language DVD, or right-click its ISO in Windows and
   choose **Mount**. It must appear as a DVD drive. Eject other F.E.A.R. discs so
   only the intended language is mounted; keep all cabinet files available.
3. Open **F.E.A.R. VR.exe from the GOG or Steam installation you want to change**.
4. Click **Import language**, confirm, and select the original **1.08 updater EXE
   in the same language as the disc**. For example, the tested Spanish updater is
   `fear_update_es_100-107_108.exe`; it is an example, not the only accepted name.
   Matching the disc and patch language is your responsibility; the launcher
   validates archive structure and checksums, not the language of the voices.
5. Wait for the completion message. The launcher reads the media and updater;
   **it never runs the updater** or replaces the game executable.
6. Keep **FEAR-VR-Language** in the game folder. It holds recovery information
   and backups of the nine language archives replaced by the import.
7. To return to the previous language, close the game, open the same launcher,
   and click **Reset language**. v1.6 Spanish backups still work after upgrading.
   Reset before importing a different language. Do not mix archives manually.

Saves and VR calibration are preserved. The launcher language dropdown changes
launcher text only; it is independent of the game-language import. Prompts are
localized in all ten launcher languages. Other language ISOs, Steam Spanish VR
and full-campaign language coverage are not established by the Spanish GOG test.

If the disc is not detected, check the mounted drive and complete cabinet files.
If the updater is refused, use the complete matching original 1.08 patch. Keep
backups and the exact error if recovery fails; see
[troubleshooting](TROUBLESHOOTING.md#language-import-and-reset).

## Before installing

Use the verified GOG **F.E.A.R. Platinum Collection** or original Steam
**F.E.A.R. base game** on Windows 10/11. Start the unmodified game once and confirm that it reaches the menu and
loads a level, then quit. Fix an existing flat-game launch failure first.
Setup rejects unsupported executable versions; do not substitute an executable
from an unrelated patch or mod to get past that check.

For a clean baseline, start with a separate unmodified GOG or Steam installation rather
than combining graphics wrappers, audio replacements, or other mods. Keep
your normal save backups. This release covers the original single-player campaign.

## Download and verify

1. Open [GitHub Releases](https://github.com/thefreemike31/fear-vr/releases/latest).
2. Expand **Assets** if needed. Download **fear-vr-v1.7.6.zip** and
   **fear-vr-v1.7.6.zip.sha256**. Ignore GitHub's automatic Source code archives.
3. Open the `.sha256` file in Notepad. Its first 64 characters are the expected hash.
4. In the folder containing the ZIP, open PowerShell and run:

   ```powershell
   Get-FileHash -Algorithm SHA256 -LiteralPath '.\fear-vr-v1.7.6.zip'
   ```

5. Compare all 64 characters. Letter case does not matter. A mismatch means
   stop and download again from the official release.
6. Right-click the ZIP, choose **Extract All**, and extract it into a new folder.
   Do not run Setup inside the ZIP. Do not merge it into an older extracted package.

An unsigned-publisher/SmartScreen reputation message is different from a named
antivirus detection. If a threat is reported or a file is quarantined, keep
protection enabled and follow [download troubleshooting](TROUBLESHOOTING.md#download-or-antivirus-problem).

## Install or upgrade

1. Close every running F.E.A.R. instance.
2. Open **F.E.A.R. VR Setup.exe** from the extracted folder. Keep **setup-files**
   beside it; Setup needs that folder.
3. Check **Game folder**. It must contain the original **FEAR.exe**, not an
   expansion or the folder where you extracted the mod. Choose **Choose another
   game folder** if detection selected the wrong copy.
4. Select **Install F.E.A.R. VR** or **Upgrade F.E.A.R. VR**. A prior beta can be
   upgraded directly; uninstalling it first is not required.
5. Wait for the success message. Setup does not start the game.

If Windows denies writes to a protected game folder, close Setup and use
**Run as administrator** on the same Setup executable. Keep the error text if
that fails. Do not remove the recovery folder to force another installation.

Setup backs up replaced files and preserves modified managed files under
**FEAR-VR-Install/preserved-files**. Saves and profiles are kept. Keep the
**FEAR-VR-Install** folder and its backups while the mod is installed.

On Steam, Setup also manages the included input polling fix. GOG does not receive
that input DLL. Upgrades from the v1.0 tester package use the same **Upgrade**
action; keep the original installation's recovery files.

## Connect the headset

Choose one route for a launch. You do not need to install an extra graphics or
audio wrapper; the release includes its required mod components.

### Virtual Desktop + VDXR

1. Open the Virtual Desktop Streamer on your PC and select **VDXR** as its
   preferred OpenXR runtime.
2. Connect from Virtual Desktop in your headset. Confirm both controllers track.
3. Close SteamVR on the PC. A running usable SteamVR takes priority in the
   mod's automatic selection.
4. Run **F.E.A.R. VR.exe** from the installed game folder using your desktop view.

Virtual Desktop's OpenXR implementation can run OpenXR games without SteamVR.
See the [VDXR project](https://github.com/mbucchia/VirtualDesktop-OpenXR) and
[Virtual Desktop downloads](https://www.vrdesktop.net/) for the runtime itself.

### Steam Link or a SteamVR headset

1. Start SteamVR and connect your headset. With Steam Link, connect its headset
   app to your PC. Wait until the headset and controllers are tracked.
2. Use a SteamVR build that includes **Win32/32-bit OpenXR support**. If the
   launcher reports that it cannot find a usable runtime, update SteamVR; use
   its beta branch if that support is unavailable in your stable version.
3. In SteamVR Settings, find **OpenXR** (enable advanced settings if necessary)
   and use **Set SteamVR as OpenXR Runtime**, then restart SteamVR if discovery
   still fails. This changes the system default; the mod launcher does not
   change your machine-wide runtime setting.
4. Run **F.E.A.R. VR.exe** in the installed game folder.

Meta Quest Link and Air Link are unsupported, including through SteamVR.

## Recording with OBS

The launcher now uses **one mirror for both the desktop and OBS**. There is no
separate OBS checkbox, window/fullscreen choice or desktop-resolution selector.
OBS is installed separately; no OBS OpenXR layer or extra capture plugin is needed.
The mirror shows the rendered **right eye**, while the headset keeps its normal
stereo view.

1. Close the game and open **F.E.A.R. VR.exe**.
2. Choose the mirror you want:

   | Launcher choice | Result |
   | --- | --- |
   | **16:9 - fill screen** | A 3840 x 2160 mirror, filled by a centered crop without stretching or added side bars. A tall eye loses some top/bottom content. Recommended for a widescreen recording. |
   | **Native - full view** | The complete eye at its native resolution and aspect. A widescreen OBS canvas may have side bars. |
   | **Off - headset only** | No desktop/OBS mirror after VR starts. Choose a visible mode to record. |

3. Select **Play in VR**. In OBS, add **Game Capture**, choose **Capture specific
   window**, and select **F.E.A.R. VR Capture (FEARVR-Capture.exe)**. Existing scenes
   targeting that window can keep using it.
4. Select the OBS source, reset its transform (**Ctrl+R**), then **Fit to Screen
   (Ctrl+F)**. Remove any old source cropping. For Fill, use a 16:9 canvas/output
   such as 1920 x 1080 or 3840 x 2160. For Native without side bars, match the
   canvas/output aspect to the source's actual dimensions.
5. Make a short recording and check framing, audio and smoothness. **Alt-Tab** can
   bring OBS or another app forward while VR continues. Stop recording in OBS
   before quitting the game normally.

Recording is controlled in OBS; choosing a mirror does not record a video.
Use **Game Capture** for the source; Window Capture sees the smaller desktop
preview. Mirror choices do not change headset resolution or framing.

New installations default to **16:9 - fill screen**. Previous full-eye preferences
migrate to **Native** and previous wide capture to **Fill**. An old unchecked OBS
box does not automatically select Off. Choosing **Play in VR** saves preferences;
previewing or canceling does not. Changes take effect on the next launch.

Closing only the mirror leaves VR running without a mirror; restart the game to
bring it back. A brief original game window may appear during startup, then hides
when VR/the mirror is ready. If the helper fails, the original game window can
return as a fallback. The mirror closes when the game ends. The fixed blank-window
issue is separate from a previously observed native exit crash; see
[troubleshooting](TROUBLESHOOTING.md#obs-capture-window).

The owner accepted the new mirror, Alt-Tab and window shutdown. A new recording
of every mode and separate Steam headset coverage are not claimed; check your
own short recording before a long session.

## Launcher language

The launcher defaults to **Automatic**, using your Windows UI-language preferences
with English as the fallback. You can select English, French, German, Spanish,
Italian, Polish, Russian, Brazilian Portuguese, Simplified Chinese or Traditional
Chinese. The selector changes the UI immediately; **Play** saves the choice for
both editions. Cancel and previews do not save it.

This translates the launcher and common messages, independently of the game's
installed language. Technical logs and the Controls guide remain in English.
Native-speaker review and automatic selection on non-English Windows systems
remain open to feedback.

## First launch

Use **F.E.A.R. VR.exe**, not **FEAR.exe** or an existing store shortcut that starts
the flat game. You can make a desktop shortcut to the VR executable. Leave it
beside the installed game; do not move the executable itself to the desktop.

Choose **16:9 - fill screen**, **Native - full view**, or **Off - headset only**,
then select **Play in VR**. Fill is the first-run default. **Play in VR** saves
your choice; canceling or previewing does not. These choices affect the desktop
mirror, not the headset. See [mirror choices and OBS](#recording-with-obs).
**Controls** opens the player guide; **Open log folder** opens support logs.
Leave the launcher running during startup and play.

Wake both controllers before launch. In **Options > VR Settings**, review
[movement and controls](CONTROLS.md), then [calibration](CALIBRATION.md).
Start with **Centered (Recommended)** projection and **100% View Width**.
The initial movement mode is running; turning speed and comfort are adjustable.

For later versions, follow that release's notes, download its complete ZIP,
verify it, extract it into a new folder, and use **Upgrade**. Do not manually
mix DLLs from different releases.

## Uninstall

1. Close F.E.A.R.
2. In the game folder, open **FEAR-VR-Install/Uninstall F.E.A.R. VR.exe**.
3. Choose **Uninstall F.E.A.R. VR** and wait for success.
4. Original replaced files are restored; mod-created managed files are removed.
   Modified managed files are preserved, and saves/profiles are retained.

The recovery executable and backups are deliberately kept. Their presence does
not mean the VR mod is still active. Use the original game launcher to test
the restored base game. Reinstall using the complete release's Setup.

## Interrupted installation

Reopen Setup for the **same game folder** and choose **Recover interrupted
setup**. When recovery succeeds, retry the install, upgrade, or uninstall.
If it reports changed files or a damaged snapshot, stop and preserve the error
and the **FEAR-VR-Install** folder. Do not delete receipts/backups or repeatedly
overwrite files. Follow [Setup recovery troubleshooting](TROUBLESHOOTING.md#setup-stops-or-recovery-fails).

## Steam installation and startup

On the first normal Steam VR start, the launcher prepares the verified original
executable for up to 4 GB of address space on 64-bit Windows, then continues into
VR automatically. Press **Play in VR** once and let it finish. Keep
**FEAR.exe.fearvr-memory-original**, the original backup beside FEAR.exe.
GOG already supports the larger address space; its executable is unchanged.
See [memory recovery](TROUBLESHOOTING.md#steam-memory-preparation) for opt-out
and restoration. Do not apply a separate 4 GB patch or combine executable mods.

If Setup detects multiple copies, select the Steam base-game folder you intend
to test. Keep the original store executable. Sign into Steam with the owning
account, then use **F.E.A.R. VR.exe** in that folder. Do not close the launcher
during startup. A failed Steam VR handoff stops with an error instead of silently
continuing in flat mode. Steam level loading may take several minutes.

Setup rejects conflicting loaders, including unrecognized input wrappers. The
exact Steam input fix included in this release is allowed on Steam only.
Disable other mods using their own instructions, or use a clean installation.
Store file verification may leave additional mod DLLs behind. GOG and Steam use
the same public Documents save/profile location; keep your existing save backups.
Setup does not start the game and uninstall retains saves and profiles.

## Experimental installed languages

The mod preserves official language archives already installed with a supported
GOG or Steam base game. Select/install your language through your game provider
before installing the mod, where that language is available. The mod does not
choose a language from Windows settings or include translation files.
Cyrillic menu text uses an automatic readable font fallback; the runtime fix was
tested with Russian menus on GOG. Other languages, Steam automatic-font coverage,
non-menu fonts and full campaigns remain experimental. VR-specific text may
remain English. A different retail executable is not supported merely because
its language is different.
