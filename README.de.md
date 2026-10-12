# Open Skills · Skills für KI-Agenten

[简体中文](README.md) · [繁體中文](README.zh-Hant.md) · [English](README.en.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [Español](README.es.md)

Eine öffentliche Sammlung praktischer Agent Skills. Vereinfachtes Chinesisch ist die Hauptsprache; Anleitungen gibt es außerdem auf traditionellem Chinesisch, Englisch, Französisch, Deutsch und Spanisch. Installieren Sie nur die benötigten Skills.

## Skill-Verzeichnis

| Kategorie | Skill | Nutzen | Download |
| --- | --- | --- | --- |
| Agent-Werkzeuge und Interoperabilität | [Agent Tool Discovery](skills/agent-tool-discovery/README.de.md) | Skills, MCP-Server und CLI-Werkzeuge finden und ihre Einbindung reparieren, wenn sie in einem lokalen Agenten funktionieren, in einem anderen aber fehlen. Vorhandene Konfigurationen bleiben erhalten. | [ZIP](https://github.com/xisheng687/open-skills/releases/download/agent-tool-discovery-v1.0.2/agent-tool-discovery.zip) |

**1 veröffentlichter Skill.** Enthalten sind Anweisungen, Referenzen, vollständige chinesische und englische Prompts sowie Anleitungen in sechs Sprachen. Private Skills und Rechnerdaten des Maintainers sind nicht enthalten.

## Herunterladen und verwenden

1. Laden Sie das einzelne Skill-ZIP herunter oder entnehmen Sie dem Repository den vollständigen Ordner `skills/<name>/`.
2. Behalten Sie alle Dateien, Referenzen und die Lizenz. Das gesamte Repository-ZIP ist kein Importpaket für einen einzelnen Skill.
3. Folgen Sie der [deutschen Anleitung](skills/agent-tool-discovery/README.de.md) oder verwenden Sie den [englischen](skills/agent-tool-discovery/references/client-prompt.en.md) bzw. [chinesischen Prompt](skills/agent-tool-discovery/references/client-prompt.zh-CN.md). Eine Antwort auf Deutsch kann ausdrücklich angefordert werden.

Installationspfade und Aufrufmechanismen hängen vom Client und seiner Version ab. Cloud-Agenten können möglicherweise nicht auf lokale Dateien zugreifen. Download oder Installation erlauben nicht automatisch die Ausführung.

## Weitere Skills hinzufügen

Jeder Skill erhält einen stabilen Ordner `skills/<name>/`; Kategorie und Suchbegriffe stehen in den Metadaten. Ergänzen Sie eine chinesische Hauptanleitung, eine englische Fassung und bei Bedarf weitere Übersetzungen sowie einen Verzeichniseintrag. Die [Beitragsregeln](CONTRIBUTING.md) sind auf Chinesisch und Englisch verfügbar.

## Datenschutz und Prüfung

Hier gehören nur allgemeine Anweisungen und öffentliche Quellen hinein: keine Zugangsdaten, echten Rechnerinventare, persönlichen Pfade, privaten Dienste, Backups oder Kundendaten. Statische Prüfung und Paketvalidierung beweisen nicht, dass jeder Client den Skill ausführen kann.

[MIT-Lizenz](LICENSE), auch im eigenständigen Skill-Paket enthalten.
