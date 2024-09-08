#

# Install Process

## Chocolatey Install

This script install chocolatey packet manager needed in order to install all the other apps via terminal.

```
powershell -command "Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))"
```

## Refreshing Environment

Refreshes terminal environment to make chocolatey work without opening another terminal shell.

```
call "%ProgramData%\chocolatey\bin\RefreshEnv.cmd"
call RefreshEnv.cmd
```

## Installing Apps

Refreshes Windows Explorer to avoid any chocolatey bugs/errors. and then proceeds to install the apps via `choco install`, with `-y` chocolatey argument.

```
taskkill /f /im explorer.exe && start explorer.exe && start cmd /k "choco install list-of-apps -y"
```

# List of the apps available

- Browsers:
  - Chrome
  - Firefox
  - Brave
  - Opera
  - Vivaldi
  - LibreWolf
  - Chromium
  - Ungoogled Chromium
- Compression:
  - 7Zip
  - PeaZip
  - WinRAR
  - NanaZip
- Gaming:
  - Steam
  - Epic Games
  - EA APP
  - Minecraft
  - Playnite
  - Prism Launcher
- Utiltiies:
  - Everything
  - CCleaner
  - Revo Uninstaller
  - TeamViewer
  - Anydesk
  - ImgBurn
  - qBitTorrent
  - Bulk Crap Uninstaller
  - Bulk Rename Utility
  - MSI AfterBurner
  - CPU-Z
  - HWinfo
  - HWMonitor
  - Display Driver Uninstaller
  - Rainmeter
  - StartAllBack
  - Translucent Taskbar
- Microsoft Tools:
  - OneDrive
  - PowerToys
  - Windows Terminal
  - Autoruns
  - Process Monitor
  - Nuget
  - Visual C++ 2015-22
- Multimedia:
  - VLC
  - AIMP
  - iTunes
  - foobar2000
  - Audacity
  - Spotify
  - HandBrake
  - MediaMonkey
  - OBS Studio
- Comunication:
  - Discord
  - Zoom
  - Telegram
  - Whatsapp
  - Skype
  - Teams
  - Slack
  - Thunderbird
- Imaging:
  - Blender
  - DarkTable
  - Krita
  - GIMP
  - InkScape
  - ShareX
  - LightShot
  - Greenshot
- Documents:
  - Adobe Acrobat Reader
  - LibreOffice
  - SumatraPDF
  - OpenOffice
  - Obsidian
  - Joplin
- Security:
  - MalwareBytes
  - Avast
  - AVG
- For Developers:
  - Git
  - GitHub Desktop
  - NodeJS
  - Python 3
  - JDK 8
  - NET 4.8
  - NET 8
  - Notepad++
  - Sublime Text
  - Neovim
  - VS Code
