<p align="center"><img src="https://raw.githubusercontent.com/ZUMBYTE-AppSolution/serverdesk-release/main/assets/app-icon.png" width="112" height="112" alt="Zumbyte - ServerDesk"></p>
<h1 align="center">Zumbyte - ServerDesk</h1>
<p align="center">Dateien, Server und Cloudspeicher. Alles an einem Ort.</p>
<p align="center"><a href="https://github.com/ZUMBYTE-AppSolution/serverdesk-release/releases">Herunterladen</a> · <a href="https://github.com/ZUMBYTE-AppSolution/serverdesk-release/wiki">Benutzerhandbuch</a> · <a href="https://www.zumbyte.de/support/">Support</a></p>
<p align="center"><img src="https://img.shields.io/badge/Windows-10%20%2F%2011-7152bd?style=flat-square" alt="Windows 10 / 11"> <img src="https://img.shields.io/github/v/release/ZUMBYTE-AppSolution/serverdesk-release?include_prereleases&amp;style=flat-square&amp;label=Beta" alt="Aktuelle Beta"></p>

**Zumbyte - ServerDesk** ist dein zentraler Arbeitsplatz für lokale Dateien, Server, Remote-Desktops und Cloudspeicher. Zwei Dateibereiche, flexible Tabs und ein integrierter Zugangstresor helfen dir, auch mit vielen Systemen den Überblick zu behalten. Ob Dateien übertragen, per SSH arbeiten oder Konfigurationen bearbeiten: Deine Werkzeuge bleiben zusammen.

Erhältlich als **Windows-x64-Beta** mit Installer oder als portable Ausgabe. Oberfläche auf Deutsch und Englisch, mit Dark und Light Mode.

## 🖼️ Einblicke

