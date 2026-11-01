# GS WiFI Pineapple Pager Companion App

**A free, community-built Windows companion for the Hak5 WiFi Pineapple Pager.**

**Current Version: V1.2.2 — Windows Beta**

> **Unofficial Project:** This is not an official Hak5 product. It is an independent GhostStrats community project created to make connecting to and managing the WiFi Pineapple Pager easier. It is not developed, sponsored, approved, or endorsed by Hak5.

## Why I Made This

I wanted a simpler, more modern way to connect to my WiFi Pineapple Pager, manage its files, and help beginners get comfortable using it.

I was looking for an alternative to relying on WinSCP for everyday Pager tasks. WinSCP is a capable, actively maintained tool, but its development began in **March 2000**—more than 26 years ago—and its first releases appeared later in 2000.

I wanted something built specifically around the Pager, with the tools in one place and a more approachable interface.

This app is completely free and community-built. Its purpose is to make things easier, not replace Hak5's official firmware, documentation, or support.

---

## What's New in V1.2.2

### Direct Firmware Download

Downloading official Pager firmware is now faster and easier.

- Updated the firmware download button to open the latest official Hak5 Pager firmware download directly.
- No more manually navigating through the Hak5 downloads website.
- New button: **GRAB THE LATEST PAGER FIRMWARE HERE**
- The existing guided firmware installation process remains available.

**Official latest firmware:**

https://downloads.hak5.org/api/devices/wifipineapplepager/firmwares/latest

**Special thanks to Darren Kitchen, founder of Hak5, for personally suggesting this improvement!** His feedback helped make the firmware download process even more convenient for beginners.

### Improved Pager Connection Guidance

We've added a helpful connection reminder directly inside the application.

**PAGER CONNECTION TIP**

After powering on your Pager, wait approximately **60 seconds** to allow the device to finish starting up before connecting it to your computer.

If the connection times out:

- Try connecting again.
- Make sure your USB-C cable supports data transfer, not just charging.
- Check that your Pager is powered on and fully started.
- Verify your Pager's connection settings and credentials.

These instructions are also shown when the application encounters a connection timeout.

### Improved Windows Installer

The installer now provides clearer visual feedback during installation.

- Animated purple activity indicator.
- Live elapsed-time counter.
- Moving installation status animation.
- Improved feedback during Install, Repair, and Uninstall.
- Clearer completion and error notifications.

These improvements help users recognize that the installer is still working during longer operations, such as setting up dependencies.

### Installer Security Improvements

- Removed an unnecessary PowerShell execution-policy bypass previously used for creating shortcuts.
- Updated desktop shortcut creation to use native Windows functionality.
- Added verification of the official Python download using SHA-256 before execution.
- Improved transparency when additional dependencies need to be installed.

**Important:** The installer is currently unsigned. Windows SmartScreen or antivirus software may display security warnings. An unsigned application is not automatically malicious, but antivirus detections should be investigated rather than bypassed.

### Version and File Updates

- Updated application version to **V1.2.2**.
- Updated Windows installer version to **V1.2.2**.
- Updated release filenames.
- Updated documentation and installation instructions.
- Preserved existing themes, SSH features, file management, and firmware tools.

---

## What the App Includes

- **Connect Device:** Connect to your Pager using SSH/SFTP.
- **Connection Guidance:** Startup reminders, timeout troubleshooting, and USB data-cable instructions.
- **File Manager:** Browse folders; drag and drop, upload, download, preview, or open files on your computer; replace existing items and delete files/folders with confirmation.
- **Firmware Update:** Guided installation of official Pager firmware, direct latest-firmware download, optional SHA-256 checksum comparison, and installation/reboot status messages.
- **Virtual Pager:** Open the Pager's local web interface.
- **Pager Terminal:** Open an SSH terminal session.
- **Payloads & Themes:** Shortcuts to Hak5's GitHub repositories and a beginner installation guide.
- **Reset Saved SSH Key:** Reset a saved Pager SSH host-key entry after an intentional reset or reflash, with fingerprint verification on reconnection.
- **Appearance:** Black & Gray, Black & Yellow, and GhostStrats Purple themes.
- **Animated Installer:** Visual activity indicator, elapsed timer, and installation status feedback.

**Note:** Theme creation is not included. This application helps you download and install existing Pager themes.

---

## Download and Install (Windows)

### Installation Instructions

1. Under **Releases**, download `GhostStrats-V122-INSTALL.zip`.
2. Right-click the ZIP and select **Extract All**.
3. Open the extracted folder and review the included README and DISCLAIMER.
4. Run the included **GS WiFI Pineapple Pager Companion App V1.2.2 Setup** executable.
5. Select **Install / Upgrade**.
6. Follow the installer instructions and allow any necessary dependencies to install.
7. Once installation finishes, launch the application from the Desktop or Start Menu shortcut.
8. Power on your Pager and allow approximately **60 seconds** for startup.
9. Connect the Pager to your computer using a USB-C cable that supports data transfer.
10. Open **Connect Device** and sign in with your own Pager credentials.

