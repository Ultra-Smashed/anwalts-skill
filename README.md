# Anwalts-Skill

Ein Skill für Claude. Der Anwalts-Skill übersetzt Verträge in normales Deutsch und markiert kritische Stellen, prüft Impressum und Datenschutzerklärung auf typische Lücken, hält mündliche Absprachen schriftlich fest und sammelt alle Kündigungsfristen in einer Liste. Das Anwalts-Briefing fasst deinen Fall zusammen, damit du deinen Anwalt fürs Beraten bezahlst und nicht fürs Einlesen. Kostenlos, MIT-Lizenz.

| Modul | Was es macht |
| --- | --- |
| **Vertrag lesen** | Kurzfassung, die wichtigsten Punkte als Tabelle und eine Ampel für jede auffällige Klausel, mit Beispiel, was sie praktisch bedeutet, und einem Vorschlag zum Nachverhandeln. |
| **Website-Check** | Impressum nach § 5 DDG, Datenschutzerklärung nach Art. 13 DSGVO und Cookie-Banner nach § 25 TDDDG gegen eine Checkliste. |
| **Absprachen festhalten** | Aus Sprachmemo oder Notizen wird eine Auftragsbestätigung, die der Kunde mit einem „passt“ bestätigt. |
| **Fristen** | Alle Verträge mit Kündigungsfrist und dem letzten Kündigungstag, nach Dringlichkeit sortiert, mit Erinnerungen. |
| **Anwalts-Briefing** | Fall in fünf Sätzen, Fristen, Zeitstrahl, Ziel, Fragen an den Anwalt und ein sortiertes Anlagenverzeichnis. |

## Installation

### Claude-App (Web, Desktop)

Am schnellsten: den Link in einen neuen Chat einfügen und Claude bitten, den Skill zu installieren:

```
https://github.com/Ultra-Smashed/anwalts-skill

Installier diesen Skill für mich.
```

Oder von Hand:

1. [`anwalt.zip`](https://github.com/Ultra-Smashed/anwalts-skill/raw/main/anwalt.zip) herunterladen (nicht entpacken).
2. In Claude unter **Settings → Capabilities** den Schalter **Code execution and file creation** einschalten. In der neueren Ansicht heißt er **Create and edit files**.
3. **Customize → Skills** öffnen, auf **+** klicken, dann **Create skill → Upload a skill** und die ZIP-Datei wählen.

Als Plugin: **Customize → Plugins**, bei den persönlichen Plugins auf **+**, dann **Add from a repository** und `Ultra-Smashed/anwalts-skill` eintragen.

Die Menünamen stehen hier so, wie Anthropic sie in der Hilfe nennt. In der deutschen Oberfläche können sie übersetzt sein.

### Claude Code

Als Plugin:

```
/plugin marketplace add Ultra-Smashed/anwalts-skill
/plugin install anwalt@anwalt
```

Oder den Ordner kopieren:

```bash
git clone https://github.com/Ultra-Smashed/anwalts-skill.git
cp -r anwalts-skill/skills/anwalt ~/.claude/skills/
```

## Benutzen

Einfach schreiben, was du brauchst, zum Beispiel:

> Ich soll diesen Rahmenvertrag unterschreiben. Ich bin der Auftragnehmer. Was muss ich wissen?

> Prüf das Impressum und die Datenschutzerklärung auf meiner Website.

> Ich habe nächste Woche einen Termin beim Anwalt wegen einer offenen Rechnung. Bereite mich vor.

Bei Abmahnung, Klage, Gerichts- oder Behördenfristen gibt der Skill keine Einschätzung. Er nennt die Frist, rät zum Anwalt und hilft dir mit dem Briefing bei der Vorbereitung.

## Dateien

```
skills/anwalt/SKILL.md            Ablauf, Module, Regeln
skills/anwalt/modes/               eine Anleitung pro Modul
anwalt.zip                       derselbe Skill-Ordner als ZIP für die Claude-App
.claude-plugin/                     plugin.json, marketplace.json
```

Nach einer Änderung im Skill-Ordner die ZIP neu bauen: `cd skills && zip -r ../anwalt.zip anwalt`.

**Keine Rechtsberatung.** Der Skill ist eine Lesehilfe und bereitet Gespräche mit Anwälten vor.

Anleitung: [thanisch.co/wissen/guides/anwalts-skill-claude](https://thanisch.co/wissen/guides/anwalts-skill-claude)

MIT-Lizenz, siehe [LICENSE](LICENSE). Von [Christopher Thanisch](https://thanisch.co).
