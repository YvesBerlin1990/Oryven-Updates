# Oryven Updates

Hier erhältst du den Installer und automatische Updates für Oryven, einen privaten Browser für **Windows 11 x64**. Downloads funktionieren ohne GitHub-Konto; der Quellcode wird separat im privaten Projekt gepflegt.

## Installieren und aktualisieren

1. [Aktuellen Installer herunterladen](https://github.com/YvesBerlin1990/Oryven-Updates/releases/latest/download/Oryven-Setup.exe) und starten. Der Assistent bietet Installation, Aktualisierung, Reparatur oder Deinstallation an und richtet WebView2 bei Bedarf ein.
2. Oryven öffnen und eine Adresse oder einen Suchbegriff eingeben.
3. Für spätere Updates in Oryven **Einstellungen → Über Oryven → Nach Updates suchen** öffnen, herunterladen und **Installieren und neu starten** wählen.

Zuletzt veröffentlicht: **Oryven 1.0.84 vom 5. November 2026**. Diese Version korrigiert den Userscript-Import aus den Einstellungen. Neue Scripts bleiben zunächst deaktiviert. Die Veröffentlichung ist bewusst **ohne Codesignatur**; veröffentlichte SHA-256-Prüfsummen dienen der Integritätsprüfung.

[Aktuelles Release und Versionshinweise](https://github.com/YvesBerlin1990/Oryven-Updates/releases/latest) · [Release 1.0.84](https://github.com/YvesBerlin1990/Oryven-Updates/releases/tag/v1.0.84)

Die native Zahlungs-API `PaymentRequest` bleibt in der verwendeten WebView2-Laufzeit abgeschaltet; die Version bestätigt keine allgemeine Freigabe aller Händlerzahlungen.

## Hilfe und weitere Informationen

Für Bedienungsfragen die integrierte Hilfe nutzen; Fehler und Wünsche über den Meldedialog in Oryven senden. Die [Dokumentation des Updatekanals](docs/UPDATEKANAL.md) erklärt Release-Dateien, Prüfsummen, Herkunftsnachweise und bisherige Abnahmen.

| Repository | Aufgabe | Zugriff |
|---|---|---|
| [Oryven](https://github.com/YvesBerlin1990/Oryven) | Browserquellcode, Tests, Buildwerkzeuge und technische Dokumentation | Privat |
| [Oryven-Feedback](https://github.com/YvesBerlin1990/Oryven-Feedback) | Meldungen und Bearbeitungsstand | Privat |
| Oryven-Updates | Installer, Update-Feed und Herkunftsnachweise | Öffentlich |

## Ablage und Zuständigkeit

Dieses Repository enthält Dokumentation; fertige Auslieferungsdateien liegen als **GitHub-Release-Assets** vor. Es enthält kein Buildsystem. Deshalb sind zusätzliche `project/`, `build/` und `dist/` hier nicht anwendbar. Quellcode und Build-Eingaben werden im privaten Oryven-Repository gepflegt. Die bestehenden Download- und Updateadressen bleiben erhalten.

Der Kanal wird im Konto [YvesBerlin1990](https://github.com/YvesBerlin1990) gepflegt. Für die App gelten die Nutzungsbedingungen im Installer; eine allgemeine Quellcode-Lizenz wird durch diesen Downloadkanal nicht erteilt.
