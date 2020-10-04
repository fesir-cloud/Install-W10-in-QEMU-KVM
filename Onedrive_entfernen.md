# Schritt 1: OneDrive-Symbol im Explorer entfernen
Drücken Sie gleichzeitig auf die Tasten [Windows] und [R], sodass sich der Befehl "Ausführen" öffnet.

Geben Sie hier "regedit" ein und bestätigen Sie mit "OK". Anschließend startet der Registrierungs-Editor.

Navigieren Sie links zum folgenden Pfad: 

    HKEY_CLASSES_ROOT\CLSID\{018D5C66-4533-4307-9B53-224DE2ED1FE6}

Klicken Sie nun auf der rechten Seite doppelt auf den Wert 

    "System.IsPinnedToNameSpaceTree".

Ändern Sie dort den Wert von 1 auf 0 und schließen Sie das Fenster mit dem Button 

    "OK".

Somit ist OneDrive im Explorer ausgeblendet. Im nächsten Schritt können Sie die Software zusätzlich deinstallieren.


# Schritt 2: OneDrive unter Windows 10 deinstallieren

Hinweis: Die folgende Anleitung lässt sich leider nur mit der Pro-Version von Windows 10 durchführen. Nutzen Sie die Home-Version, können Sie lediglich den Start von OneDrive deaktivieren.

Drücken Sie gleichzeitig auf die Tasten 

    [Windows] und [R], 
sodass sich der Befehl "Ausführen" öffnet.

Geben Sie hier "gpedit.msc" ein und bestätigt Sie mit "OK". Anschließend startet der Editor für lokale Gruppenrichtlinien.

Navigieren Sie links nun zum folgenden Pfad: Computerkonfiguration, Administrative Vorlagen, Windows-Komponenten, OneDrive.

Rechts finden Sie anschließend die Einstellung "Verwendung von OneDrive für die Datenspeicherung verhindern". Öffnen Sie diese mit einem Doppelklick.

Wählen Sie hier die Option "Aktiviert" aus und schließen Sie das Fenster wieder über den Button "OK".

Schließen Sie das Fenster und drücken Sie gleichzeitig auf die Tasten [Windows] und [X].

Unten links im Bild erscheint ein Kontextmenü. Wählen Sie hier die Option "Eingabeaufforderung (Administrator)".

Geben Sie hier den Befehl "taskkill /f /im OneDrive.exe" ein und bestätigen Sie ihn mit der "Enter"-Taste.

Geben Sie anschließend auch den zweiten Befehl ein. Je nach 32-Bit oder 64-Bit System benötigen Sie den passenden Befehl.

64-Bit: %SystemRoot%\SysWOW64\OneDriveSetup.exe /uninstall

32-Bit: %SystemRoot%\System32\OneDriveSetup.exe /uninstall

Bestätigen Sie auch den zweiten Befehl mit der [Enter]-Taste und schließen Sie das Fenster. OneDrive wurde nun erfolgreich deinstalliert.
