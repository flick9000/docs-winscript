#

# Set As DNS

Each command sets the primary DNS server for the specified interface, and the index=2 commands add a secondary DNS server.

## Google DNS

```
netsh interface ip set dns name="Ethernet" static 8.8.8.8
netsh interface ip add dns name="Ethernet" 8.8.4.4 index=2
```

## Cloudflare DNS

```
netsh interface ip set dns name="Ethernet" static 1.1.1.1
netsh interface ip add dns name="Ethernet" 1.0.0.1 index=2
```

## OpenDNS DNS

```
netsh interface ip set dns name="Ethernet" static 208.67.222.222
netsh interface ip add dns name="Ethernet" 208.67.220.220 index=2
```

## Quad9 DNS

```
netsh interface ip set dns name="Ethernet" static 9.9.9.9
netsh interface ip add dns name="Ethernet" 149.112.112.112 index=2
```

# Clean-up

## Clean Temporary Files

Deletes files from Windows Prefetch, User Temp and Windows Temp folders.

```
del /s /f /q c:\windows\temp\.
del /s /f /q C:\WINDOWS\Prefetch
del /s /f /q %temp%\.
```

## Empty Recycle Bin

This command uses PowerShell to empty the Recycle Bin by iterating through its items and removing them forcefully. It also prints a message indicating which item is being deleted.

```
PowerShell -ExecutionPolicy Unrestricted -Command "$bin = (New-Object -ComObject Shell.Application).NameSpace(10); $bin.items() | ForEach {; Write-Host "^""Deleting $($_.Name) from Recycle Bin"^""; Remove-Item $_.Path -Recurse -Force; }"

```

# Misc Options

## Enable Dark Mode

Disables Light Mode for System and Apps.

```
reg add "HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Themes\Personalize" /v "AppsUseLightTheme" /t REG_DWORD /d 0 /f
reg add "HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Themes\Personalize" /v "SystemUsesLightTheme" /t REG_DWORD /d 0 /f
```

## Show File Extensions

Shows file extensions by default.

```
reg add "HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Advanced" /v "HideFileExt" /t REG_DWORD /d 0 /f
```

## Disable Sticky Keys

Disables sticky keys.

```
reg add "HKCU\Control Panel\Accessibility\StickyKeys" /v "Flags" /t REG_SZ /d "58" /f
```

## Disable Taskbar Widgets

Disables taskbar widgets.

```
reg add "HKCU\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced" /v "TaskbarDa" /t REG_DWORD /d 0 /f
```

## Disable Numlock on startup

Disables Numlock on startup

```
reg add "HKCU\Control Panel\Keyboard" /v "InitialKeyboardIndicators" /t REG_SZ /d "0" /f

```

## Disable Snap Flyout

Disables Snap Assist Flyout

```
reg add "HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Advanced" /v "EnableSnapAssistFlyout" /t REG_DWORD /d 0 /f
```

## Add Ultimate Performance

> This script only creates the power scheme, you need to acticate it manually from the Control Panel.

This command creates a copy of the specified power scheme, identified by its GUID (e9a42b02-d5df-448d-aa00-03f14749eb61).

```
powercfg -duplicatescheme e9a42b02-d5df-448d-aa00-03f14749eb61
```

## Set Services to Manual

Sets these services to a specific start instruction.

