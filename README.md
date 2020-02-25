# Install-W10-in-QEMU-KVM

#   1.  Schreibe folgende Eigenschaften in die Registry-Datenbank:
#   (https://www.askvg.com/collection-of-registry-tweaks-for-windows-7/)  
    Windows Registry Editor Version 5.00

    [HKEY_CLASSES_ROOT\AllFilesystemObjects\shellex\ContextMenuHandlers\Copy To]
    @="{C2FBB630-2971-11D1-A18C-00C04FD75D13}"

    [HKEY_CLASSES_ROOT\AllFilesystemObjects\shellex\ContextMenuHandlers\Move To]
    @="{C2FBB631-2971-11D1-A18C-00C04FD75D13}"

    [HKEY_CURRENT_USER\Control Panel\Desktop]
    "AutoEndTasks"="1"
    "HungAppTimeout"="1000"
    "MenuShowDelay"="8"
    "WaitToKillAppTimeout"="2000"
    "LowLevelHooksTimeout"="1000"

    [HKEY_CURRENT_USER\Control Panel\Mouse]
    "MouseHoverTime"="8"

    [HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer]
    "NoLowDiskSpaceChecks"=dword:00000001
    "LinkResolveIgnoreLinkInfo"=dword:00000001
    "NoResolveSearch"=dword:00000001
    "NoResolveTrack"=dword:00000001
    "NoInternetOpenWith"=dword:00000001

    [HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control]
    "WaitToKillServiceTimeout"="2000"
    
#   2.  sysdm.cpl  >>  Erweitert   >>   Leistung  >>  Einstellungen  -> (x) Für optimale Leistung anpassen

#   3.  Windows + I  >>  Erleichterte Bedienung  >>  Anzeige  ->  Transparenz in Windows anzeigen (aus)

#   4.  Windows + I  >>  Personalisierung  >>  Farbenn  ->  Tranzparenzeffekte (aus) + Farben auf Dunkel stellen

#   Windows + E  >>  Ansicht  >> Optionen  ->  /austoben (

#   5.  shell:ChangeRemoveProgramsFolder  >>  Windows-Features aktivieren oder Deaktivieren  ->  Internetexplorer 11 & Media Player deaktivieren

#   6.  services.msc  //Hier könne "überflüssige services auf MANUAL gestellt werden"/"niemals deaktivieren, fals doch wichtiger Systemprozess"  Folgende Liste kann bedenkenlos manualisiert werden:
    
    Connected User Experiences and Telemetry (To turn off Telemetry and Data Collection) (Check this and this)
    Diagnostic Policy Service
    Diagnostic Tracking Service (To turn off Telemetry and Data Collection)
    Distributed Link Tracking Client (If your computer is not connected to any network)
    dmwappushsvc (To turn off Telemetry and Data Collection)
    Downloaded Maps Manager (If you don't use Maps app)
    IP Helper (If you don't use IPv6 connection)
    Program Compatibility Assistant Service
    Print Spooler (If you don't have a printer)
    Remote Registry (You can set it to DISABLED for Security purposes)
    Secondary Logon
    Security Center (Check this)
    TCP/IP NetBIOS Helper (If you are not in a workgroup network)
    Touch Keyboard and Handwriting Panel Service (If you don't want to use touch keyboard and handwriting features)
    Windows Defender Service (If you don't use Windows Defender program)
    Windows Error Reporting Service
    Windows Image Acquisition (WIA) (If you don't have a scanner)
    Windows Search (If you don't use Windows Search feature frequently) (Check this)
#

#   

    Nützliche shellcommandos:
    
    shell:common administrative tools
    shell:printersfolder
    shell:printhood
    shell:ChangeRemoveProgramsFolder
    shell:CryptoKeys
    shell:DpapiKeys
    shell:ConflictFolder
    shell:Device Metadata Store
    shell:Fonts
   
#   

    Nützliche .msc & .cpl & .exe
    
    sysdm.cpl
    printmanagement.msc
    mstsc.msc
    gpedit.msc
    regedit
