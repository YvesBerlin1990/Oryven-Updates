# Oryven Updates

Öffentlicher Updatekanal für den privaten Windows-11-Browser Oryven. Updates und Versionshinweise funktionieren ohne GitHub-Konto; der Quellcode und das Meldearchiv bleiben privat.

## Oryven 1.0.86 aktualisieren

Voraussetzung ist die bereits abgeschlossene einmalige Umstellung auf **1.0.85**. Ab **1.0.86** laufen diese und alle folgenden Versionen ausschließlich über die interne Oryven-Updatefunktion:

1. In Oryven **Einstellungen → Über Oryven → Nach Updates suchen** öffnen.
2. Versionshinweise lesen und das Update herunterladen.
3. **Installieren und neu starten** oder die Installation beim Beenden wählen. Danach zeigt Oryven **1.0.86** an.

Die reine Update-EXE aktualisiert die vorhandene Anwendung. Profile, Einstellungen, Lesezeichen, Passwörter, Scripts und Websiteanmeldungen bleiben erhalten. Es gibt keine erneute Einrichtung und keinen zweiten Profilumzug.

[Release 1.0.86 und Changelog](https://github.com/YvesBerlin1990/Oryven-Updates/releases/tag/v1.0.86) · [Versionshinweise im Repository](docs/1.0.86.de.md) · [Updatevertrag](docs/UPDATEKANAL.md)

Version 1.0.86 ergänzt Lesezeichen per Maus, Orvonkey 1.0 und freiwillige private GitHub-Scriptquellen. Einzelheiten stehen im Changelog, das auch in Oryven unter „Neu in Oryven“ erscheint.

## Release-Dateien

`Oryven-Update.exe` ist der reine interne Updater. Version 1.0.85 erwartet technisch noch den früheren Namen `Oryven-Setup.exe`; unter diesem Namen liegt ausschließlich eine bytegleiche Kopie desselben Updaters. **Es wird kein neuer Installer ausgeliefert.** Neue Clients verwenden direkt `Oryven-Update.exe`.

Paketgröße, SHA-256, Version und eingebettete Dateien werden geprüft. Frühere Programmdateien bleiben bis zum bestätigten Neustart verfügbar. Die EXE ist bewusst unsigniert; Sicherheitsrichtlinien werden nicht verändert.

Alte Velopack-Clients bis 1.0.84 erhalten hierüber keine nachträgliche automatische Systemumstellung. Frühere originale Releases und Downloads bleiben unverändert erhalten; diese Version ist ein Update für bereits umgestellte Installationen.

## Zugehörige Repositories

| Repository | Aufgabe | Zugriff |
|---|---|---|
| [Oryven](https://github.com/YvesBerlin1990/Oryven) | Quellcode, Tests, Buildwerkzeuge und Versionshinweise | Privat |
| Oryven-Updates | Updatepakete, öffentlicher Feed, Changelog und Herkunftsnachweise | Öffentlich |
| [Oryven-Feedback](https://github.com/YvesBerlin1990/Oryven-Feedback) | Fehler- und Wunschmeldungen sowie Bearbeitungsstand | Privat |

Dieses Repository enthält die öffentliche Dokumentation; fertige Dateien liegen als GitHub-Release-Assets vor. Es besitzt kein eigenes Buildsystem. Quellcode und Build-Eingaben werden im privaten Oryven-Repository gepflegt. Die vorhandene integrierte Hilfe und der Meldedialog bleiben die Anlaufstellen für Bedienungsfragen und Fehler.

Die App-Nutzungsbedingungen und bestehenden Lizenzhinweise bleiben erhalten. Durch den öffentlichen Downloadkanal wird keine allgemeine Quellcode-Lizenz erteilt.
