# Anwalts-Skill

Ein Skill für Claude. Der Anwalts-Skill übersetzt Verträge in normales Deutsch und markiert kritische Stellen, prüft Impressum und Datenschutzerklärung auf typische Lücken, hält mündliche Absprachen schriftlich fest und sammelt alle Kündigungsfristen in einer Liste. Das Anwalts-Briefing fasst deinen Fall zusammen, damit du deinen Anwalt fürs Beraten bezahlst und nicht fürs Einlesen. Kostenlos, MIT-Lizenz.
> **Keine Rechtsberatung.** Der Skill ist eine Lesehilfe und ersetzt keinen Anwalt. Bitte lies die [rechtlichen Hinweise](#rechtliche-hinweise), bevor du ihn nutzt.


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

## Rechtliche Hinweise

**Keine Rechtsberatung.** Der Skill ist ein Werkzeug zur Information und Vorbereitung. Er erbringt keine Rechtsdienstleistung im Sinne des Rechtsdienstleistungsgesetzes (RDG) und ersetzt keine Beratung durch eine Anwältin oder einen Anwalt. Der Name „Anwalts-Skill“ beschreibt das Thema, nicht eine anwaltliche Leistung.

**Keine Gewähr.** KI kann Fehler machen, Klauseln falsch einordnen oder neue Gesetze und Urteile nicht kennen. Die Anleitungen im Skill haben den Rechtsstand Deutschland, November 2026. Prüf jedes Ergebnis, bevor du darauf eine Entscheidung stützt, und hol im Zweifel anwaltlichen Rat.

**Fristen.** Bei Abmahnung, Klage, Mahnbescheid, Kündigung oder Behördenschreiben laufen oft kurze Fristen. Warte nicht auf eine Auswertung, sondern hol sofort anwaltliche Hilfe.

**Vertraulichkeit und Datenschutz.** Was du hochlädst, wird von Claude (Anthropic) verarbeitet. Verträge enthalten oft personenbezogene Daten und Geschäftsgeheimnisse, und viele Verträge, etwa Geheimhaltungsvereinbarungen, verbieten die Weitergabe an Dritte. Prüf vorher, ob du die Unterlagen weitergeben darfst, und schwärze Namen, Adressen und Kontodaten, wenn sie für deine Frage nicht nötig sind. Sieh in den Einstellungen deines Claude-Kontos nach, ob deine Chats zur Verbesserung der Modelle genutzt werden dürfen.

**Berufsgeheimnisträger.** Wer selbst einer Schweigepflicht unterliegt, etwa Ärztinnen, Steuerberater oder Anwälte, darf Mandanten- oder Patientendaten nur unter den Voraussetzungen von § 203 StGB und der DSGVO an Dienstleister geben. Ohne geklärte Grundlage nur anonymisierte Unterlagen verwenden.

**Website-Check.** Die Checkliste deckt typische Lücken ab, aber nicht alle Pflichten jeder Branche. Sie schützt nicht sicher vor Abmahnungen. Rechtstexte wie Impressum, Datenschutzerklärung oder AGB lässt du am besten von einer Anwältin oder einem spezialisierten Anbieter erstellen.

**Haftung.** Der Skill wird kostenlos und ohne Gewähr bereitgestellt (MIT-Lizenz). Eine Haftung für Schäden aus seiner Nutzung ist ausgeschlossen, soweit das gesetzlich zulässig ist.

Anleitung: [thanisch.co/wissen/guides/anwalts-skill-claude](https://thanisch.co/wissen/guides/anwalts-skill-claude)

MIT-Lizenz, siehe [LICENSE](LICENSE). Von [Christopher Thanisch](https://thanisch.co).
