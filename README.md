<h1 align="center">Zumbyte - ServerDesk</h1>
<p align="center">Dateien. Server. Verbindungen. Ein gemeinsamer Arbeitsbereich.</p>
<p align="center"><a href="https://github.com/ZUMBYTE-AppSolution/serverdesk-release/releases">Windows-Installer & portable Ausgabe</a> · <a href="https://github.com/ZUMBYTE-AppSolution/serverdesk-release/wiki">Dokumentation</a> · <a href="https://github.com/ZUMBYTE-AppSolution/serverdesk-release/issues">Fehler melden</a></p>
<p align="center"><img src="https://img.shields.io/badge/Windows-10%20%2F%2011-7152bd?style=flat-square" alt="Windows 10 / 11"> <img src="https://img.shields.io/github/v/release/ZUMBYTE-AppSolution/serverdesk?include_prereleases&amp;style=flat-square&amp;label=Beta" alt="Beta-Version"></p>

ServerDesk verbindet einen Explorer mit zwei Dateibereichen, einen Zugangstresor, einen Codeeditor und eingebettete Remotesitzungen. Die native Oberfläche folgt dem ursprünglichen Zumbyte-Mockup: kompakte Tabs und Pfadleisten, farbige Favoriten sowie Dark und Light Mode.

Die Quellcode-Entwicklung erfolgt privat; Downloads erscheinen im öffentlichen Release-Repository. Dies ist eine Windows-x64-Beta. Die gemeinsame Avalonia-Codebasis und das portable Tresorformat bereiten macOS vor; ein geprüftes macOS-Paket und eine macOS-RDP-Integration sind noch offen.

## ✨ Funktionen

- **Zwei Dateibereiche:** mehrere Tabs pro Seite, Adress-Breadcrumbs, Verzeichnissuche, Sortierung und verschiebbare, ein- und ausblendbare Spalten.
- **Arbeitsbereiche:** eigene Verbindungen, Zugangsdaten und unabhängige Masterkeys; getrennte Tabs, Pfade und Fensterpositionen. Passwortabfrage beim Start und Wechsel, optional auf diesem Gerät speichern.
- **Freie Tabs:** Explorer-, Editor-, SSH-, RDP- und VNC-Tabs lassen sich als Desktopfenster abkoppeln und wieder andocken. Der vorhandene Inhalt bleibt erhalten. Der Hinweis dazu steht in der Statusleiste.
- **Dateiaktionen:** Kopieren, Ausschneiden, Einfügen und Umbenennen per Tastatur und Kontextmenü; Löschen mit Rückfrage, unter Windows lokal standardmäßig in den Papierkorb.
- **Server & Computer:** Profile für SFTP, SSH, FTP, FTPS, SMB, HTTPS-WebDAV, RDP und VNC; optional einzeln beim Start öffnen.
- **Verbindungsstatus:** Aufklappbare Hostgruppen in der Seitenleiste, Protokolle darunter. Statuspunkte rechtsbündig und mittig in den Listen und Sitzungsleisten; Tabköpfe bleiben ohne Punkt. Explorer zeigt nach erfolgreicher Verbindung eine Aktion zum Trennen.
- **Terminal & Transfers:** untere Tabs für eine interaktive lokale PowerShell, die Transferliste mit Bytefortschritt und Geschwindigkeit sowie die Aktivität. SSH öffnet eine dauerhafte PTY-Shell mit ANSI-Farben im eigenen Verbindungstab. Terminal-Schriftgröße, Zwischenablage per Strg+C/V und Kontextmenü sind einstellbar. Schließen des SSH-Tabs trennt diese Sitzung; eine separate SFTP-Verbindung bleibt erhalten.
- **Remote Desktop:** RDP unter Windows über Microsofts natives Steuerelement; VNC mit Bildschirm, Maus und Tastatur direkt im Tab. Die Übersicht zeigt RDP/VNC; SSH bleibt unter Server & Computer.
- **LAN-/WLAN-Suche:** Beim Anlegen eines Profils Adapter und lokalen IPv4-Bereich wählen. RDP-/VNC-Dienste anhand ihrer Protokollantwort erkennen und Host, Typ und Port vorfüllen; vorhandene Profile werden gekennzeichnet. Fortschritt und Abbrechen, ohne Anmeldung während der Suche.
- **Zugangstresor:** Private Schlüssel über **Durchsuchen…** auswählen. Jeder Arbeitsbereich besitzt eine passwortgeschützte `.zmasterkey`-Datei und einen eigenen verschlüsselten `.zstorage`-Speicher für Zugänge und Verbindungen. Import, Export, frei wählbarer Speicherort und laufende Änderungsüberwachung für synchronisierte Cloudordner.
- **Netzwerk & Cloud:** Cloudspeicher erscheinen ausschließlich unter **Speicher**. WebDAV/Nextcloud und SMB werden automatisch zugeordnet; SFTP-/FTP-/FTPS-Speicher lassen sich im Profil einordnen. Lokale Sync-Ordner einschließlich iCloud Drive bleiben erreichbar.
- **Codeeditor:** eigene Tabs, einstellbare Schriftgröße, Syntaxfarben, Zeilennummern, Suchen/Ersetzen, Syntaxprüfung und wahlweise externer Editor. Serverdateien können beim Speichern automatisch zurückgeladen werden; Konflikte stoppen den Upload.
- **Archive:** ZIP, TAR, TAR.GZ und GZ erstellen; ZIP, TAR, TAR.GZ/TGZ und GZ lokal aus dem Kontextmenü entpacken.
- **SFTP-Rechte:** rwx, Oktalwerte, Sonderbits, Owner und Gruppe; Servernamen oder numerische UID/GID, optional rekursiv mit Vorschau und Bestätigung.
- **Updates:** Release/Beta-Auswahl, GitHub-Versionsprüfung, Changelog, Installation mit Neustart und gezielte Rückkehr zu verfügbaren älteren Paketen.

