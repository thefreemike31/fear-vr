# Installation, updates, and recovery

## Upgrading to v1.7.1

This hotfix repairs a progress-blocking ladder regression from the body update.
Close the game, extract the complete v1.7.1 ZIP, keep setup-files beside Setup,
and choose **Upgrade**. Keep all body meshes and the new capture helper together;
do not copy only the DLL. Saves, language backups and calibration remain intact.
No profile or calibration reset is required. The new optional OBS workflow is
explained [below](#recording-with-obs).

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
2. Expand **Assets** if needed. Download **fear-vr-v1.7.1.zip** and
   **fear-vr-v1.7.1.zip.sha256**. Ignore GitHub's automatic Source code archives.
3. Open the `.sha256` file in Notepad. Its first 64 characters are the expected hash.
4. In the folder containing the ZIP, open PowerShell and run:

   ```powershell
   Get-FileHash -Algorithm SHA256 -LiteralPath '.\fear-vr-v1.7.1.zip'
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

The optional experimental capture window provides the complete rendered **right
eye** through a separate desktop helper. OBS is installed separately. No OBS
OpenXR layer or extra capture plugin is required. Capture is off by default.

1. Close the game and open **F.E.A.R. VR.exe**. Enable **OBS capture window**.
2. Choose **Windowed** or **Borderless (desktop size)**. Capture disables exclusive
   fullscreen so the Windows desktop keeps its resolution.
3. Choose **Capture: native eye (1:1)** for the full eye at its rendered resolution,
   or **Capture: 16:9 (fit full eye)** for a 3840 x 2160 source containing the whole
   eye. These choices change capture framing, not headset resolution.
4. Select **Play in VR**. In OBS, add a **Game Capture** source, choose
   **Capture specific window**, and select **F.E.A.R. VR Capture**
   (**FEARVR-Capture.exe**). Select the capture helper, not FEAR.exe.
5. Select the OBS source, reset its transform (**Ctrl+R**) and **Fit to Screen**
   (**Ctrl+F**). Leave cropping at zero. Native capture keeps the same eye-sized
   source through menus and loading; menu content is fitted inside it.
6. For a recording at the eye's exact resolution, set OBS **Base (Canvas)** and
   **Output (Scaled)** resolutions to the capture source's dimensions. Those
   dimensions depend on your headset/runtime settings; do not copy someone else's.
   For a 16:9 recording, use a 16:9 canvas/output and Fit to Screen. A near-square
   eye has side bars when fitted to 16:9; removing them requires cropping or
   distortion. The capture mode preserves the complete view.
7. Make a short recording and check framing, audio and smoothness before a long
   session. You can bring OBS to the foreground while VR stays live.
   Stop OBS recording before quitting the game.

To return to ordinary play, close the game, turn **OBS capture window** off and
launch again. Format changes take effect on the next launch. If you close the
capture window manually, restart the game to reopen it. The helper closes when
the game ends. Recording is controlled in OBS; this launcher option alone does
not record a video. Use Game Capture: Window Capture sees the smaller desktop
preview. The launcher's desktop 720p/1080p setting does not set capture resolution.

This first capture release has known follow-ups: an intermittent control glitch
and native Quit/exit crashes have been observed; their causes are unconfirmed.
Compare a fresh launch with capture off if controls or performance change.
GOG gameplay recordings cover windowed native/16:9 and borderless native;
borderless 16:9 gameplay and the full Steam capture matrix remain unverified.
See [capture troubleshooting](TROUBLESHOOTING.md#obs-capture-window).

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

Choose **Fullscreen** (the first-run default), **Windowed**, or **Borderless
(desktop size)**. Windowed offers **1280 x 720** or **1920 x 1080**. Select
**Play in VR** when ready. Your choice is
remembered across launches and editions; closing without playing does not save
changes. These settings control the desktop mirror, not headset resolution.
The game may also remember the desktop resolution in its normal display settings.
**Controls** opens the player guide; **Open log folder** opens support logs.
Leave the launcher running while playing in windowed mode.

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