The usual Pager USB network address is `172.16.52.1`.

If your connection times out, try again and confirm that your USB cable supports data transfer.

### System Requirements

- Windows 10 or Windows 11 (64-bit).
- Python 3.9–3.13 with Tkinter and pip, or allow Setup to install its private Python 3.12 runtime.
- Internet access when downloading missing dependencies.
- USB-C cable supporting data transfer.
- Hak5 WiFi Pineapple Pager.

The installer supports **Install / Upgrade, Repair, and Uninstall** for recognized installations.

**Security notice:** The setup executable is unsigned. If Windows Security identifies a threat, review the detection before running it. Do not disable antivirus protection to complete installation.

---

## Add Payloads and Themes

The **Payloads & Themes** section opens the relevant Hak5 GitHub repositories, where you can browse and download available community files.

- [Hak5 Pager repository collection](https://github.com/hak5/wifipineapplepager)
- [Pager payloads](https://github.com/hak5/wifipineapplepager-payloads)
- [Pager themes](https://github.com/hak5/wifipineapplepager-themes)

Download the files you want from GitHub and **extract any ZIP archives first**.

Use the application's File Manager to upload files or folders to the appropriate location.

### Payload Locations

Internal storage:

`/root/payloads/user/`

SD-card storage:

`/mmc/root/payloads/user/`

### Theme Locations

Internal storage:

`/root/themes/`

SD-card storage:

`/mmc/root/themes/`

Follow the individual payload or theme repository README for additional instructions and correct folder structure.

**Back up important files before replacing or deleting folders.**

Run payloads only on devices and networks you own or are authorized to test.

---

## Firmware and Safety

The application now provides a direct download shortcut for the latest official Pager firmware.

**Latest firmware:**

https://downloads.hak5.org/api/devices/wifipineapplepager/firmwares/latest

**Official Hak5 firmware downloads page:**

https://downloads.hak5.org/pineapple/pager

Download official Pager firmware only.

Firmware updates can fail if power or connectivity is interrupted.

Keep the Pager powered on and allow sufficient time for the installation and automatic reboot.

A completed firmware upload does **not** necessarily mean the firmware installation has finished.

When Hak5 publishes a reference SHA-256 value, the application's optional checksum comparison can help verify the downloaded firmware.

---

## Source Code and Transparency

A separate source download is available for developers, contributors, and anyone interested in reviewing how the application works.

**Source archive:**

`GhostStrats-V122-SOURCE.zip`

The source package includes the application source code, project assets, and Windows build instructions.

The installer is provided separately for users who just want to install the application.

**Source availability is not a license grant.** No software license has been selected for this release. Please request permission before redistributing modified versions or reusing project artwork.

---

## Uninstall

To remove the application:

1. Open **Windows Settings**.
2. Navigate to **Apps → Installed Apps**.
3. Find **GS WiFI Pineapple Pager Companion App**.
4. Select **Uninstall**.

You can also use the installer’s Uninstall option.

Uninstalling the Windows application does not remove shared/system Python installations or erase files stored on the physical Pager.

Saved application preferences may be retained.

---

## Testing and Known Limitations

Version V1.2.2 has undergone automated testing, including tests covering the application changes and installer behavior.

- 37 automated tests passed during the V1.2.2 update.
- Windows application and installer executables compiled successfully.
- Connection reminder visibility was checked in a graphical test environment.
- Release ZIP files underwent integrity checks.

**Physical Pager testing and complete Windows installation, upgrade, repair, and uninstall validation are still recommended before considering this release production-stable.**

Antivirus compatibility can vary between systems. The installer has not been guaranteed free of SmartScreen or antivirus warnings.

---

## Special Thanks

A special thank you to **Darren Kitchen, founder of Hak5**, for suggesting the direct firmware download improvement.

The goal of this project has always been to help make the WiFi Pineapple Pager easier to use, especially for beginners.

Suggestions and feedback from the community help improve the application and make these tools more accessible.

Thank you to everyone supporting, testing, and sharing feedback on the project!

---

## Disclaimer

**Not an official Hak5 product.**

This is an independently built community companion created by GhostStrats to simplify WiFi Pineapple Pager management.

Hak5, WiFi Pineapple, and related names belong to their respective owners.

This software is provided **as-is**, without warranty. Use it at your own risk.

Users are responsible for backups, firmware choices, payloads, permissions, and compliance with applicable laws.

See the included disclaimer for more information.

---

## Project History

[WinSCP project history](https://winscp.net/eng/docs/project_history) documents work beginning in March 2000 and public releases later in 2000.

WinSCP remains a separate, actively maintained project. This application is simply a Pager-focused alternative.

---

**Current Release:** V1.2.2 — Windows Beta

**Created by GhostStrats**

*Privacy is Rebellion. Safety is an Illusion.*
