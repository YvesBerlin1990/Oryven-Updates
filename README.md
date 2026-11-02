# Oryven Updates

Öffentlicher Downloadkanal für Oryven-Installationen und automatische Updates. Der Quellcode bleibt im privaten Projekt-Repository.

## Aktuelle Version

**Oryven 1.0.82**, veröffentlicht am **2. November 2026**.

- [Aktuellen Installer herunterladen](https://github.com/YvesBerlin1990/Oryven-Updates/releases/latest/download/Oryven-Setup.exe)
- [Aktuelles Release und Versionshinweise](https://github.com/YvesBerlin1990/Oryven-Updates/releases/latest)
- [Release 1.0.82](https://github.com/YvesBerlin1990/Oryven-Updates/releases/tag/v1.0.82)

Version 1.0.82 enthält die Korrekturen für Minimieren und Wiederherstellen sowie die erweiterten Userscript-Funktionen. Sie liegt auch oberhalb der zuvor lokal verteilten 1.0.81. Das Updateangebot für 1.0.75, 1.0.79 und 1.0.81 wurde geprüft.

Diese Veröffentlichung erfolgt bewusst **ohne Codesignatur**; ein Zertifikat ist für den vereinbarten privaten Nutzerkreis nicht vorgesehen. SHA-256-Prüfsummen dienen der Integritätsprüfung und ersetzen keine Codesignatur.

## Installieren oder aktualisieren

Für eine Installation den oben verlinkten `Oryven-Setup.exe` herunterladen und starten. Der gemeinsame Assistent bietet je nach vorhandenem Zustand Installation, Aktualisierung beziehungsweise Reparatur oder Deinstallation an.

In einem bereits installierten Oryven unter **Einstellungen → Über Oryven → Nach Updates suchen** prüfen, das Update herunterladen und **Installieren und neu starten** wählen. Nach dem Update muss die Versionsanzeige **1.0.82** nennen. Browserdaten bleiben bei der Aktualisierung erhalten.

Downloads und Updateprüfung funktionieren ohne GitHub-Konto. Der Velopack-Kanal heißt historisch `private`; dieser Name bezeichnet keine GitHub-Zugriffsbeschränkung.

## Dateien eines Releases

| Datei | Zweck |
|---|---|
| `Oryven-Setup.exe` | Gemeinsamer Installer für Nutzer |
| `Oryven.Browser-<Version>-private-full.nupkg` | Original-Vollpaket für den Updater |
| `releases.private.json` | Update-Feed mit Paketnamen, Versionen, Größen und Prüfsummen |
| `source-<Version>.json` | Herkunftsnachweis mit Quellcode-Commit, Inhaltsfingerabdruck, Build-Konfiguration und Paketprüfsummen |

Der technische Velopack-Erstinstaller ist im gemeinsamen Installer eingebettet und wird nicht separat als fünfte Datei hochgeladen. Ältere Releases können noch eine abweichende Dateiauswahl haben.

Für 1.0.82 sind alle vier öffentlichen Downloads einschließlich Größen und SHA-256-Prüfsummen geprüft. Der [Herkunftsnachweis für 1.0.82](https://github.com/YvesBerlin1990/Oryven-Updates/releases/download/v1.0.82/source-1.0.82.json) benennt den tatsächlich gebauten Quellstand.

## Versionsfolge

Veröffentlichte Versionen werden nicht durch neue Dateien gleichen Namens ersetzt. Korrekturen erhalten eine neue Versionsnummer, die auch höher sein muss als bereits lokal verteilte Versionen. Entwürfe derselben oder einer älteren Version dürfen die Wahl der nächsten Version nicht beeinflussen.
