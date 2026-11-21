# Oryven Updates

Öffentlicher Updatekanal für den privaten Windows-11-Browser Oryven. Updates und Versionshinweise funktionieren ohne GitHub-Konto; Quellcode und Meldearchiv bleiben privat.

Dokumentationsstand: 21. November 2026 · Aktuell veröffentlicht: **Oryven 1.0.92** vom 21. November 2026.

## Oryven 1.0.92 aktualisieren

Voraussetzung ist eine bereits auf das native EXE-System umgestellte Installation **ab 1.0.85**, Windows 11 x64 und die vorhandene Microsoft WebView2 Evergreen Runtime. Seit **1.0.86** laufen reguläre Aktualisierungen ausschließlich über die interne Oryven-Updatefunktion:

1. In Oryven **Einstellungen → Über Oryven → Nach Updates suchen** öffnen.
2. Versionshinweise lesen und das Update herunterladen.
3. **Installieren und neu starten** oder die Installation beim Beenden wählen. Danach zeigt Oryven **1.0.92** an.

Für bereits eingerichtete Apps anschließend im eigenen App-Fenster **⋯ → App-Symbol aktualisieren** wählen. Eine Neueinrichtung ist nicht nötig.

Profile, Einstellungen, Lesezeichen, Passwörter, Scripts und Websiteanmeldungen bleiben erhalten. Es gibt keine erneute Einrichtung und keinen zweiten Profilumzug.

[Release 1.0.92 und Changelog](https://github.com/YvesBerlin1990/Oryven-Updates/releases/tag/v1.0.92) · [Versionshinweise im Repository](docs/1.0.92.de.md) · [Updatevertrag](docs/UPDATEKANAL.md)

## Änderungen in 1.0.92

- **Scharfe Desktop-Symbole für Website-Apps:** Oryven verwendet geeignete große Bilder aus den Symbolangaben und dem App-Manifest der Website. Das bisher allein übernommene kleine Tab-Symbol wird dadurch beispielsweise bei Romeo durch eine deutlich höher aufgelöste Vorlage ersetzt.
- Aus geeigneten Vorlagen entstehen acht Windows-Symbolgrößen von **16 bis 256 Pixeln**. Seitenverhältnis und Transparenz bleiben erhalten. Windows kann damit eine passende Größe für Desktop, Taskleiste und unterschiedliche Skalierungen wählen.
- **Bereits installierte Apps aktualisieren:** Öffne die betreffende Website-App und wähle in ihrem Drei-Punkte-Menü **App-Symbol aktualisieren**. Eine Neueinrichtung ist nicht nötig. App-Kennung, Oryven-Bereich, Startadresse, Anmeldung und Verknüpfung bleiben erhalten. Ein neuer Symboldateiname und eine gezielte Windows-Benachrichtigung verhindern, dass weiterhin das kleine alte Symbol aus dem Cache verwendet wird.
- Beschädigte, zu große oder nicht erreichbare Symbolquellen blockieren die Einrichtung nicht. Bei einer fehlgeschlagenen Symbolaktualisierung bleibt das bisherige Symbol erhalten. Ein nur noch erreichbares kleines Ersatzsymbol ersetzt kein bereits höher aufgelöstes Website-Symbol. Fremde oder veränderte Desktop-Verknüpfungen werden nicht überschrieben.
- Die Symbole werden ohne Übernahme deiner Profilcookies oder Zugangsdaten abgerufen. Die Bildverarbeitung läuft getrennt vom Bedienfenster. Der Einrichtungsdialog zeigt den laufenden Vorgang und verhindert widersprüchliche Eingaben während des Speicherns.
- Die Aktualisierung erfolgt über den bestehenden internen Updateweg. Starter, Profile, Lesezeichen, Passwörter, Einstellungen und Scriptdaten bleiben erhalten; eine erneute Einrichtung oder ein Profilumzug findet nicht statt.

Die Symbolqualität hängt weiterhin von den Vorlagen ab, die die Website bereitstellt. Fehlt ein geeignetes großes Rasterbild, bleibt das vorhandene Browser-Symbol der Fallback.

Die native Zahlungs-API `PaymentRequest` bleibt eine Einschränkung der WebView2-Plattform. Die Versionshinweise bestätigen keine allgemeine Unterstützung sämtlicher Händler-Checkouts.

## Release-Dateien

| Datei | Zweck |
|---|---|
| `Oryven-Update.exe` | Reines internes Update einer vorhandenen nativen Installation |
| `Oryven-Setup.exe` | Bytegleicher Updater-Alias für den festen Downloadnamen des Clients 1.0.85 |
| `oryven-release.json` | Version, Downloadnamen, Größe, SHA-256 und Changelog |
| `releases.private.json` | Leerer historischer Feed für alte Velopack-Clients |
| `source-1.0.92.json` | Herkunftsnachweis zu tatsächlichem Quellcommit, Buildkonfiguration und Paketprüfsummen |

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