![ServerDesk: zwei Dateibereiche, Serververbindungen und Transfers](https://raw.githubusercontent.com/ZUMBYTE-AppSolution/serverdesk-release/main/assets/screenshots/explorer-dark.png)

| Light Mode | Eigenständiger Editor |
| --- | --- |
| ![Explorer im Light Mode](https://raw.githubusercontent.com/ZUMBYTE-AppSolution/serverdesk-release/main/assets/screenshots/explorer-light.png) | ![Editor mit Dateitabs und Syntaxfarben](https://raw.githubusercontent.com/ZUMBYTE-AppSolution/serverdesk-release/main/assets/screenshots/editor-dark.png) |

| Server & Computer | Zugangstresor |
| --- | --- |
| ![Verbindungen und Hostgruppen](https://raw.githubusercontent.com/ZUMBYTE-AppSolution/serverdesk-release/main/assets/screenshots/connections-dark.png) | ![Zugangstresor](https://raw.githubusercontent.com/ZUMBYTE-AppSolution/serverdesk-release/main/assets/screenshots/vault-dark.png) |

| Terminal | Auto-Lock |
| --- | --- |
| ![Integriertes Terminal](https://raw.githubusercontent.com/ZUMBYTE-AppSolution/serverdesk-release/main/assets/screenshots/terminal-dark.png) | ![Gesperrter Arbeitsbereich](https://raw.githubusercontent.com/ZUMBYTE-AppSolution/serverdesk-release/main/assets/screenshots/auto-lock-dark.png) |

| Cloudspeicher | Datenträger & Netzlaufwerke |
| --- | --- |
| ![Cloudkonten verwalten](https://raw.githubusercontent.com/ZUMBYTE-AppSolution/serverdesk-release/main/assets/screenshots/cloud-dark.png) | ![Speicherübersicht mit Laufwerksbelegung](https://raw.githubusercontent.com/ZUMBYTE-AppSolution/serverdesk-release/main/assets/screenshots/storage-dark.png) |

Die Screenshots zeigen ServerDesk mit Beispieldaten. Klicke auf ein Bild für die volle Auflösung.

## ✨ Dein Arbeitsplatz für Dateien und Systeme

| Bereich | Das bietet dir ServerDesk |
| --- | --- |
| **Dateimanager** | Zwei Dateibereiche mit mehreren Tabs, Pfadleisten, Suche, farbigen Favoriten und anpassbaren Spalten. Sortierung, Erstelldatum und serverabhängige Rechte, Owner und Gruppe. |
| **Verbindungen** | SSH, SFTP, FTP, FTPS, HTTPS-WebDAV, SMB, RDP und VNC. Profile desselben Hosts gruppieren, Status erkennen und mehrere Verbindungen gemeinsam öffnen. |
| **Flexible Fenster** | Tabs herausziehen und wieder andocken, zusätzliche App-Fenster öffnen und Sidebar sowie unteren Arbeitsbereich anpassen. Fensterpositionen und Größen bleiben gespeichert. |
| **Arbeitsbereiche** | Eigene Verbindungen und Zugangsdaten pro Arbeitsbereich, jeweils mit eigenem Masterkey und Passwort. Berufliche und private Systeme getrennt verwalten. |
| **Remote Desktop** | RDP und VNC direkt in Verbindungstabs verwenden. Im lokalen LAN oder WLAN nach passenden Diensten suchen und gefundene Systeme als Profile übernehmen. |
| **Terminal** | Lokale PowerShell und SSH-Sitzungen mit Zwischenablage, Schriftwahl und Größen-Dropdown. Beim Schließen eines SSH-Tabs wird dessen Verbindung beendet. |

### Dateien direkt ans Ziel übertragen

Ziehe Dateien und Ordner zwischen Dateibereichen oder App-Fenstern – oder nutze **Strg+C / Strg+X / Strg+V**. Downloads beginnen nach der Zielwahl und schreiben direkt in den gewählten Ordner. Auch beim Ablegen im Windows-Explorer oder auf dem Desktop werden die Daten ohne vollständigen TEMP-Download übergeben. Server-zu-Server-Kopien werden als Stream weitergeleitet.

- Aufklappbare Ordnertransfers mit Gesamtgröße, Fortschritt, Geschwindigkeit und geschätzter Restzeit.
- Dateien oder ganze Ordner pausieren, fortsetzen oder stoppen; optionaler dezenter Ton nach einem abgeschlossenen Download.
- Unvollständige Dateien im Zielordner unter einem gekennzeichneten Namen; fertige Dateien werden nach erfolgreichem Abschluss freigegeben.
- Vorhandene Dateien werden nicht ungefragt überschrieben. Beim Ausschneiden über verschiedene Systeme hinweg bleibt die Quelle bis zur erfolgreichen Übertragung und Inhaltsprüfung erhalten.
- In der Transferliste Zielpfade ansehen, kopieren und lokale Zielordner öffnen.

ZIP, TAR, TAR.GZ und GZ lassen sich lokal über das Kontextmenü erstellen beziehungsweise entpacken. SFTP-Dateirechte einschließlich Owner und Gruppe können abhängig von den Serverberechtigungen bearbeitet werden.

### Cloud und Speicher übersichtlich verwalten

Unter **Speicher** findest du Datenträger mit Speicherbelegung, Netzlaufwerke und Cloudkonten in getrennten, einklappbaren Gruppen.

| Anbieter / Zugang | Anmeldung |
| --- | --- |
| OneDrive, Google Drive, Dropbox | Browser-Anmeldung mit OAuth und den Sicherheitsabfragen deines Kontos |
| iCloud Drive | Apple Account, Passwort und Zwei-Faktor-Bestätigung |
| Nextcloud | Browser-Freigabe einschließlich unterstützter 2FA-/SSO-Verfahren |
| WebDAV | HTTPS-Adresse und Zugangsdaten |
| Lokale Sync-Ordner | Vorhandene Ordner nutzen; gefundenes iCloud Drive erst nach deiner Zustimmung |

Die Anbieterfreigabe für OneDrive, Google Drive und Dropbox erfolgt derzeit über rclone. iCloud-App-Passwörter werden für den direkten Drive-Zugang nicht unterstützt. [Cloudkonten einrichten](https://github.com/ZUMBYTE-AppSolution/serverdesk-release/wiki/Cloud-und-Netzwerk).

### Ein Editor, auch ohne Haupt-App

ServerDesk Editor öffnet lokale Dateien unabhängig von der Haupt-App. Unter Windows stehen kaskadierte Kontextmenüs zum Öffnen und Erstellen von Dateien bereit; die Integration lässt sich abschalten.

Mehrere Dateitabs, Sitzungen, Schriftarten und Größen, **Speichern unter**, Dateiüberwachung, Syntaxfarben und sprachabhängige Syntaxprüfung gehören dazu. Ergänzt werden sie durch Code-Faltung, Regex-Suche und Ersetzen, Suchen in Dateien, Dateivergleich sowie wählbare Kodierung und Zeilenenden. Unterstützte Formate umfassen unter anderem HTML, CSS, JavaScript, TypeScript, PHP, Python, C#, SQL, XML, JSON und YAML.

Serverdateien können beim Speichern automatisch zurückgeladen werden. Änderungen werden auf Konflikte geprüft. Auf Wunsch verwendest du einen externen Editor. [Mehr zum Editor](https://github.com/ZUMBYTE-AppSolution/serverdesk-release/wiki/Editor).

## 🔐 Deine Zugangsdaten schützen

**Jeder Arbeitsbereich hat seinen eigenen verschlüsselten Tresor.** Verbindungsprofile und Zugangsdaten werden mit AES-256-GCM geschützt. Ein unabhängiger 256-Bit-Schlüssel wird über das Masterpasswort mit PBKDF2-SHA256 und 600.000 Iterationen abgesichert.

- **Masterpasswort:** Beim Start und Wechsel entsperren. Die optionale Gerätefreigabe liegt unter Windows DPAPI-geschützt im aktuellen Benutzerkonto; das Passwort selbst wird dabei nicht gespeichert.
- **Auto-Lock:** Eine sechsstellige PIN festlegen und nach 1, 5, 10, 15, 20, 30 oder 60 Minuten Inaktivität sperren lassen. Alle App-Fenster werden gesperrt und Verbindungen getrennt. Die korrekte PIN entsperrt automatisch und stellt zuvor aktive Verbindungen wieder her. Ein Neustart verlangt bei aktivem Auto-Lock immer das Masterpasswort.
- **Sensible Aktionen:** Passwortanzeigen, Verbindungen löschen und Änderungen am Masterkey erfordern eine manuelle Masterpasswort-Freigabe. Diese gilt höchstens zehn Minuten.
- **Eigener Speicherort:** Masterkey und Speicherdatei lokal, auf einem anderen Datenträger oder in einem synchronisierten Cloudordner ablegen. Import, Export, Änderungsüberwachung und Konfliktschutz helfen beim Gerätewechsel. Parallele Änderungen werden nicht automatisch zusammengeführt.
- **Verbindungsvertrauen:** SSH-Hostschlüssel werden geprüft; TLS-Zertifikatsprüfungen bleiben aktiv. Verwende verschlüsselte Protokolle: klassisches FTP und manche VNC-Verfahren schützen den Datenverkehr nicht durchgängig.

Die Tresorverschlüsselung schützt **Verbindungen und Zugangsdaten**. Heruntergeladene Dateien, Editor-Arbeitskopien, Pfade und lokale Protokolle sind dadurch nicht automatisch verschlüsselt. Verwahre Masterpasswort und Sicherungen sicher: Ein vergessenes Masterpasswort kann nicht zurückgesetzt werden. [Sicherheit und Speicherorte](https://github.com/ZUMBYTE-AppSolution/serverdesk-release/wiki/Daten-und-Sicherheit).

## 📦 Installation und erster Start

1. Die gewünschte Ausgabe unter [Releases](https://github.com/ZUMBYTE-AppSolution/serverdesk-release/releases) herunterladen.
2. **Installer:** `Setup.exe` ausführen. **Portabel:** `Portable.zip` vollständig entpacken und `Zumbyte - ServerDesk.exe` im Hauptordner starten.
3. Ein Masterpasswort mit mindestens zwölf Zeichen für deinen Arbeitsbereich festlegen.
4. Links und rechts Verzeichnisse öffnen, Verbindungsprofile anlegen und deine Ansicht einrichten.

Die benötigten Laufzeiten sind enthalten. Für die Nutzung brauchst du keine Entwicklungswerkzeuge. Auch die portable Ausgabe speichert Einstellungen im Windows-Benutzerprofil.

**Aktueller Stand:** Windows 10/11 x64, Beta. Die Dateien sind derzeit nicht mit einem Herausgeberzertifikat signiert; `SHA256SUMS.txt` enthält die Prüfsummen. Eine macOS-Ausgabe ist noch nicht verfügbar. Die Kompatibilität externer Server, Cloudkonten und Anmeldeverfahren hängt vom jeweiligen Anbieter ab. [Versionshinweise und bekannte Einschränkungen](https://github.com/ZUMBYTE-AppSolution/serverdesk-release/wiki/Beta-Grenzen).

## 🔄 Updates und Versionswahl

In der installierten Ausgabe wählst du unter **Updates & Versionen** zwischen **Release** und **Beta**. Vor einem Update werden Version und Changelog angezeigt. Pakete werden über das offizielle GitHub-Release-Repository bezogen und gegen die SHA-256-Prüfsumme des Releasefeeds geprüft.

Verfügbare ältere Pakete können für einen Rückwechsel ausgewählt werden, soweit sie mit den gespeicherten Sicherheits- und Kontodaten kompatibel sind. Ein Rollback setzt persönliche Dateien und Tresore nicht zurück. Portable Ausgaben werden durch ein neues entpacktes Paket aktualisiert. [Updates und Rollback](https://github.com/ZUMBYTE-AppSolution/serverdesk-release/wiki/Updates-und-Rollback).

## 💬 Hilfe, Lizenz und Kontakt

[Benutzerhandbuch](https://github.com/ZUMBYTE-AppSolution/serverdesk-release/wiki) · [Fehler melden](https://github.com/ZUMBYTE-AppSolution/serverdesk-release/issues) · [Support](https://www.zumbyte.de/support/)

ServerDesk ist proprietäre Software von **Zumbyte - AppSolution**. Nutzungsbedingungen und Einschränkungen stehen in der [Lizenz](LICENSE). Der Quellcode ist nicht öffentlich. Die Lizenzen mitgelieferter Komponenten findest du direkt unter **Über ServerDesk → Lizenzen ansehen** und im Downloadpaket. Die Drittkomponenten erlauben kommerzielle Einbindung unter ihren jeweiligen Lizenzbedingungen.

**Zumbyte - AppSolution | [www.zumbyte.de](https://www.zumbyte.de/)**  
© 2026 Zumbyte - AppSolution · [Datenschutz](https://www.zumbyte.de/datenschutz/) · [Impressum](https://www.zumbyte.de/impressum/)
