# Oryven – öffentlicher Updatekanal

Dokumentationsstand: 22. November 2026 · Aktuell veröffentlicht: 1.0.94 vom 22. November 2026.

## Version 1.0.94

[Release und Changelog](https://github.com/YvesBerlin1990/Oryven-Updates/releases/tag/v1.0.94) · [Versionshinweise](1.0.94.de.md)

Nach der einmaligen Umstellung auf 1.0.85 gilt dauerhaft der interne Oryven-Updateweg. 1.0.86 und spätere Versionen werden in der bereits installierten Anwendung angeboten, heruntergeladen und nach Nutzerwahl angewandt. Ein neuer Erstinstaller oder ein erneuter Profilumzug gehört nicht dazu.

## Ablauf

Unter **Einstellungen → Über Oryven → Nach Updates suchen** prüfen. „Installieren und neu starten“ und die Installation beim Beenden verwenden dieselbe vorhandene Oberfläche. Schließe vor dem Update auch geöffnete Website-Apps. Die normale Browsersitzung wird gespeichert; der eigene Updater wartet auf genau diesen Prozess und startet denselben Profilpfad wieder.

`oryven-release.json` enthält Version, Namen, Größe, SHA-256 und Changelog. Downloadadressen sind an die gelesene Version gebunden. Größe und Hash werden vor dem Austausch erneut geprüft. Das vollständige eingebettete Dateiverzeichnis wird validiert. Die vorhandene Dateitransaktion erhält die Rückfallversion bis zur passenden Startbestätigung.

## Dateien

| Datei | Zweck |
|---|---|
| `Oryven-Update.exe` | Reines internes Update einer vorhandenen nativen Oryven-Installation |
| `Oryven-Setup.exe` | Bytegleicher Updater-Alias für den fest erwarteten Downloadnamen des Clients 1.0.85; kein Installer |
| `oryven-release.json` | Updateversion, Dateinamen, Größe, SHA-256 und Changelog |
| `releases.private.json` | Leerer alter Feed, damit Velopack-Clients keine ungeeigneten Pakete erhalten |
| `source-1.0.94.json` | Tatsächlicher privater Quellcommit, Inhaltsfingerabdruck, Baukonfiguration und Paketprüfsummen |

Der Client 1.0.85 akzeptiert nur den früheren festen Dateinamen. Beide EXE-Dateien sind deshalb identisch; `PreferredFileName` lässt neue Clients direkt die Update-EXE beziehen. Es werden kein WebView2-Bootstrapper und kein Installationsassistent mitgeliefert. Ersteinrichtung, Reparatur und Profilumzug werden abgewiesen. Vorhandener Starter, Profile und Datenpfade bleiben erhalten.

Die bewusst unsignierte Ausgabe braucht kein privates Codesignaturzertifikat. HTTPS und SHA-256 ersetzen keine unabhängige Herausgebersignatur. Windows-Sicherheitsrichtlinien werden nicht verändert.

## Zuständigkeiten und Herkunft

[Oryven](https://github.com/YvesBerlin1990/Oryven) enthält privat Quellcode, Tests und die maßgeblichen Versionshinweise. Dieses öffentliche Repository stellt Updatepakete und Changelog bereit. Oryven liest seine Ansicht „Neu in Oryven“ aus den Texten dieser Releases. [Oryven-Feedback](https://github.com/YvesBerlin1990/Oryven-Feedback) bleibt das private Meldearchiv.

Die Abnahme prüft interne Übergänge von den echten Clients 1.0.85, 1.0.91, 1.0.92 und 1.0.93 mit synthetischen geschützten Profilen, einschließlich der verschlüsselten ROMEO-Freigabe und ihres Tresoreintrags. Nach dem Update wird der Appstart über den unveränderten vorhandenen Starter geprüft. Zur bestehenden nativen Browserabnahme mit 650 Prüfpunkten kommen 69 ROMEO-Prüfpunkte mit den gepackten Bibliotheken und vier vollständigen Prozessneustarts hinzu. Sie prüfen Einrichtung, manuelles Anmelden nach Vorausfüllen, eigene Eingaben, Widerruf und die Grenzen zu normalen und privaten Ansichten, fremden Ursprüngen und Frames. Die persönliche ROMEO-Sitzung ist damit nicht abgenommen; deren Verlustursache bleibt offen. Keine persönlichen Browserdaten werden kopiert oder verändert. Der Build-Commit für 1.0.94 ist `a9a0d0f1f995860e55cdb93cd36ff8787b1bbae3` mit `v1.0.94`; der Herkunftsnachweis verbindet die Pakete genau mit diesem Stand. Spätere Dokumentationspflege verändert weder Paket noch Tag.

Veröffentlichte Originaldateien und frühere Tags bleiben unverändert. Der frühere Release 1.0.84 verwendet noch Velopack und bleibt als historischer Stand verfügbar; er erhält dadurch keine nachträgliche automatische Umstellung auf das neue System. Der Kanalname `private` ist die historische technische Kanalkennung und keine Zugriffsbeschränkung der öffentlichen Downloads.
