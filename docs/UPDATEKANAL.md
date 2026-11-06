# Oryven Updates

Öffentlicher Downloadkanal für Oryven-Installationen und automatische Updates. Der Quellcode bleibt im privaten Projekt-Repository.

## Aktuelle Version

**Oryven 1.0.84**, veröffentlicht am **5. November 2026**. Downloadstand geprüft am **5. November 2026**.

- [Aktuellen Installer herunterladen](https://github.com/YvesBerlin1990/Oryven-Updates/releases/latest/download/Oryven-Setup.exe)
- [Aktuelles Release und Versionshinweise](https://github.com/YvesBerlin1990/Oryven-Updates/releases/latest)
- [Release 1.0.84](https://github.com/YvesBerlin1990/Oryven-Updates/releases/tag/v1.0.84)

Version 1.0.84 behebt den Userscript-Import beim Öffnen des Script Managers aus den Einstellungen. Die Syntaxprüfung benötigt keinen ausgewählten Webseiten-Tab mehr und funktioniert auch für Editor und ZIP-Import aus internen Oryven-Seiten. Neue Scripts bleiben zunächst deaktiviert; fehlerhafte Syntax überschreibt keine vorhandene Scriptdatei.

Die native Browser-Zahlungsschnittstelle `PaymentRequest` bleibt in der verwendeten WebView2-Laufzeit abgeschaltet. Die Veröffentlichung bestätigt keine allgemeine Freigabe aller Händlerzahlungen.

Die bisherigen Korrekturen einschließlich der Zahlungsdialoge aus 1.0.83 bleiben enthalten. Der Updatekanal bietet 1.0.84 für installierte 1.0.75, 1.0.79, 1.0.81, 1.0.82 und 1.0.83 an. Das Upgrade von 1.0.83 auf 1.0.84 wurde einschließlich Datenerhalt und 151 Laufzeitprüfungen mit den installierten Bibliotheken geprüft.

Diese Veröffentlichung erfolgt bewusst **ohne Codesignatur**; ein Zertifikat ist für den vereinbarten privaten Nutzerkreis nicht vorgesehen. SHA-256-Prüfsummen dienen der Integritätsprüfung und ersetzen keine Codesignatur.

## Installieren oder aktualisieren

Für eine Installation den oben verlinkten `Oryven-Setup.exe` herunterladen und starten. Der gemeinsame Assistent bietet je nach vorhandenem Zustand Installation, Aktualisierung beziehungsweise Reparatur oder Deinstallation an.

In einem bereits installierten Oryven unter **Einstellungen → Über Oryven → Nach Updates suchen** prüfen, das Update herunterladen und **Installieren und neu starten** wählen. Nach dem Update muss die Versionsanzeige **1.0.84** nennen. Browserdaten bleiben bei der Aktualisierung erhalten.

Downloads und Updateprüfung funktionieren ohne GitHub-Konto. Der Velopack-Kanal heißt historisch `private`; dieser Name bezeichnet keine GitHub-Zugriffsbeschränkung.

## Dateien eines Releases

| Datei | Zweck |
|---|---|
| `Oryven-Setup.exe` | Gemeinsamer Installer für Nutzer |
| `Oryven.Browser-<Version>-private-full.nupkg` | Original-Vollpaket für den Updater |
| `releases.private.json` | Update-Feed mit Paketnamen, Versionen, Größen und Prüfsummen |
| `source-<Version>.json` | Herkunftsnachweis mit Quellcode-Commit, Inhaltsfingerabdruck, Build-Konfiguration und Paketprüfsummen |

Der technische Velopack-Erstinstaller ist im gemeinsamen Installer eingebettet und wird nicht separat als fünfte Datei hochgeladen. Ältere Releases können noch eine abweichende Dateiauswahl haben.

Am 5. November 2026 wurden alle vier öffentlichen Downloads von 1.0.84 ohne Anmeldung geladen und anhand ihrer Größen und SHA-256-Prüfsummen abgeglichen. Der aktuelle Feed verweist auf das passende Vollpaket und stimmt mit dem Feed des Releases überein. Der [Herkunftsnachweis für 1.0.84](https://github.com/YvesBerlin1990/Oryven-Updates/releases/download/v1.0.84/source-1.0.84.json) benennt den tatsächlich gebauten Quellstand `5d38122369a0acc8f1c7a438b89f62213d3fbbea`.

## Zugehörige Repositories

| Repository | Aufgabe | Zugriff |
|---|---|---|
| [Oryven](https://github.com/YvesBerlin1990/Oryven) | Quellcode, Tests, Buildwerkzeuge und technische Dokumentation | Privat |
| [Oryven-Updates](https://github.com/YvesBerlin1990/Oryven-Updates) | Installationsdateien, Update-Feed und Herkunftsnachweise | Öffentlich |
| [Oryven-Feedback](https://github.com/YvesBerlin1990/Oryven-Feedback) | Fehler- und Wunschmeldungen mit optionalen Screenshots sowie Bearbeitungsstand | Privat |

Der Browser verwendet dieses öffentliche Repository direkt für Downloads, Updateprüfung und Versionshinweise. Die Trennung ermöglicht Downloads ohne Anmeldung und erhält zugleich den privaten Zugriff auf Quellcode und Meldungen.

## Versionsfolge

Veröffentlichte Versionen werden nicht durch neue Dateien gleichen Namens ersetzt. Korrekturen erhalten eine neue Versionsnummer, die auch höher sein muss als bereits lokal verteilte Versionen. Entwürfe derselben oder einer älteren Version dürfen die Wahl der nächsten Version nicht beeinflussen.