- AJRouter: Disabled
- ALG: Demand
- AppIDSvc: Demand
- AppMgmt: Demand
- AppReadiness: Demand
- AppVClient: Disabled
- AppXSvc: Demand
- Appinfo: Demand
- AssignedAccessManagerSvc: Disabled
- AxInstSV: Demand
- BDESVC: Demand
- BITS: AutomaticDelayedStart
- BTAGService: Demand
- BcastDVRUserService: Demand
- BluetoothUserService: Demand
- Browser: Demand
- CDPSvc: Demand
- COMSysApp: Demand
- CaptureService: Demand
- CertPropSvc: Demand
- ClipSVC: Demand
- ConsentUxUserSvc: Demand
- CredentialEnrollmentManagerUserSvc: Demand
- CscService: Demand
- DcpSvc: Demand
- DevQueryBroker: Demand
- DeviceAssociationBrokerSvc: Demand
- DeviceAssociationService: Demand
- DeviceInstall: Demand
- DevicePickerUserSvc: Demand
- DevicesFlowUserSvc: Demand
- DiagTrack: Disabled
- DialogBlockingService: Disabled
- DisplayEnhancementService: Demand
- DmEnrollmentSvc: Demand
- DoSvc: AutomaticDelayedStart
- DsSvc: Demand
- DsmSvc: Demand
- EFS: Demand
- EapHost: Demand
- EntAppSvc: Demand
- FDResPub: Demand
- Fax: Demand
- FrameServer: Demand
- FrameServerMonitor: Demand
- GraphicsPerfSvc: Demand
- HomeGroupListener: Demand
- HomeGroupProvider: Demand
- HvHost: Demand
- IEEtwCollectorService: Demand
- IKEEXT: Demand
- InstallService: Demand
- InventorySvc: Demand
- IpxlatCfgSvc: Demand
- KtmRm: Demand
- LicenseManager: Demand
- LxpSvc: Demand
- MSDTC: Demand
- MSiSCSI: Demand
- MapsBroker: AutomaticDelayedStart
- McpManagementService: Demand
- MessagingService: Demand
- MicrosoftEdgeElevationService: Demand
- MixedRealityOpenXRSvc: Demand
- MsKeyboardFilter: Demand
- NPSMSvc: Demand
- NaturalAuthentication: Demand
- NcaSvc: Demand
- NcbService: Demand
- NcdAutoSetup: Demand
- NetSetupSvc: Demand
- NetTcpPortSharing: Disabled
- Netman: Demand
- NgcCtnrSvc: Demand
- NgcSvc: Demand
- NlaSvc: Demand
- P9RdrService: Demand
- PNRPAutoReg: Demand
- PNRPsvc: Demand
- PcaSvc: Demand
- PeerDistSvc: Demand
- PenService: Demand
- PerfHost: Demand
- PhoneSvc: Demand
- PimIndexMaintenanceSvc: Demand
- PlugPlay: Demand
- PolicyAgent: Demand
- PrintNotify: Demand
- PrintWorkflowUserSvc: Demand
- PushToInstall: Demand
- QWAVE: Demand
- RasAuto: Demand
- RasMan: Demand
- RemoteAccess: Disabled
- RemoteRegistry: Disabled
- RetailDemo: Demand
- RmSvc: Demand
- RpcLocator: Demand
- SCPolicySvc: Demand
- SCardSvr: Demand
- SDRSVC: Demand
- SEMgrSvc: Demand
- SNMPTRAP: Demand
- SNMPTrap: Demand
- SSDPSRV: Demand
- ScDeviceEnum: Demand
- SecurityHealthService: Demand
- Sense: Demand
- SensorDataService: Demand
- SensorService: Demand
- SensrSvc: Demand
- SessionEnv: Demand
- SharedAccess: Demand
- SharedRealitySvc: Demand
- SmsRouter: Demand
- SstpSvc: Demand
- StateRepository: Demand
- StiSvc: Demand
- StorSvc: Demand
- TabletInputService: Demand
- TapiSrv: Demand
- TextInputManagementService: Demand
- TieringEngineService: Demand
- TimeBroker: Demand
- TimeBrokerSvc: Demand
- TokenBroker: Demand
- TroubleshootingSvc: Demand
- TrustedInstaller: Demand
- UI0Detect: Demand
- UdkUserSvc: Demand
- UevAgentService: Disabled
- UmRdpService: Demand
- UnistoreSvc: Demand
- UserDataSvc: Demand
- UsoSvc: Demand
- VSS: Demand
- VacSvc: Demand
- W32Time: Demand
- WEPHOSTSVC: Demand
- WFDSConMgrSvc: Demand
- WMPNetworkSvc: Demand
- WManSvc: Demand
- WPDBusEnum: Demand
- WSService: Demand
- WaaSMedicSvc: Demand
- WalletService: Demand
- WarpJITSvc: Demand
- WbioSrvc: Demand
- WcsPlugInService: Demand
- WdNisSvc: Demand
- WdiServiceHost: Demand
- WdiSystemHost: Demand
- WebClient: Demand
- Wecsvc: Demand
- WerSvc: Demand
- WiaRpc: Demand
- WinHttpAutoProxySvc: Demand
- WinRM: Demand
- WpcMonSvc: Demand
- WpnService: Demand
- WwanSvc: Demand
- XblAuthManager: Demand
- XblGameSave: Demand
- XboxGipSvc: Demand
- XboxNetApiSvc: Demand
- autotimesvc: Demand
- bthserv: Demand
- camsvc: Demand
- cbdhsvc: Demand
- cloudidsvc: Demand
- dcsvc: Demand
- defragsvc: Demand
- diagnosticshub.standardcollector.service: Demand
- diagsvc: Demand
- dmwappushservice: Demand
- dot3svc: Demand
- edgeupdate: Demand
- edgeupdatem: Demand
- embeddedmode: Demand
- fdPHost: Demand
- fhsvc: Demand
- hidserv: Demand
- icssvc: Demand
- lfsvc: Demand
- lltdsvc: Demand
- lmhosts: Demand
- msiserver: Demand
- netprofm: Demand
- p2pimsvc: Demand
- p2psvc: Demand
- perceptionsimulation: Demand
- pla: Demand
- seclogon: Demand
- shpamsvc: Disabled
- smphost: Demand
- spectrum: Demand
- sppsvc: AutomaticDelayedStart
- ssh-agent: Disabled
- svsvc: Demand
- swprv: Demand
- tzautoupdate: Disabled
- uhssvc: Disabled
- upnphost: Demand
- vds: Demand
- vm3dservice: Demand
- vmicguestinterface: Demand
- vmicheartbeat: Demand
- vmickvpexchange: Demand
- vmicrdv: Demand
- vmicshutdown: Demand
- vmictimesync: Demand
- vmicvmsession: Demand
- vmicvss: Demand
- vmvss: Demand
- wbengine: Demand
- wcncsvc: Demand
- webthreatdefsvc: Demand
- wercplsupport: Demand
- wisvc: Demand
- wlidsvc: Demand
- wlpasvc: Demand
- wmiApSrv: Demand
- workfolderssvc: Demand

