#

# Remove Windows Apps

## Remove 3rd-party apps

This script is a set of PowerShell commands that remove specific Windows apps (usually pre-installed or downloaded from the Microsoft Store) from a system.

#### The script targets the following apps for removal:

- Candy Crush Saga: "king.com.CandyCrushSaga"
- Candy Crush Soda Saga: "king.com.CandyCrushSodaSaga"
- Shazam: "ShazamEntertainmentLtd.Shazam"
- Flipboard: "Flipboard.Flipboard"
- Twitter: "9E2F88E3.Twitter"
- iHeartRadio: "ClearChannelRadioDigital.iHeartRadio"
- Duolingo: "D5EA27B7.Duolingo-LearnLanguagesforFree"
- Adobe Photoshop Express: "AdobeSystemsIncorporated.AdobePhotoshopExpress"
- Pandora: "PandoraMediaInc.29680B314EFC2"
- Eclipse Manager: "46928bounde.EclipseManager"
- Actipro Software: "ActiproSoftwareLLC.562882FEEB491"
- Spotify: "SpotifyAB.SpotifyMusic"

```PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "king.com.CandyCrushSaga" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage \"king.com.CandyCrushSodaSaga\" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage \"ShazamEntertainmentLtd.Shazam\" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage \"Flipboard.Flipboard\" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage \"9E2F88E3.Twitter\" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage \"ClearChannelRadioDigital.iHeartRadio\" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage \"D5EA27B7.Duolingo-LearnLanguagesforFree\" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage \"AdobeSystemsIncorporated.AdobePhotoshopExpress\" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage \"PandoraMediaInc.29680B314EFC2\" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage \"46928bounde.EclipseManager\" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage \"ActiproSoftwareLLC.562882FEEB491\" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage \"SpotifyAB.SpotifyMusic\" | Remove-AppxPackage"
```

## Remove extension apps

This script is a set of PowerShell commands designed to remove specific image and video extension apps from a Windows system.

#### The script targets the following extensions:

- HEIF Image Extension:
- WebP Image Extension:
- HEVC Video Extension:
- Raw Image Extension:
- Web Media Extensions:

```PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.HEIFImageExtension" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage \"Microsoft.VP9VideoExtensions\" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage \"Microsoft.WebpImageExtension\" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage \"Microsoft.HEVCVideoExtension\" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage \"Microsoft.RawImageExtension\" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage \"Microsoft.WebMediaExtensions\" | Remove-AppxPackage"
```

## Remove Microsoft apps

This PowerShell script contains a series of commands to remove a wide range of Microsoft apps and built-in applications from a Windows system. Each command uses the Get-AppxPackage cmdlet to locate a specific app by its package name and then uses Remove-AppxPackage to uninstall it.

#### List of Apps Targeted for Removal:

- Microsoft Family Safety
- Outlook for Windows
- Clipchamp
- 3D Builder
- 3D Viewer
- Bing Weather
- Bing Sports
- Bing Finance
- Office Hub
- Bing News
- OneNote
- Sway
- Windows Phone
- Communications Phone
- Your Phone
- Get Started
- Microsoft Solitaire Collection
- Sticky Notes
- Communications Apps
- Skype
- GroupMe
- To-Do
- Mixed Reality Portal
- Feedback Hub
- Alarms & Clock
- Camera
- MS Paint
- Maps
- Minecraft for Windows
- People
- Wallet
- Print 3D
- OneConnect

```
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "MicrosoftCorporationII.MicrosoftFamily" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.OutlookForWindows" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Clipchamp.Clipchamp" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.3DBuilder" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.Microsoft3DViewer" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.BingWeather" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.BingSports" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.BingFinance" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.MicrosoftOfficeHub" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.BingNews" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.Office.OneNote" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.Office.Sway" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.WindowsPhone" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.CommsPhone" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.YourPhone" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.Getstarted" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.549981C3F5F10" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.Messaging" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.MixedReality.Portal" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.WindowsFeedbackHub" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.WindowsAlarms" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.WindowsCamera" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.MSPaint" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.WindowsMaps" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.MinecraftUWP" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.People" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.Wallet" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.Print3D" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.OneConnect" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.MicrosoftSolitaireCollection" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.MicrosoftStickyNotes" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "microsoft.windowscommunicationsapps" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.SkypeApp" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.GroupMe10" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.Todos" | Remove-AppxPackage"####
```

## Remove Xbox apps

