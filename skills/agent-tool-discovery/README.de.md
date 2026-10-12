# Agent Tool Discovery · Werkzeuge finden und ihre Einbindung reparieren

[简体中文](README.md) · [繁體中文](README.zh-Hant.md) · [English](README.en.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [Español](README.es.md)

**Kategorie:** Agent-Werkzeuge und Interoperabilität · **Version:** 1.0.2

## Welches Problem wird gelöst?

„Bereits installiert, aber ein anderer Agent findet es nicht.“ Skill-Verzeichnisse, MCP-Konfigurationen und Anmeldesitzungen unterscheiden sich zwischen Clients. Ein CLI-Werkzeug kann im Terminal funktionieren, im PATH einer Desktop-App aber fehlen.

Dieser Skill erfasst lokale Agenten und Werkzeuge, nutzt eine gemeinsame Skill-Quelle und wählt je nach tatsächlicher Unterstützung native Erkennung, einzelne symbolische Links oder nachverfolgte Kopien. Er passt MCP-Definitionen an den Client an, prüft CLI-Pfade, erstellt einen lokalen Index und unterscheidet vorhandene Dateien, Erkennung und erfolgreiche Aufrufe.

## Herunterladen und installieren

Laden Sie das [eigenständige ZIP](https://github.com/xisheng687/open-skills/releases/download/agent-tool-discovery-v1.0.2/agent-tool-discovery.zip) herunter oder entnehmen Sie dem Repository den vollständigen Ordner `skills/agent-tool-discovery/`. Behalten Sie alle Dateien und Referenzen. Weder SKILL.md allein noch das gesamte Repository-ZIP ist das vollständige Importpaket dieses Skills.

Unterstützte Clients können `~/.agents/skills/agent-tool-discovery/` nutzen; Claude Code verwendet `~/.claude/skills/agent-tool-discovery/`. Prüfen Sie Produkt und Version. Vergleichen Sie vorhandene gleichnamige Pakete, statt sie zu überschreiben.

Fügen Sie das ZIP an oder nennen Sie den entpackten Ordner und bitten Sie den Agenten:

> Installiere nur diesen Skill im bestätigten Benutzer-Skill-Verzeichnis dieses Clients. Erhalte das ganze Paket und widersprüchliche Versionen. Prüfe die Erkennung in einer neuen Sitzung. Führe noch keine Bestandsaufnahme oder Reparatur aus.

## Verwenden

> Nutze agent-tool-discovery, um die Agenten und Werkzeuge dieses Rechners zu prüfen. Berichte nur und ändere nichts. Antworte auf Deutsch.

> Nutze agent-tool-discovery, um die Werkzeugerkennung meiner lokalen Agenten zu prüfen und zu reparieren. Erhalte bestehende Konfigurationen. Frage mich bei nötiger Anmeldung oder ungelösten Konflikten. Antworte auf Deutsch.

In Codex ist `$agent-tool-discovery` möglich. Ohne Installation können Sie den vollständigen [englischen](references/client-prompt.en.md) oder [chinesischen Prompt](references/client-prompt.zh-CN.md) verwenden. Diese Prompts erlauben standardmäßig begrenzte reversible Reparaturen; für eine reine Prüfung ausdrücklich „nur prüfen, nichts ändern“ angeben.

## Berechtigungen, Datenschutz und Grenzen

Bestehende Konfigurationen, deaktivierte Zustände und Projektbereiche bleiben erhalten. Keine Abhängigkeiten installieren, Tools aktualisieren oder Originale löschen; keine OAuth-Zugangsdaten oder eingebetteten Geheimnisse auf weitere Clients übertragen. Bei einer reinen Prüfung werden keine Indizes, Regeln, Backups oder Aufgaben angelegt. Download oder Installation erlauben nicht automatisch Reparaturen.

Inventare, Backups und Berichte bleiben lokal und privat, außerhalb versionierter oder öffentlich geteilter Verzeichnisse. Der Skill besteht aus Anweisungen, ohne Hintergrunddienst oder Upload-Skript, und benötigt lokalen Zugriff. Der Katalog ist keine Kompatibilitätszertifizierung. Nicht mögliche Prüfungen werden als unbestätigt ausgewiesen. Drittprodukte haben eigene Datenrichtlinien.

## Optionale regelmäßige Prüfungen

Nach Abschluss können Sie regelmäßige Prüfungen wählen. Zustimmung, Häufigkeit, Zeitplanung und lokaler Zugriff müssen bestätigt werden. Standardmäßig wird nur gelesen; ohne relevante Änderungen gibt es keine Meldung. Automatische Reparaturen benötigen eine gesonderte Erlaubnis; Anmeldung und Konflikte werden nicht automatisch erledigt.

[MIT-Lizenz](LICENSE).
