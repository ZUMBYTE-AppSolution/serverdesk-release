# Pluginintegration · Beta 24

## Prüfung vom 11.11.2026

Das unveränderte veröffentlichte Zumbyte-Remote-Plugin **0.2.0-alpha.1** wurde mit den endgültigen Paketen geprüft. Katalog und Pakete benötigen weder GitHub-API noch GitHub-Token.

| Prüfung des entpackten Pakets | Windows x64 | macOS arm64 | macOS x64 unter Rosetta |
| --- | ---: | ---: | ---: |
| Kerntests einschließlich Plugin-Sicherheit | 198 | 196 | 196 |
| Bestehende Oberfläche | 91 | 88 | 88 |
| Arbeitsbereiche / Sicherheit / Erststart / Editor | 18 / 8 / 4 / 4 | 18 / 8 / 4 / 4 | 18 / 8 / 4 / 4 |
| Bestehende Remote-Funktionen | 56 | 53 | 53 |
| Originalplugin mit nativer Eingabe und mehreren Sitzungen | 21 | 21 | 21 |
| Apple-Signatur, Notarisierung und Gatekeeper | entfällt | App und PKG akzeptiert | App und PKG akzeptiert |

Zusätzlich wurde ein freigegebener echter Windows-Rechner über den im Originalpaket enthaltenen Windows-Dienst und einen echten Remote-Server verbunden. Das Livebild läuft direkt im ServerDesk-Tab. Auf beiden Mac-Builds erreichten native Maus- und Tastaturereignisse das Windows-Testfenster: Klickzähler und tatsächlich eingegebener Text wurden am Ziel geprüft. Nach Fokusverlust, Fensterdeaktivierung und Tabwechsel blieb die Zieleingabe unverändert. Eine echte Windows-Sitzung und zwei weitere Tabs auf einem getrennten Protokollserver liefen gleichzeitig; Eingaben wechselten nicht zum anderen Server. Das Schließen eines Tabs erhielt die anderen Sitzungen. Tresorsperre beendete Provider und Windows-Sitzung.

Der endgültige Windows-Build wurde zusätzlich mit echtem Relay-Livebild, unterdrückter Hintergrundeingabe und Sitzungsende bei Tresorsperre geprüft. Positive Windows-Browserereignisse wurden gegen die getrennten Protokollserver geprüft, um bei einem Viewer auf seinem eigenen Zielrechner eine Eingabeschleife zu vermeiden. Die Teststeuerung verwendet native Ereignisse im eigenen Fenster; eine physische Mac-Tastatur wurde damit nicht separat geprüft.

Die Gegenstelle der Protokollprüfung lehnt Eingaben vor der Sitzungsannahme ab. Auch ein vorzeitiges `release` darf eine ausstehende Zustimmung nicht abbrechen. Die Screenshots sind Aufnahmen der laufenden App mit nativen WebView2-/WKWebView-Snapshots. Die echte Windows-Testfläche und die synthetische Gegenprobe sind eindeutig beschriftet.

Grenzen: Die Live-Freigabe gilt für den Windows-Dienst über Relay. Der zusätzliche WebRTC-Verbindungsversuch zum bestehenden Electron-Host blieb beim Verbindungsaufbau und ist nicht abgenommen. Der Prüfserver liefert für WebRTC keine ICE-Server (`iceServers: []`). WebKit beschränkt lokale ICE-Kandidaten ohne Freigabe von Aufnahmegeräten; eine STUN-/TURN-Konfiguration ist deshalb ein möglicher nächster Prüfschritt. Das ist eine Einordnung, kein bestätigter Verbindungsnachweis. [WebKit-Hintergrund](https://webkit.org/blog/7763/a-closer-look-into-webrtc/). macOS x64 wurde unter Rosetta auf Apple Silicon geprüft, nicht auf physischer Intel-Hardware. Linux ist nicht freigegeben. Windows-Binärdateien besitzen kein Authenticode-Zertifikat; die Mac-App und ihre Installer sind mit Developer ID signiert und notarisiert.

Geprüfte Programm-Assemblies:

- Windows x64: `7460be4382d1b2d0ca1c1dfc613f3dd2bf4e592fe60a16e0d8d143fdd6decae5`
- macOS arm64: `c734203b1960574b4ac84d0b8eec5e2879c9635d5bfe065eff367940da369be2`
- macOS x64: `70fff714285c98d3dd8099ed4636a8ddf593472be55215f0a107f01fea6fb43d`

## Reproduzierbare Protokolltests

Der Host implementiert ServerDesk Plugin-API 1, Laufzeit `serverdesk.web-provider/1`, für `de.zumbyte.remote`. Der Ed25519-Schlüssel ist fest im Host verankert. Katalog und Release-Dateien werden ohne GitHub-API und ohne GitHub-Token geladen.

Die reproduzierbare Prüfung verwendet das unveränderte veröffentlichte Paket `ZumbyteRemote-ServerDesk-Plugin-0.2.0-alpha.1.zip`, SHA-256 `6718a22d821adc46b2d08fb04c5322559a702754fef6ca19c2f0525ac1fa7f33`. `--self-test --plugin-fixtures <folder>` prüft Signatur, Archiv, Prüfsummen, Grenzen, API/Plattform, Rückfall und Sitzungsaufschub. Der Ordner enthält das originale ZIP, catalog.json und catalog.sig.

`tools/plugin-protocol-fixture.mjs` stellt zwei getrennte lokale Testserver mit derselben Geräte-ID bereit. Die ausdrücklich synthetische JPEG-Testfläche stammt aus der Testumgebung. `--plugin-smoke --plugin-multi --plugin-native-input` installiert das originale Paket über den echten signierten Onlinekatalog und prüft die unveränderten Provider in nativen WebView2-/WKWebView-Flächen. Ein isolierter verschlüsselter Testarbeitsbereich verhindert Zugriffe auf Benutzerprofile.

Prüfungen: Login mit und ohne gespeicherten Token, Geräteliste und stabile Origin-Zuordnung, drei getrennte Sitzungen, Relay-Bild, gerichtete native Maus-/Tastaturereignisse, Freigabe bei Fokusverlust, inaktives Fenster, versteckter Tab, Schließen einer Sitzung ohne Beeinträchtigung der anderen, profilfremde Tresor-/Netzwerk-/Socketzugriffe, Tresorsperre, Arbeitsbereichswechsel und erneute Anmeldung. Windows liefert Testereignisse über den nativen Browser; macOS über interne NSEvents an das eigene Fenster. Diese Nachweise ersetzen keinen Test einer physischen Windows-Tastatur oder eines echten Remote-Zielsystems.

Aufnahmen enthalten den tatsächlichen Avalonia-Inhalt und native Live-Snapshots der eingebetteten Browser an deren tatsächlichen Grenzen. Globale Bildschirmaufnahme- und Bedienungshilfenrechte sind dafür nicht nötig. Testserver und Testbild werden nicht als produktiver Remote-Computer ausgegeben. WebRTC zu einem echten Remote-Host und Windows-Diensteinrichtung gegen einen echten Server sind ohne entsprechende Testumgebung nicht belegt.

Quellcode und Testwerkzeuge bleiben im privaten Repository. Öffentliche Pakete enthalten ausschließlich kompilierte Programme, Laufzeiten, Lizenzen und verifizierte Prüfergebnisse.
