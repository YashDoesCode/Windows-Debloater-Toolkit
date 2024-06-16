
![Screenshot 2024-06-17 024115](https://github.com/YashDoesCode/Windows-Debloater-Tools/assets/169293586/7d329a98-6bda-46b7-b521-1ae498e4f782)

# Uninstall Widgets

```powershell
winget uninstall –id 9MSSGKG348SP

Get-AppxPackage *WebExperience* | Remove-AppxPackage
```

# Uninstall Bloatware

### Recommended

```powershell
Get-AppxPackage *3dbuilder* | Remove-AppxPackage

Get-AppxPackage *acg* | Remove-AppxPackage

Get-AppxPackage *AV1VideoExtension* | Remove-AppxPackage

Get-AppxPackage *calculator* | Remove-AppxPackage

Get-AppxPackage *communications* | Remove-AppxPackage

Get-AppxPackage *Microsoft.549981C3F5F10* | Remove-AppxPackage

Get-AppxPackage *disney* | Remove-AppxPackage

Get-AppxPackage *dolbyaccess* | Remove-AppxPackage

Get-AppxPackage *WindowsFeedbackHub* | Remove-AppxPackage

Get-AppxPackage *fitbitcoach* | Remove-AppxPackage

Get-AppxPackage *officehub* | Remove-AppxPackage

Get-AppxPackage *getstarted* | Remove-AppxPackage

Get-AppxPackage *zunemusic* | Remove-AppxPackage

Get-AppxPackage *HEIFImageExtension* | Remove-AppxPackage

Get-AppxPackage *GetHelp* | Remove-AppxPackage

Get-AppxPackage *maps* | Remove-AppxPackage

Get-AppxPackage *solitairecollection* | Remove-AppxPackage

Get-AppxPackage *Todos* | Remove-AppxPackage

Get-AppxPackage *Teams* | Remove-AppxPackage

Get-AppxPackage *bingfinance* | Remove-AppxPackage

Get-AppxPackage *zunevideo* | Remove-AppxPackage

Get-AppxPackage *bingnews* | Remove-AppxPackage

Get-AppxPackage *WindowsNotepad* | Remove-AppxPackage

Get-AppxPackage *onenote* | Remove-AppxPackage

Get-AppxPackage *OneDriveSync* | Remove-AppxPackage

Get-AppxPackage *Paint* | Remove-AppxPackage

Get-AppxPackage *people* | Remove-AppxPackage

Get-AppxPackage *phototastic* | Remove-AppxPackage

Get-AppxPackage *picsart* | Remove-AppxPackage

Get-AppxPackage *plex* | Remove-AppxPackage

Get-AppxPackage *PowerAutomateDesktop* | Remove-AppxPackage

Get-AppxPackage *ScreenSketch* | Remove-AppxPackage

Get-AppxPackage *skypeapp* | Remove-AppxPackage

Get-AppxPackage *MicrosoftStickyNotes* | Remove-AppxPackage

Get-AppxPackage *SpotifyMusic* | Remove-AppxPackage

Get-AppxPackage *bingsports* | Remove-AppxPackage

Get-AppxPackage *soundrecorder* | Remove-AppxPackage

Get-AppxPackage *bingweather* | Remove-AppxPackage

Get-AppxPackage *xbox* | Remove-AppxPackage

```

### Advanced (I know what I’m doing)

```powershell
Get-AppxPackage *camera* | Remove-AppxPackage

Get-AppxPackage *WindowsTerminal* | Remove-AppxPackage

Get-AppxPackage *windowsstore* | Remove-AppxPackage

Get-AppxPackage *WebpImageExtension* | Remove-AppxPackage

Get-AppxPackage *alarms* | Remove-AppxPackage

Get-AppxPackage *windowsphone* | Remove-AppxPackage

Get-AppxPackage *YourPhone* | Remove-AppxPackage

Get-AppxPackage *photos* | Remove-AppxPackage

Get-AppxPackage -AllUsers -Name Microsoft.WindowsAlarms | Remove-AppxPackage

Get-AppxPackage *MicrosoftEdge* | Remove-AppxPackage

Get AppxPackage Microsoft.MicrosoftEdge_41.16299.1004.0_netural__8wekyb3d8bbwe｜Remove-AppxPackage
```

### Uninstall All At Once `{Except Microsoft Store}`

```tsx
Get-AppXPackage | where-object {$_.name -notlike '*store*'} | Remove-AppxPackage
```

### Restore All At Once {Even OEM/AOSP Packages}

```powershell
Get-AppxPackage -allusers Microsoft.WindowsStore | Foreach {Add-AppxPackage -DisableDevelopmentMode -Register "$($_.InstallLocation)AppXManifest.xml"
```