```
sc config AJRouter start=disabled
sc config ALG start=demand
sc config AppIDSvc start=demand
sc config AppMgmt start=demand
sc config AppReadiness start=demand
sc config AppVClient start=disabled
sc config AppXSvc start=demand
sc config Appinfo start=demand
sc config AssignedAccessManagerSvc start=disabled
sc config AxInstSV start=demand
sc config BDESVC start=demand
sc config BITS start=AutomaticDelayedStart
sc config BTAGService start=demand
sc config BcastDVRUserService start=demand
sc config BluetoothUserService start=demand
sc config Browser start=demand
sc config CDPSvc start=demand
sc config COMSysApp start=demand
sc config CaptureService start=demand
sc config CertPropSvc start=demand
sc config ClipSVC start=demand
sc config ConsentUxUserSvc start=demand
sc config CredentialEnrollmentManagerUserSvc start=demand
sc config CscService start=demand
sc config DcpSvc start=demand
sc config DevQueryBroker start=demand
sc config DeviceAssociationBrokerSvc start=demand
sc config DeviceAssociationService start=demand
sc config DeviceInstall start=demand
sc config DevicePickerUserSvc start=demand
sc config DevicesFlowUserSvc start=demand
sc config DiagTrack start=disabled
sc config DialogBlockingService start=disabled
sc config DisplayEnhancementService start=demand
sc config DmEnrollmentSvc start=demand
sc config DoSvc start=AutomaticDelayedStart
sc config DsSvc start=demand
sc config DsmSvc start=demand
sc config EFS start=demand
sc config EapHost start=demand
sc config EntAppSvc start=demand
sc config FDResPub start=demand
sc config Fax start=demand
sc config FrameServer start=demand
sc config FrameServerMonitor start=demand
sc config GraphicsPerfSvc start=demand
sc config HomeGroupListener start=demand
sc config HomeGroupProvider start=demand
sc config HvHost start=demand
sc config IEEtwCollectorService start=demand
sc config IKEEXT start=demand
sc config InstallService start=demand
sc config InventorySvc start=demand
sc config IpxlatCfgSvc start=demand
sc config KtmRm start=demand
sc config LicenseManager start=demand
sc config LxpSvc start=demand
sc config MSDTC start=demand
sc config MSiSCSI start=demand
sc config MapsBroker start=AutomaticDelayedStart
sc config McpManagementService start=demand
sc config MessagingService start=demand
sc config MicrosoftEdgeElevationService start=demand
sc config MixedRealityOpenXRSvc start=demand
sc config MsKeyboardFilter start=demand
sc config NPSMSvc start=demand
sc config NaturalAuthentication start=demand
sc config NcaSvc start=demand
sc config NcbService start=demand
sc config NcdAutoSetup start=demand
sc config NetSetupSvc start=demand
sc config NetTcpPortSharing start=disabled
sc config Netman start=demand
sc config NgcCtnrSvc start=demand
sc config NgcSvc start=demand
sc config NlaSvc start=demand
sc config P9RdrService start=demand
sc config PNRPAutoReg start=demand
sc config PNRPsvc start=demand
sc config PcaSvc start=demand
sc config PeerDistSvc start=demand
sc config PenService start=demand
sc config PerfHost start=demand
sc config PhoneSvc start=demand
sc config PimIndexMaintenanceSvc start=demand
sc config PlugPlay start=demand
sc config PolicyAgent start=demand
sc config PrintNotify start=demand
sc config PrintWorkflowUserSvc start=demand
sc config PushToInstall start=demand
sc config QWAVE start=demand
sc config RasAuto start=demand
sc config RasMan start=demand
sc config RemoteAccess start=disabled
sc config RemoteRegistry start=disabled
sc config RetailDemo start=demand
sc config RmSvc start=demand
sc config RpcLocator start=demand
sc config SCPolicySvc start=demand
sc config SCardSvr start=demand
sc config SDRSVC start=demand
sc config SEMgrSvc start=demand
sc config SNMPTRAP start=demand
sc config SNMPTrap start=demand
sc config SSDPSRV start=demand
sc config ScDeviceEnum start=demand
sc config SecurityHealthService start=demand
sc config Sense start=demand
sc config SensorDataService start=demand
sc config SensorService start=demand
sc config SensrSvc start=demand
sc config SessionEnv start=demand
sc config SharedAccess start=demand
sc config SharedRealitySvc start=demand
sc config SmsRouter start=demand
sc config SstpSvc start=demand
sc config StateRepository start=demand
sc config StiSvc start=demand
sc config StorSvc start=demand
sc config TabletInputService start=demand
sc config TapiSrv start=demand
sc config TextInputManagementService start=demand
sc config TieringEngineService start=demand
sc config TimeBroker start=demand
sc config TimeBrokerSvc start=demand
sc config TokenBroker start=demand
sc config TroubleshootingSvc start=demand
sc config TrustedInstaller start=demand
sc config UI0Detect start=demand
sc config UdkUserSvc start=demand
sc config UevAgentService start=disabled
sc config UmRdpService start=demand
sc config UnistoreSvc start=demand
sc config UserDataSvc start=demand
sc config UsoSvc start=demand
sc config VSS start=demand
sc config VacSvc start=demand
sc config W32Time start=demand
sc config WEPHOSTSVC start=demand
sc config WFDSConMgrSvc start=demand
sc config WMPNetworkSvc start=demand
sc config WManSvc start=demand
sc config WPDBusEnum start=demand
sc config WSService start=demand
sc config WaaSMedicSvc start=demand
sc config WalletService start=demand
sc config WarpJITSvc start=demand
sc config WbioSrvc start=demand
sc config WcsPlugInService start=demand
sc config WdNisSvc start=demand
sc config WdiServiceHost start=demand
sc config WdiSystemHost start=demand
sc config WebClient start=demand
sc config Wecsvc start=demand
sc config WerSvc start=demand
sc config WiaRpc start=demand
sc config WinHttpAutoProxySvc start=demand
sc config WinRM start=demand
sc config WpcMonSvc start=demand
sc config WpnService start=demand
sc config WwanSvc start=demand
sc config XblAuthManager start=demand
sc config XblGameSave start=demand
sc config XboxGipSvc start=demand
sc config XboxNetApiSvc start=demand
sc config autotimesvc start=demand
sc config bthserv start=demand
sc config camsvc start=demand
sc config cbdhsvc start=demand
sc config cloudidsvc start=demand
sc config dcsvc start=demand
sc config defragsvc start=demand
sc config diagnosticshub.standardcollector.service start=demand
sc config diagsvc start=demand
sc config dmwappushservice start=demand
sc config dot3svc start=demand
sc config edgeupdate start=demand
sc config edgeupdatem start=demand
sc config embeddedmode start=demand
sc config fdPHost start=demand
sc config fhsvc start=demand
sc config hidserv start=demand
sc config icssvc start=demand
sc config lfsvc start=demand
sc config lltdsvc start=demand
sc config lmhosts start=demand
sc config msiserver start=demand
sc config netprofm start=demand
sc config p2pimsvc start=demand
sc config p2psvc start=demand
sc config perceptionsimulation start=demand
sc config pla start=demand
sc config seclogon start=demand
sc config shpamsvc start=disabled
sc config smphost start=demand
sc config spectrum start=demand
sc config sppsvc start=AutomaticDelayedStart
sc config ssh-agent start=disabled
sc config svsvc start=demand
sc config swprv start=demand
sc config tzautoupdate start=disabled
sc config uhssvc start=disabled
sc config upnphost start=demand
sc config vds start=demand
sc config vm3dservice start=demand
sc config vmicguestinterface start=demand
sc config vmicheartbeat start=demand
sc config vmickvpexchange start=demand
sc config vmicrdv start=demand
sc config vmicshutdown start=demand
sc config vmictimesync start=demand
sc config vmicvmsession start=demand
sc config vmicvss start=demand
sc config vmvss start=demand
sc config wbengine start=demand
sc config wcncsvc start=demand
sc config webthreatdefsvc start=demand
sc config wercplsupport start=demand
sc config wisvc start=demand
sc config wlidsvc start=demand
sc config wlpasvc start=demand
sc config wmiApSrv start=demand
sc config workfolderssvc start=demand
sc config wscsvc start=AutomaticDelayedStart
sc config wuauserv start=demand
sc config wudfsvc start=demand
```

## Disable Hibernation

Disables hibernation, not needed for desktop computers.

```
powercfg.exe /hibernate off
```

## Disable Prefetch

Prefetch files are temporary files containing information about application programs, which helps in the quicker loading of programs.

```
sc stop sysmain
sc config sysmain start=disabled
```
