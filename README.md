# Oryven Updates

Öffentlicher Updatekanal für den privaten Windows-11-Browser Oryven. Updates und Versionshinweise funktionieren ohne GitHub-Konto; Quellcode und Meldearchiv bleiben privat.

Dokumentationsstand: 21. November 2026 · Aktuell veröffentlicht: **Oryven 1.0.89** vom 17. November 2026.

## Oryven 1.0.89 aktualisieren

Voraussetzung ist eine bereits auf das native EXE-System umgestellte Installation **ab 1.0.85**, Windows 11 x64 und die vorhandene Microsoft WebView2 Evergreen Runtime. Seit **1.0.86** laufen reguläre Aktualisierungen ausschließlich über die interne Oryven-Updatefunktion:

1. In Oryven **Einstellungen → Über Oryven → Nach Updates suchen** öffnen.
2. Versionshinweise lesen und das Update herunterladen.
3. **Installieren und neu starten** oder die Installation beim Beenden wählen. Danach zeigt Oryven **1.0.89** an.

Profile, Einstellungen, Lesezeichen, Passwörter, Scripts und Websiteanmeldungen bleiben erhalten. Es gibt keine erneute Einrichtung und keinen zweiten Profilumzug.

[Release 1.0.89 und Changelog](https://github.com/YvesBerlin1990/Oryven-Updates/releases/tag/v1.0.89) · [Versionshinweise im Repository](docs/1.0.89.de.md) · [Updatevertrag](docs/UPDATEKANAL.md)

## Änderungen in 1.0.89

- Neue normale und private Tabs fokussieren sofort die Adressleiste; Rechtsklick und Kopieren erhalten die markierte Auswahl.
- Orvonkey zeigt kompakte Scriptzeilen und erreichbare Aktionen. Suche, Filter und Umschaltung bleiben während Hintergrundprüfungen bedienbar.
- GitHub-Ordnerquellen können ausdrücklich auch Unterordner einbeziehen. Bestehende Quellen werden nicht automatisch erweitert; fehlerhafte oder unvollständige Abgleiche lösen keine lokale Löschung aus.
- Beim Monitorwechsel wird die Browseraufnahme angepasst, ohne Dokument und Formulare neu zu laden. Der dokumentierte Test umfasst zwei Monitore mit jeweils 100 Prozent Skalierung; unterschiedliche physische DPI-Einstellungen bleiben gesondert zu prüfen.
- Transparente Webseiten verwenden wieder eine weiße Browsergrundfläche; ausdrücklich dunkle oder farbige Seiten behalten ihren Hintergrund.

Die native Zahlungs-API `PaymentRequest` bleibt eine Einschränkung der WebView2-Plattform. Die Versionshinweise bestätigen keine allgemeine Unterstützung sämtlicher Händler-Checkouts.

## Release-Dateien

| Datei | Zweck |
|---|---|
| `Oryven-Update.exe` | Reines internes Update einer vorhandenen nativen Installation |
| `Oryven-Setup.exe` | Bytegleicher Updater-Alias für den festen Downloadnamen des Clients 1.0.85 |
| `oryven-release.json` | Version, Downloadnamen, Größe, SHA-256 und Changelog |
| `releases.private.json` | Leerer historischer Feed für alte Velopack-Clients |
| `source-1.0.89.json` | Herkunftsnachweis zu tatsächlichem Quellcommit, Buildkonfiguration und Paketprüfsummen |

**Der aktuelle Download namens Oryven-Setup.exe ist kein Erstinstaller.** Neue Clients verwenden direkt Oryven-Update.exe. Der Updater enthält keinen Einrichtungsassistenten oder WebView2-Bootstrapper. Alte Velopack-Clients bis 1.0.84 erhalten darüber keine nachträgliche automatische Systemumstellung. Frühere originale Releases und Downloads bleiben als historische Stände erhalten.

Paketgröße, SHA-256, Version und eingebettete Dateien werden geprüft. Frühere Programmdateien bleiben bis zum bestätigten Neustart verfügbar. Die EXE ist bewusst unsigniert; HTTPS und Hashprüfung ersetzen keine unabhängige Herausgebersignatur.

## Zugehörige Repositories

| Repository | Aufgabe | Zugriff |
|---|---|---|
| [Oryven](https://github.com/YvesBerlin1990/Oryven) | Quellcode, Tests, Buildwerkzeuge und maßgebliche Versionshinweise | Privat |
| Oryven-Updates | Updatepakete, öffentlicher Feed, Changelog und Herkunftsnachweise | Öffentlich |
| [Oryven-Feedback](https://github.com/YvesBerlin1990/Oryven-Feedback) | Fehler- und Wunschmeldungen sowie Bearbeitungsstand | Privat |

Dieses Repository enthält die öffentliche Dokumentation; fertige Dateien liegen als GitHub-Release-Assets vor. Es besitzt kein eigenes Buildsystem. Die integrierte Hilfe und der Meldedialog im Browser sind die Anlaufstellen für Bedienungsfragen und Fehler.

Die App-Nutzungsbedingungen und bestehenden Lizenzhinweise bleiben erhalten. Durch den öffentlichen Downloadkanal wird keine allgemeine Quellcode-Lizenz erteilt.
