# VaultX Auth 🛡️

VaultX Auth is a secure, high-performance Desktop Authenticator designed to manage authentication keys, generate TOTP codes, and facilitate streamlined login procedures (such as the Riot Games login flow) with security and efficiency.

This repository serves as the official public distribution channel for VaultX Auth releases.

---

## Downloads 🚀

| Version | Platform | Installer | Size | SHA-256 Checksum |
|:---|:---|:---|:---|:---|
| **v1.0.0-beta** | Windows 10/11 | [Download Installer (Direct)](https://github.com/rockbuilds/vaultxauth-client/releases/download/v1.0.0-beta/VaultX.Auth.Setup.1.0.0.exe) | 117 MB | `e597f40e0a2740dabcbbcb8e50f53ed52627e6e71ea6f3dec6c66cc10173371d` |

> [!IMPORTANT]
> Always verify that the SHA-256 checksum of your downloaded installer matches the checksum above before running it.

---

## Verification Guide 🔒

To guarantee file integrity and ensure the installer hasn't been modified or tampered with, you can run the following command in Windows PowerShell after downloading:

```powershell
# Go to your Downloads folder
cd "$env:USERPROFILE\Downloads"

# Compare the hash
(Get-FileHash -Algorithm SHA256 "VaultX Auth Setup 1.0.0.exe").Hash -eq "e597f40e0a2740dabcbbcb8e50f53ed52627e6e71ea6f3dec6c66cc10173371d"
```
*If this command returns `True`, your download is safe and authentic.*

---

## Installation Steps ⚙️

1. Download the latest `VaultX Auth Setup 1.0.0.exe` installer from the [Releases](https://github.com/rockbuilds/vaultxauth-client/releases/download/v1.0.0-beta/VaultX.Auth.Setup.1.0.0.exe) page.
2. Double-click the installer to run the setup wizard.
3. The setup installs the software and automatically places a shortcut on your Desktop and Start Menu.
4. Open **VaultX Auth** to begin using the authenticator.

---

## Troubleshooting & Antivirus Notes ⚠️

### 1. Windows SmartScreen Block / Windows Defender Flags
Because VaultX Auth is a custom, unsigned binary containing an integrated Python engine, Windows SmartScreen or standard Antivirus software might trigger false-positive warnings (e.g., "Unknown Publisher").

- **To bypass SmartScreen:** Click **More Info** and select **Run Anyway**.
- **Why it happens:** Code signing certificates cost thousands of dollars annually. To keep our distribution lightweight and independent, we do not bundle commercial code signing. Verify the hash above to be absolutely sure the file is clean.

### 2. Startup Port Conflict (Error 10048)
If the application fails to start or shows a port error, verify that port `8000` is not being occupied by another background application (like another local web developer server or proxy tool).