This PowerShell script is designed to remove various Xbox-related applications and components from a Windows system.

#### Here’s the list of targeted apps:

- Xbox App
- Xbox TCUI (Text Chat User Interface)
- Xbox Gaming Overlay
- Xbox Game Overlay
- Xbox Identity Provider
- Xbox Speech To Text Overlay

```
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.XboxApp" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.Xbox.TCUI" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.XboxGamingOverlay" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.XboxGameOverlay" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.XboxIdentityProvider" | Remove-AppxPackage"
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "Microsoft.XboxSpeechToTextOverlay" | Remove-AppxPackage"
```

# Disable Windows Features

## Internet Explorer

These commands are used to disable different versions of Internet Explorer if they are present on the system. The -NoRestart flag means the system will not restart automatically after the feature is disabled. The try-catch block ensures that if the feature is not found, a user-friendly message is displayed instead of an error.

```
powershell -Command "try { Disable-WindowsOptionalFeature -FeatureName "Internet-Explorer-Optional-amd64" -Online -NoRestart -ErrorAction Stop; Write-Output "Successfully disabled the feature Internet-Explorer-Optional-amd64." } catch { Write-Output "Feature not found." }"
powershell -Command "try { Disable-WindowsOptionalFeature -FeatureName "Internet-Explorer-Optional-x86" -Online -NoRestart -ErrorAction Stop; Write-Output "Successfully disabled the feature Internet-Explorer-Optional-x86." } catch { Write-Output "Feature not found." }"
powershell -Command "try { Disable-WindowsOptionalFeature -FeatureName "Internet-Explorer-Optional-x64" -Online -NoRestart -ErrorAction Stop; Write-Output "Successfully disabled the feature Internet-Explorer-Optional-x64." } catch { Write-Output "Feature not found." }"
```

## Hyper-V

> Virtual Machines might not work when disabling this feature

This PowerShell command disables the Hyper-V feature on a Windows system. The -NoRestart flag ensures that the system does not restart automatically after the operation. The try-catch block is used to handle errors by providing a user-friendly message if the feature is not found.

```
powershell -Command "try { Disable-WindowsOptionalFeature -FeatureName "Microsoft-Hyper-V-All" -Online -NoRestart -ErrorAction Stop; Write-Output "Successfully disabled the feature Microsoft-Hyper-V-All." } catch { Write-Output "Feature not found." }"
```

## Fax & Scan

This PowerShell command disables the Fax Services feature on a Windows system. The -NoRestart flag ensures that the system does not restart automatically after the operation. The try-catch block is used to handle errors by providing a message if the feature is not found.

```
powershell -Command "try { Disable-WindowsOptionalFeature -FeatureName "FaxServicesClientPackage" -Online -NoRestart -ErrorAction Stop; Write-Output "Successfully disabled the feature FaxServicesClientPackage." } catch { Write-Output "Feature not found." }"
```

## Media Player

This PowerShell command is used to disable the Windows Media Player feature on a Windows system. The -NoRestart flag prevents the system from restarting automatically after the operation. The try-catch block handles any errors by providing a user-friendly message if the feature is not found.

```
powershell -Command "try { Disable-WindowsOptionalFeature -FeatureName 'WindowsMediaPlayer' -Online -NoRestart -ErrorAction Stop; Write-Output 'Successfully disabled the feature WindowsMediaPlayer.' } catch { Write-Output 'Feature not found.' }"
```

## Windows Search

> Indexing and search will not work after disabling this feature

This PowerShell command disables the Search Engine Client feature on a Windows system. The -NoRestart flag ensures the system does not restart automatically after the operation. The try-catch block provides error handling by displaying a message if the feature is not found.

```
powershell -Command "try { Disable-WindowsOptionalFeature -FeatureName "SearchEngine-Client-Package" -Online -NoRestart -ErrorAction Stop; Write-Output "Successfully disabled the feature SearchEngine-Client-Package." } catch { Write-Output "Feature not found." }"

```

# Remove Microsoft Store

> Once uninstalled you will not be able to install store apps anymore.

This PowerShell command is used to uninstall the Microsoft Store from a Windows system. The -ExecutionPolicy Unrestricted flag allows the command to run without restrictions on script execution policies. The Get-AppxPackage cmdlet locates the app, and Remove-AppxPackage removes it.

```
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage "*Microsoft.WindowsStore*" | Remove-AppxPackage"
```

# Remove OneDrive

