# Oryven Updates

Öffentlicher Updatekanal für den privaten Windows-11-Browser Oryven. Updates und Versionshinweise funktionieren ohne GitHub-Konto; Quellcode und Meldearchiv bleiben privat.

Dokumentationsstand: 21. November 2026 · Aktuell veröffentlicht: **Oryven 1.0.93** vom 21. November 2026.

## Oryven 1.0.93 aktualisieren

Voraussetzung ist eine bereits auf das native EXE-System umgestellte Installation **ab 1.0.85**, Windows 11 x64 und die vorhandene Microsoft WebView2 Evergreen Runtime. Seit **1.0.86** laufen reguläre Aktualisierungen ausschließlich über die interne Oryven-Updatefunktion:

1. In Oryven **Einstellungen → Über Oryven → Nach Updates suchen** öffnen.
2. Versionshinweise lesen und das Update herunterladen.
3. **Installieren und neu starten** oder die Installation beim Beenden wählen. Danach zeigt Oryven **1.0.93** an.

Bestehende Website-Apps erhalten beim nächsten Start die kompakte Ansicht. Falls ein altes Symbol geblieben ist, im App-Fenster **⋯ → App-Symbol aktualisieren** wählen. Eine Neueinrichtung ist nicht nötig.

Profile, Einstellungen, Lesezeichen, Passwörter, Scripts und Websiteanmeldungen bleiben erhalten. Es gibt keine erneute Einrichtung und keinen zweiten Profilumzug.

[Release 1.0.93 und Changelog](https://github.com/YvesBerlin1990/Oryven-Updates/releases/tag/v1.0.93) · [Versionshinweise im Repository](docs/1.0.93.de.md) · [Updatevertrag](docs/UPDATEKANAL.md)

## Änderungen in 1.0.93

- **Website-Apps wirken jetzt wie eigene Apps:** Eine einzige kompakte Titelleiste zeigt App-Symbol, Namen, Website und App-Menü. Die separate Adress- und Navigationsleiste, Tabs und das Oryven-Branding entfallen im App-Fenster. Die Website erhält den frei gewordenen Platz.
- **Bedienung im App-Menü:** Zurück, Vorwärts, Startseite, Neu laden, Seitensuche und Downloads bleiben erreichbar. Websiteinformationen, Symbolaktualisierung und App-Verwaltung stehen ebenfalls im Menü bereit. Navigation, Suche, Drucken und Zoom funktionieren weiterhin mit ihren Tastenkürzeln.
- Die kompakte Websiteanzeige zeigt den tatsächlichen geöffneten Ursprung und kennzeichnet einen Wechsel zu einer fremden Website. Weitere Anmelde- und Websitefenster behalten ihre sichtbare Adresse.
- Kleine App-Fenster ab 480 Pixeln Breite und die Rückkehr aus dem Vollbild erhalten die reduzierte Oberfläche. Das normale Oryven-Browserfenster behält seine bisherigen Leisten.
- Die scharfen Symbole aus 1.0.92 bleiben erhalten. Auch die Titelleiste verwendet die größte vorhandene Symbolvariante und verkleinert sie passend. Bereits eingerichtete Website-Apps verwenden dieselbe App-Kennung, Anmeldung, denselben Oryven-Bereich und ihre vorhandene Desktop-Verknüpfung.
- Die Aktualisierung erfolgt über den bestehenden internen Updateweg. Starter, Profile, Lesezeichen, Passwörter, Einstellungen und Scriptdaten bleiben erhalten. Eine Neueinrichtung oder ein Profilumzug ist nicht nötig.

Die native Zahlungs-API `PaymentRequest` bleibt eine Einschränkung der WebView2-Plattform. Die Versionshinweise bestätigen keine allgemeine Unterstützung sämtlicher Händler-Checkouts.

## Release-Dateien

| Datei | Zweck |
|---|---|
| `Oryven-Update.exe` | Reines internes Update einer vorhandenen nativen Installation |
| `Oryven-Setup.exe` | Bytegleicher Updater-Alias für den festen Downloadnamen des Clients 1.0.85 |
| `oryven-release.json` | Version, Downloadnamen, Größe, SHA-256 und Changelog |
| `releases.private.json` | Leerer historischer Feed für alte Velopack-Clients |
| `source-1.0.93.json` | Herkunftsnachweis zu tatsächlichem Quellcommit, Buildkonfiguration und Paketprüfsummen |

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
