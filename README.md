# Install-W10-in-QEMU-KVM

#   Schreibe folgende Eigenschaften in die Registry-Datenbank:
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
    
#   sysdm.cpl  >>  Erweitert   >>   Leistung  >>  Einstellungen  -> (x) Für optimale Leistung anpassen
#   Windows + I  >>  Erleichterte Bedienung  >>  Anzeige  ->  Transparenz in Windows anzeigen (aus)
#   Windows + I  >>  Personalisierung  >>  Farbenn  ->  Tranzparenzeffekte (aus) + Farben auf Dunkel stellen
 