These batch commands are used to completely uninstall and remove OneDrive from a Windows system. They stop any running OneDrive processes, initiate the uninstallation process through available installers, delete associated registry keys, and remove OneDrive folders from multiple locations. This comprehensive approach helps in ensuring that no traces of OneDrive remain on the system.

```
taskkill /f /im OneDrive.exe
echo -- Uninstalling OneDrive through the installers
start %systemroot%\SysWOW64\OneDriveSetup.exe /uninstall
start %programfiles(x86)%\Microsoft Office\root\Integration\Addons\OneDriveSetup.exe /uninstall
echo -- Removing OneDrive registry keys
reg delete "HKEY_CLASSES_ROOT\WOW6432Node\{018D5C66-4533-4307-9B53-224DE2ED1FE6}" /f
reg delete "HKEY_CLASSES_ROOT\CLSID{018D5C66-4533-4307-9B53-224DE2ED1FE6}" /f
reg delete "HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run\OneDrive" /f
echo -- Removing OneDrive folders
rd "%UserProfile%\OneDrive" /Q /S
rd "%LocalAppData%\Microsoft\OneDrive" /Q /S
rd "%ProgramData%\Microsoft OneDrive" /Q /S
rd "C:\OneDriveTemp" /Q /S
```

# Remove Edge

These commands are used to completely uninstall Microsoft Edge. First, a registry key is added to enable the uninstallation process. The PowerShell script then searches for the Edge installer and runs it with specific arguments to remove Edge from the system. It provides feedback on whether the uninstallation was successful or if there were issues.

```
reg add "HKLM\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdateDev" /v "AllowUninstall" /t REG_DWORD /d "1" /f
Powershell -ExecutionPolicy Unrestricted -Command "$installer = (Get-ChildItem \"$($env:ProgramFiles)*\Microsoft\Edge\Application\*\Installer\setup.exe\"); if (!$installer) { Write-Host \"Installer not found. Microsoft Edge may already be uninstalled.\"; } else { $installer | ForEach-Object { $uninstallerPath = $_.FullName; $installerArguments = @(\"--uninstall\", \"--system-level\", \"--verbose-logging\", \"--force-uninstall\"); Write-Output \"Uninstalling through uninstaller: $uninstallerPath\"; $process = Start-Process -FilePath \"$uninstallerPath\" -ArgumentList $installerArguments -Wait -PassThru; if ($process.ExitCode -eq 0 -or $process.ExitCode -eq 19) { Write-Host \"Successfully uninstalled Edge.\"; } else { Write-Error \"Failed to uninstall, uninstaller failed with exit code $($process.ExitCode).\"; }; }; }"
```

# Remove CoPilot

These registry commands are used to configure settings related to Windows Copilot and Bing Chat:

- Disabling Windows Copilot: The first command disables Windows Copilot for all users on the system.
- Bing Chat Eligibility: The third command sets the current user's eligibility for Bing Chat to 0, which may prevent access or functionality.
  These changes will take effect after modifying the registry and may require a restart or re-login to apply fully.

```
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows\WindowsCopilot" /v "TurnOffWindowsCopilot" /t "REG_DWORD" /d "1" /f
reg add "HKCU\Software\Policies\Microsoft\Windows\WindowsCopilot" /v "TurnOffWindowsCopilot" /t "REG_DWORD" /d "0" /f
reg add "HKCU\Software\Microsoft\Windows\Shell\Copilot\BingChat" /v "IsUserEligible" /t "REG_DWORD" /d "0" /f
```

# Remove Widgets

These commands are used for configuration and removal tasks related to a Windows app and taskbar settings:

- Disable Taskbar Data: The first command modifies the registry to disable a specific feature related to taskbar data.
- Uninstall App: The PowerShell command uninstalls the MicrosoftWindows.Client.WebExperience app from the system.
- Deprovision App: The final command deprovisions the same app, ensuring it cannot be installed or reinstalled for any user on the system.

These actions will take effect immediately after execution and may require a restart or re-login to fully apply.

```
reg add "HKCU\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced" /v "TaskbarDa" /t "REG_DWORD" /d "0" /f
PowerShell -ExecutionPolicy Unrestricted -Command "Get-AppxPackage \"MicrosoftWindows.Client.WebExperience\" | Remove-AppxPackage"
reg add "HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Appx\AppxAllUserStore\Deprovisioned\MicrosoftWindows.Client.WebExperience_cw5n1h2txyewy" /f
```
