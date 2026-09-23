# Installation, updates, and recovery

[Back to the main guide](README.md) · [Troubleshooting](TROUBLESHOOTING.md)

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
2. Expand **Assets** if needed. Download **fear-vr-v1.4.1.zip** and
   **fear-vr-v1.4.1.zip.sha256**. Ignore GitHub's automatic Source code archives.
3. Open the `.sha256` file in Notepad. Its first 64 characters are the expected hash.
4. In the folder containing the ZIP, open PowerShell and run:

   ```powershell
   Get-FileHash -Algorithm SHA256 -LiteralPath '.\fear-vr-v1.4.1.zip'
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

Choose **Fullscreen** (the first-run default) or **Windowed**, with **1280 x 720**
or **1920 x 1080** for windowed mode, then select **Play in VR**. Your choice is
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
