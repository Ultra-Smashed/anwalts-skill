# Modul Fristen

Ziel: Eine Liste aller Verträge mit Kündigungsfrist und dem letzten Tag, an dem man kündigen kann, damit sich nie wieder etwas ungewollt verlängert.

## Eingabe

Verträge als PDFs, Fotos, Bestätigungsmails oder eine Liste (Anbieter, Startdatum, Laufzeit, Frist). Typisch: Miete, Leasing, Versicherungen, Telefon/Internet, Software, Wartung, Mitgliedschaften, Kundenverträge, Dienstleister.

## Ablauf

1. Je Vertrag erfassen: Vertragspartner · Gegenstand · Beginn · Mindestlaufzeit · automatische Verlängerung (um wie lange) · Kündigungsfrist · Form der Kündigung (Textform, schriftlich, Kündigungsbutton) · Kosten pro Monat/Jahr · Fundstelle (Paragraf/Seite).
2. **Letzten Kündigungstag berechnen** mit Code (Laufzeitende minus Frist), für das aktuelle und das nächste Laufzeitende. Unklare Angaben als unklar markieren.
3. **Hinweis Verbraucherverträge:** Seit März 2022 verlängern sich viele Verbraucherverträge nach der Mindestlaufzeit nur noch auf unbestimmte Zeit mit einem Monat Kündigungsfrist (§ 309 Nr. 9 BGB). Für Geschäftsverträge gilt das nicht. Nur erwähnen, wenn relevant.
4. **Ausgabe:**
   - Tabelle sortiert nach letztem Kündigungstag, mit Ampel (🔴 in den nächsten 30 Tagen, 🟡 in 90 Tagen)
   - Kosten pro Jahr gesamt (mit Code)
   - Kündigungsvorlagen für Verträge, die der Mensch beenden will
   - Ist ein Kalender- oder Aufgaben-Werkzeug verbunden: anbieten, für jeden Kündigungstag eine Erinnerung zwei Wochen vorher anzulegen. Sonst eine .ics-Datei mit den Terminen erzeugen, wenn Dateien möglich sind.

Biete an, die Liste beim nächsten neuen Vertrag zu ergänzen.
