# Oryven – öffentlicher Updatekanal

Dokumentationsstand: 21. November 2026 · Aktuell veröffentlicht: 1.0.89 vom 17. November 2026.

## Version 1.0.89

[Release und Changelog](https://github.com/YvesBerlin1990/Oryven-Updates/releases/tag/v1.0.89) · [Versionshinweise](1.0.89.de.md)

Nach der einmaligen Umstellung auf 1.0.85 gilt dauerhaft der interne Oryven-Updateweg. 1.0.86 und spätere Versionen werden in der bereits installierten Anwendung angeboten, heruntergeladen und nach Nutzerwahl angewandt. Ein neuer Erstinstaller oder ein erneuter Profilumzug gehört nicht dazu.

## Ablauf

Unter **Einstellungen → Über Oryven → Nach Updates suchen** prüfen. „Installieren und neu starten“ und die Installation beim Beenden verwenden dieselbe vorhandene Oberfläche. Die Sitzung wird gespeichert; der eigene Updater wartet auf genau diesen Prozess und startet denselben Profilpfad wieder.

`oryven-release.json` enthält Version, Namen, Größe, SHA-256 und Changelog. Downloadadressen sind an die gelesene Version gebunden. Größe und Hash werden vor dem Austausch erneut geprüft. Das vollständige eingebettete Dateiverzeichnis wird validiert. Die vorhandene Dateitransaktion erhält die Rückfallversion bis zur passenden Startbestätigung.

## Dateien

| Datei | Zweck |
|---|---|
| `Oryven-Update.exe` | Reines internes Update einer vorhandenen nativen Oryven-Installation |
| `Oryven-Setup.exe` | Bytegleicher Updater-Alias für den fest erwarteten Downloadnamen des Clients 1.0.85; kein Installer |
| `oryven-release.json` | Updateversion, Dateinamen, Größe, SHA-256 und Changelog |
| `releases.private.json` | Leerer alter Feed, damit Velopack-Clients keine ungeeigneten Pakete erhalten |
| `source-1.0.89.json` | Tatsächlicher privater Quellcommit, Inhaltsfingerabdruck, Baukonfiguration und Paketprüfsummen |

Der Client 1.0.85 akzeptiert nur den früheren festen Dateinamen. Beide EXE-Dateien sind deshalb identisch; `PreferredFileName` lässt neue Clients direkt die Update-EXE beziehen. Es werden kein WebView2-Bootstrapper und kein Installationsassistent mitgeliefert. Ersteinrichtung, Reparatur und Profilumzug werden abgewiesen. Vorhandener Starter, Profile und Datenpfade bleiben erhalten.

Die bewusst unsignierte Ausgabe braucht kein privates Codesignaturzertifikat. HTTPS und SHA-256 ersetzen keine unabhängige Herausgebersignatur. Windows-Sicherheitsrichtlinien werden nicht verändert.

## Zuständigkeiten und Herkunft

[Oryven](https://github.com/YvesBerlin1990/Oryven) enthält privat Quellcode, Tests und die maßgeblichen Versionshinweise. Dieses öffentliche Repository stellt Updatepakete und Changelog bereit. Oryven liest seine Ansicht „Neu in Oryven“ aus den Texten dieser Releases. [Oryven-Feedback](https://github.com/YvesBerlin1990/Oryven-Feedback) bleibt das private Meldearchiv.

Die Abnahme prüft den internen Übergang vom echten Client 1.0.85 mit synthetischen Profilen einschließlich Lesezeichen, Zugangsdaten, Einstellungen und Scriptwerten. Keine persönlichen Browserdaten werden dafür kopiert oder verändert. Der Build-Commit für 1.0.89 ist `296bf692604fc07965f2a9f64f2a12e468fb0ebd` mit `v1.0.89`; der Herkunftsnachweis verbindet die Pakete genau mit diesem gebauten Stand. Spätere Dokumentationspflege verändert weder Paket noch Tag.

Veröffentlichte Originaldateien und frühere Tags bleiben unverändert. Der frühere Release 1.0.84 verwendet noch Velopack und bleibt als historischer Stand verfügbar; er erhält dadurch keine nachträgliche automatische Umstellung auf das neue System. Der Kanalname `private` ist die historische technische Kanalkennung und keine Zugriffsbeschränkung der öffentlichen Downloads.
