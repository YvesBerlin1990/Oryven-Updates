# Oryven Updates

Öffentlicher Updatekanal für den privaten Windows-11-Browser Oryven. Updates und Versionshinweise funktionieren ohne GitHub-Konto; Quellcode und Meldearchiv bleiben privat.

Dokumentationsstand: 22. November 2026 · Aktuell veröffentlicht: **Oryven 1.0.94** vom 22. November 2026.

## Oryven 1.0.94 aktualisieren

Voraussetzung ist eine bereits auf das native EXE-System umgestellte Installation **ab 1.0.85**, Windows 11 x64 und die vorhandene Microsoft WebView2 Evergreen Runtime. Seit **1.0.86** laufen reguläre Aktualisierungen ausschließlich über die interne Oryven-Updatefunktion:

1. In Oryven **Einstellungen → Über Oryven → Nach Updates suchen** öffnen.
2. Versionshinweise lesen und das Update herunterladen.
3. **Installieren und neu starten** oder die Installation beim Beenden wählen. Danach zeigt Oryven **1.0.94** an.

Nach dem Update in der ROMEO-App **⋯ → ROMEO-Anmeldung einrichten** öffnen und den Zugang direkt im nativen Dialog hinterlegen. Nach der Windows-Bestätigung füllt nur diese App die Felder voraus; du klickst selbst auf **Anmelden**. Eine erneute App-Einrichtung ist nicht nötig.

Profile, Einstellungen, Lesezeichen, Passwörter, Scripts und Websiteanmeldungen bleiben erhalten. Es gibt keine erneute Einrichtung und keinen zweiten Profilumzug.

[Release 1.0.94 und Changelog](https://github.com/YvesBerlin1990/Oryven-Updates/releases/tag/v1.0.94) · [Versionshinweise im Repository](docs/1.0.94.de.md) · [Updatevertrag](docs/UPDATEKANAL.md)

## Änderungen in 1.0.94

- **Gespeicherter Zugang nur für die ROMEO-App:** Über **ROMEO-Anmeldung einrichten** Profilnamen und Passwort einmal im vorhandenen Windows-verschlüsselten Tresor hinterlegen und mit Windows bestätigen.
- **Beim Öffnen vorausgefüllt:** Ausschließlich diese App füllt leere Anmeldefelder voraus. Du klickst selbst auf **Anmelden**; eigene Eingaben bleiben erhalten. Das Formular wird nicht automatisch abgeschickt.
- **Jederzeit ausschaltbar:** Die App-Freigabe lässt sich widerrufen. Gelöschte Zugänge werden nicht durch andere Konten ersetzt; der Tresor bleibt wie bisher verwaltbar.
- **Anmeldestatus ohne Geheimnisse prüfen:** Die App zeigt nur Speicherbeschreibbarkeit und Vorhandensein der ROMEO-Schlüssel, keine Passwörter, Cookies oder Schlüsselwerte.
- Normale Browserfenster, andere Apps, private Ansichten und globale Datenschutzeinstellungen bleiben unverändert. Die Ursache des tatsächlichen Sitzungsverlusts bleibt offen; die Anmeldehilfe garantiert keine unbegrenzte ROMEO-Sitzung.
- Das reguläre Update erhält Starter, App-Kennung, Desktop-Verknüpfung, Profile, Favoriten, Tresor und Scriptdaten. Eine Neueinrichtung oder ein Profilumzug ist nicht nötig.

Die native Zahlungs-API `PaymentRequest` bleibt eine Einschränkung der WebView2-Plattform. Die Versionshinweise bestätigen keine allgemeine Unterstützung sämtlicher Händler-Checkouts.

## Release-Dateien

| Datei | Zweck |
|---|---|
| `Oryven-Update.exe` | Reines internes Update einer vorhandenen nativen Installation |
| `Oryven-Setup.exe` | Bytegleicher Updater-Alias für den festen Downloadnamen des Clients 1.0.85 |
| `oryven-release.json` | Version, Downloadnamen, Größe, SHA-256 und Changelog |
| `releases.private.json` | Leerer historischer Feed für alte Velopack-Clients |
| `source-1.0.94.json` | Herkunftsnachweis zu tatsächlichem Quellcommit, Buildkonfiguration und Paketprüfsummen |

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
