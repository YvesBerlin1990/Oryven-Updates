# Oryven Updates

Öffentlicher Downloadkanal für Oryven-Installationen und automatische Updates. Der Quellcode bleibt im privaten Projekt-Repository.

## Aktuelle Version

**Oryven 1.0.83**, veröffentlicht am **3. November 2026**. Downloadstand geprüft am **5. November 2026**.

- [Aktuellen Installer herunterladen](https://github.com/YvesBerlin1990/Oryven-Updates/releases/latest/download/Oryven-Setup.exe)
- [Aktuelles Release und Versionshinweise](https://github.com/YvesBerlin1990/Oryven-Updates/releases/latest)
- [Release 1.0.83](https://github.com/YvesBerlin1990/Oryven-Updates/releases/tag/v1.0.83)

Version 1.0.83 korrigiert die Übergabe von Zahlungs- und Anmeldedialogen: Fensterreferenzen, Rückmeldungen an den Shop, spätere Weiterleitungen und Formular-POST-Daten bleiben erhalten. Die normale oder private Sitzung des aufrufenden Tabs wird beibehalten. Außerdem enthält der Meldedialog eine eigene Rubrik für Zahlungsprobleme.

Die native Browser-Zahlungsschnittstelle `PaymentRequest` bleibt in der verwendeten WebView2-Laufzeit abgeschaltet. Die Veröffentlichung bestätigt keine allgemeine Freigabe aller Händlerzahlungen.

Die bisherigen Korrekturen und Userscript-Funktionen bleiben enthalten. Der Updatekanal bietet 1.0.83 für installierte 1.0.75, 1.0.79, 1.0.81 und 1.0.82 an; das Upgrade von 1.0.82 auf 1.0.83 wurde bei der Veröffentlichung geprüft.

Diese Veröffentlichung erfolgt bewusst **ohne Codesignatur**; ein Zertifikat ist für den vereinbarten privaten Nutzerkreis nicht vorgesehen. SHA-256-Prüfsummen dienen der Integritätsprüfung und ersetzen keine Codesignatur.

## Installieren oder aktualisieren

Für eine Installation den oben verlinkten `Oryven-Setup.exe` herunterladen und starten. Der gemeinsame Assistent bietet je nach vorhandenem Zustand Installation, Aktualisierung beziehungsweise Reparatur oder Deinstallation an.

In einem bereits installierten Oryven unter **Einstellungen → Über Oryven → Nach Updates suchen** prüfen, das Update herunterladen und **Installieren und neu starten** wählen. Nach dem Update muss die Versionsanzeige **1.0.83** nennen. Browserdaten bleiben bei der Aktualisierung erhalten.

Downloads und Updateprüfung funktionieren ohne GitHub-Konto. Der Velopack-Kanal heißt historisch `private`; dieser Name bezeichnet keine GitHub-Zugriffsbeschränkung.

## Dateien eines Releases

| Datei | Zweck |
|---|---|
| `Oryven-Setup.exe` | Gemeinsamer Installer für Nutzer |
| `Oryven.Browser-<Version>-private-full.nupkg` | Original-Vollpaket für den Updater |
| `releases.private.json` | Update-Feed mit Paketnamen, Versionen, Größen und Prüfsummen |
| `source-<Version>.json` | Herkunftsnachweis mit Quellcode-Commit, Inhaltsfingerabdruck, Build-Konfiguration und Paketprüfsummen |

Der technische Velopack-Erstinstaller ist im gemeinsamen Installer eingebettet und wird nicht separat als fünfte Datei hochgeladen. Ältere Releases können noch eine abweichende Dateiauswahl haben.

Am 5. November 2026 wurden alle vier öffentlichen Downloads von 1.0.83 erneut ohne Anmeldung geladen und anhand ihrer Größen und SHA-256-Prüfsummen abgeglichen. Der aktuelle Feed verweist auf das passende Vollpaket und stimmt mit dem Feed des Releases überein. Der [Herkunftsnachweis für 1.0.83](https://github.com/YvesBerlin1990/Oryven-Updates/releases/download/v1.0.83/source-1.0.83.json) benennt den tatsächlich gebauten Quellstand `e0fa7453ac04892bbdcf8a3c940578a242eec137`.

## Zugehörige Repositories

| Repository | Aufgabe | Zugriff |
|---|---|---|
| [Oryven](https://github.com/YvesBerlin1990/Oryven) | Quellcode, Tests, Buildwerkzeuge und technische Dokumentation | Privat |
| [Oryven-Updates](https://github.com/YvesBerlin1990/Oryven-Updates) | Installationsdateien, Update-Feed und Herkunftsnachweise | Öffentlich |
| [Oryven-Feedback](https://github.com/YvesBerlin1990/Oryven-Feedback) | Fehler- und Wunschmeldungen mit optionalen Screenshots sowie Bearbeitungsstand | Privat |

Der Browser verwendet dieses öffentliche Repository direkt für Downloads, Updateprüfung und Versionshinweise. Die Trennung ermöglicht Downloads ohne Anmeldung und erhält zugleich den privaten Zugriff auf Quellcode und Meldungen.

## Versionsfolge

Veröffentlichte Versionen werden nicht durch neue Dateien gleichen Namens ersetzt. Korrekturen erhalten eine neue Versionsnummer, die auch höher sein muss als bereits lokal verteilte Versionen. Entwürfe derselben oder einer älteren Version dürfen die Wahl der nächsten Version nicht beeinflussen.
