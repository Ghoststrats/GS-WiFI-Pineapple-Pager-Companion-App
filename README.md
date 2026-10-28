# GS WiFI Pineapple Pager Companion App

**A free, community-built Windows companion for the Hak5 WiFi Pineapple Pager.**

> **Unofficial project:** This is **not an official Hak5 product**. It is an independent GhostStrats community project created to make connecting to and managing the WiFi Pineapple Pager easier. It is not developed, sponsored, approved, or endorsed by Hak5.

## Why I made this

I wanted a simpler, more modern way to connect to my WiFi Pineapple Pager, manage its files, and help beginners get comfortable using it.

I was looking for an alternative to relying on WinSCP for everyday Pager tasks. WinSCP is a capable, actively maintained tool, but its development began in **March 2000**—more than 26 years ago—and its first releases appeared later in 2000.

I wanted something built specifically around the Pager, with the tools in one place and a more approachable interface.

This app is free and community-built. It is meant to make things easier, not to replace Hak5's official firmware, documentation, or support.

## What the app includes

- **Connect Device:** Connect to your Pager using SSH/SFTP.
- **File Manager:** Browse folders; drag and drop, upload, download, preview, or open files on your computer; replace existing items and delete files/folders with confirmation.
- **Firmware Update:** A guided process for official signed Pager firmware, including optional SHA-256 checksum comparison and installation/reboot status messages.
- **Virtual Pager:** Open the Pager's local web interface.
- **Pager Terminal:** Open an SSH terminal session.
- **Payloads & Themes:** Shortcuts to Hak5's GitHub repositories and a beginner installation guide.
- **Appearance:** Black & Gray, Black & Yellow, and GhostStrats Purple themes.

**Note:** Theme creation is not included. This application helps you download and install existing Pager themes.

## Download and install (Windows)

1. Under **Releases**, download `GS_WiFI_Pineapple_Pager_Companion_App_V6.2.3_Easy_Install.zip`.
2. Right-click the ZIP and choose **Extract All**. Open the extracted folder.
3. Read `README.txt` and `DISCLAIMER.txt`, then double-click `GS_WiFI_Pineapple_Pager_Companion_App_Setup_V6.2.3_RC.exe`.
4. Choose **Install / Upgrade**. The installer can also **Repair** or **Uninstall** a recognized installation.
5. If Python or required packages are missing, Setup will attempt to install them; an internet connection is needed. The setup window also provides a link to the official Python download page if automatic setup fails.
6. Launch the program from the Desktop or Start Menu shortcut, connect your Pager to the computer using a USB-C **data** cable, and sign in with your own Pager credentials. The usual USB network address is `172.16.52.1`.

**Requirements:** Windows 10/11 (64-bit); Python 3.9–3.13 with Tkinter and pip (or allow Setup to install its private Python 3.12 runtime); an internet connection for missing dependencies.

The setup EXE is **unsigned**, so Windows may display an unknown-publisher warning.

## Add payloads and themes

The **Payloads & Themes** section opens the relevant **Hak5 GitHub pages**, where you can browse and download community files:

- [Hak5 Pager repository collection](https://github.com/hak5/wifipineapplepager)
- [Pager payloads](https://github.com/hak5/wifipineapplepager-payloads)
- [Pager themes](https://github.com/hak5/wifipineapplepager-themes)

Download the files you want from GitHub, **extract any ZIP archives first**, and use the app's **File Manager** to drag them into the correct folder or click **Upload Files / Upload Folder**.

- **Payloads:** Use the appropriate category under `/root/payloads/user/`, or `/mmc/root/payloads/user/` for SD-card storage.
- **Themes:** Use `/root/themes/`, or `/mmc/root/themes/` for SD-card storage.

Follow each payload/theme repository's README for any additional folder structure or setup requirements.

**Back up files before replacing or deleting folders.** Run payloads only on devices and networks you own or are authorized to test.

## Firmware and safety

Download **official Pager firmware only** from:

https://downloads.hak5.org/pineapple/pager

Firmware updates can fail if power or connectivity is interrupted.

Keep the Pager powered on and allow it time to reboot automatically. A completed upload is **not** the same as a completed firmware installation.

An optional checksum comparison helps verify the downloaded file when Hak5 publishes a reference SHA-256 value.

## Source code and transparency

A separate `GS_WiFI_Pineapple_Pager_Companion_App_V6.2.3_Source_Code.zip` contains the Python and Go source files, assets, and Windows build instructions for inspection.

The release installer is a separate download for users who just want to install the app.

**Source availability is not a license grant.** No license has been selected for this release; please ask for permission before redistributing modified versions or reusing project artwork.

## Uninstall

Use **Windows Settings → Apps → Installed Apps**, select **GS WiFI Pineapple Pager Companion App**, and choose **Uninstall**.

Uninstalling this Windows application does not uninstall shared/system Python or erase files on the physical Pager. Saved app preferences may be retained.

## Disclaimer

**Not an official Hak5 product.** This is an independently built community companion made to simplify Pager management.

Hak5, WiFi Pineapple, and related names belong to their respective owners.

This software is provided **as-is**, without warranty; use it at your own risk.

The user is responsible for backups, firmware choices, payloads, permissions, and compliance with applicable laws. See `DISCLAIMER.txt` in the easy-install download.

## Project history

[WinSCP project history](https://winscp.net/eng/docs/project_history) documents work starting in March 2000 and public releases later in 2000.

WinSCP remains a separate, actively maintained project; this app is simply a Pager-focused alternative.

**Release:** v6.2.3 (release candidate).

Full installation/upgrade/uninstall and physical Pager testing should be completed on Windows before calling it production-stable.