## 📦 Installation

Öffne die [GitHub Releases](https://github.com/ZUMBYTE-AppSolution/serverdesk-release/releases) und wähle die aktuelle Beta.

**Installer:** die `Setup.exe` herunterladen und ausführen. Das Paket enthält die benötigten .NET-Laufzeiten; Visual Studio und ein separat installiertes SDK sind nicht erforderlich. Integrierte Updates und Rollbacks benötigen die installierte Ausgabe.

**Portabel:** die `Portable.zip` vollständig in einen eigenen Ordner entpacken und `Zumbyte - ServerDesk.exe` im Hauptordner starten. Die Unterordner `current` und `current/rdp` mit entpacken. Die portable Ausgabe prüft verfügbare Versionen; zum Versionswechsel ein neues Paket verwenden. Einstellungen liegen weiterhin im Benutzerprofil.

Installer und Binärdateien sind derzeit **nicht mit einem Herausgeberzertifikat signiert**. Prüfsummen stehen im jeweiligen Release unter `SHA256SUMS.txt`.

## ⌨️ Schnellstart

1. Beim ersten Start für jeden Arbeitsbereich ein Masterpasswort mit mindestens 12 Zeichen festlegen. Vorhandene Profile werden einmalig übernommen. Danach links und rechts ein Verzeichnis öffnen. `Alt+D` oder `Strg+L` bearbeitet den Pfad.
2. Unter **Server & Computer** ein Profil anlegen und bei Bedarf einen Zugang aus dem Tresor zuweisen.
3. Einen Tab ziehen, um ihn abzukoppeln. Den Tabkopf des Zusatzfensters auf einen Dateibereich zurückziehen oder **Zurück in die App** wählen.
4. Unter **Einstellungen** Arbeitsbereiche, Autostart, externe Editoren und automatischen Rückupload konfigurieren.

| Tastatur | Aktion |
| --- | --- |
| `Strg+C / X / V` | Dateien kopieren / ausschneiden / einfügen |
| `Strg+A` | Alle Dateien im aktiven Bereich auswählen |
| `F2` / `Entf` | Umbenennen / Löschen mit Rückfrage |
| `Umschalt+Entf` | Endgültiges Löschen mit Rückfrage |
| `Alt+D`, `Strg+L`, `F4` | Pfad bearbeiten |
| `Strg+F` / `F5` / `F7` | Suchen / Aktualisieren / Neuer Ordner |
| `Strg+S` / `Strg+G` | Editor speichern / zur Zeile springen |
| `Strg+Mausrad` | Editor-/Terminal-Schriftgröße ändern und speichern |
| `Strg+C / V` im Terminal | Auswahl kopieren / Text einfügen; Strg+C ohne Auswahl unterbricht |
| `Strg+K` / `Strg+N` | Verbindung / Arbeitsbereich anlegen |

## 🔄 Updates & Rollback

Unter **Updates & Versionen** zwischen **Release** und **Beta** wählen. Release enthält stabile Veröffentlichungen; Beta enthält Vorabversionen. Ein leerer Kanal wechselt nicht automatisch zum anderen Kanal.

Vor der Installation zeigt ServerDesk Version und Changelog. Das Paket muss zum offiziellen Repository, Tag, Kanal, App-Namen und zur SHA256-Prüfsumme des Releasefeeds passen. Beim Neustart werden ungespeicherte Editorinhalte abgefragt, die Konfiguration gesichert und Remotesitzungen getrennt. Ein Rollback ändert die Anwendungsversion; persönliche Dateien und Tresore werden nicht auf einen früheren Stand zurückgesetzt. Nach der Masterkey-Migration ist ein integrierter Rückwechsel auf Versionen vor Beta 6 gesperrt, da diese das neue Arbeitsbereichsformat nicht unterstützen.

## 🔐 Daten & Grenzen der Beta

Die lokale Konfiguration liegt unter `%LOCALAPPDATA%\Zumbyte\ServerDesk`. Ab Beta 6 sind Verbindungsprofile und Zugangsdaten gemeinsam pro Arbeitsbereich verschlüsselt. Ein zufälliger, unabhängiger 256-Bit-Schlüssel verschlüsselt den Speicher mit AES-256-GCM. Das Masterpasswort schützt diesen Schlüssel mittels PBKDF2-SHA256 mit 600.000 Iterationen und AES-256-GCM. **Passwort auf diesem Gerät speichern** ist standardmäßig aus und hinterlegt unter Windows eine DPAPI-geschützte Gerätefreigabe für das aktuelle Benutzerkonto. Das Passwort selbst wird nicht gespeichert; die Gerätefreigabe gehört nicht in den Cloudordner.

Bei der einmaligen Migration bleiben Profilkennungen erhalten. Die bisherigen gemeinsam verwendeten Profile werden zur Bestandserhaltung in jeden vorhandenen Arbeitsbereich übernommen; danach sind sie unabhängig. Die bisherige Konfiguration wird zunächst verschlüsselt gesichert. Alte externe Backups und ursprüngliche SSH-Schlüsseldateien bleiben bestehen. Tabs, Pfade, Aktivitätsprotokolle, Editorcache und heruntergeladene Dateien liegen weiterhin außerhalb dieser Verschlüsselung.

Für mehrere Systeme dasselbe Dateipaar in einen synchronisierten Ordner legen und auf jedem System importieren. Die App überwacht Änderungen per Dateiwächter und regelmäßiger Prüfung. Aktuelle Daten werden im sicheren Leerlauf geladen; offene Dialoge, Bearbeitungen und Transfers führen zu einem Hinweis. Veraltete Schreibversuche werden blockiert. `.bak` und `.history` enthalten verschlüsselte Sicherungen. Cloudanbieter können parallele Änderungen als Konfliktkopien speichern: Diese müssen getrennt geprüft werden; eine automatische Zusammenführung oder atomare Transaktion zwischen Rechnern wird nicht garantiert. Das Dateiformat ist plattformunabhängig; ein vollständiger Windows/macOS-Synctest und ein Mac-Paket stehen noch aus.

Das Terminal verwendet eine verwaltete VT-Emulation; die Kompatibilität komplexer Vollbildprogramme hängt von deren Anforderungen ab. Transfers lassen sich noch nicht pausieren oder wiederaufnehmen. Archive werden lokal verarbeitet. Direkte OAuth-Cloudanbieter und S3 sind noch nicht integriert. Syntaxfarben decken mehr Sprachen ab als die verfügbaren Syntaxparser. Details und weitere Grenzen stehen im [Wiki](https://github.com/ZUMBYTE-AppSolution/serverdesk-release/wiki/Beta-Grenzen).

## 🔐 Lizenz und Quellcode

ServerDesk ist proprietäre Software. Der Quellcode wird privat verwaltet. Ohne ausdrückliche schriftliche Erlaubnis von Zumbyte - AppSolution sind Nutzung, Vervielfältigung, Weitergabe, kommerzielle Verwertung und die Erstellung abgeleiteter Tools aus dem Quellcode untersagt. Das gilt auch für angepasste Fassungen und geschützte Codeschnipsel. Drittanbieterrechte und zwingende gesetzliche sowie GitHub-Plattformrechte bleiben unberührt. Einzelheiten: [LICENSE](LICENSE).

Releases werden ausschließlich lokal erstellt und geprüft. Das öffentliche Repository enthält nur README, Lizenz, fertige Releasepakete und das Benutzer-Wiki. Es enthält keine Bauanleitungen, Quelltexte oder GitHub-Buildworkflows.

## 💬 Support & Rechtliches

**Zumbyte - AppSolution | [www.zumbyte.de](https://www.zumbyte.de/)**  
© 2026 Zumbyte - AppSolution

[Support](https://www.zumbyte.de/support/) · [Datenschutz](https://www.zumbyte.de/datenschutz/) · [Impressum](https://www.zumbyte.de/impressum/) · [GitHub Issues](https://github.com/ZUMBYTE-AppSolution/serverdesk-release/issues)

Das App-Icon wurde von Zumbyte geliefert. Die übrigen Symbole stammen aus [Iconify](https://iconify.design/) / Microsoft Fluent UI System Icons (MIT). Die Lizenzen und Herkunftsnachweise aller mitgelieferten Drittkomponenten stehen im Paket unter `licenses`, einschließlich des angepassten VNC-Adapters.

---
<p align="center">Zumbyte - ServerDesk · Entwickelt von Zumbyte - AppSolution</p>
