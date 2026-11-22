# Lieferanten-Selbstauskunft – Co-Manufacturing Molkerei

Kleine Web-App ohne Server, mit der (potenzielle) Lohnhersteller eine strukturierte Selbstauskunft ausfüllen.

| Datei | Für wen | Zweck |
|---|---|---|
| `index.html` | Lieferanten | Fragebogen in 7 Abschnitten (Unternehmen, Produkte & Technologie, Kapazität & Abfüllung, Rohstoffe, Qualität & Zertifikate, Nachhaltigkeit, Zusammenarbeit) plus Übersicht |
| `auswertung.html` | Sie (intern) | Mehrere Antwortdateien laden, mit Fit-Score vergleichen, als CSV nach Excel exportieren |

## Einrichten (2 Minuten)
Öffnen Sie `index.html` in einem Texteditor und tragen Sie oben im Block `CONFIG` ein:
Firmenname, Logo-Buchstaben, Ansprechperson, E-Mail und optional die Rückmeldefrist.

## Verteilen
- **Per E-Mail:** `index.html` als Anhang verschicken. Der Lieferant öffnet die Datei per Doppelklick im Browser.
- **Online:** Datei auf Ihrer Website oder kostenlos über GitHub Pages bereitstellen und den Link verschicken.

## Ablauf beim Lieferanten
1. Fragebogen ausfüllen. Die Eingaben werden automatisch lokal im Browser gespeichert, Unterbrechen ist jederzeit möglich.
2. In der Übersicht die **Antwortdatei (JSON)** herunterladen und optional ein **PDF** drucken.
3. „E-Mail vorbereiten“ öffnet eine E-Mail an Sie mit Kurzprofil. Die JSON-Datei hängt der Lieferant an.

## Auswerten
`auswertung.html` öffnen und die erhaltenen JSON-Dateien hineinziehen. Die Tabelle lässt sich per Klick auf die Spaltenköpfe sortieren.
Die Gewichtung des Fit-Scores steht in `WEIGHTS` im Quelltext.

## Fragen anpassen
Alle Fragen stehen im Array `SECTIONS` in `index.html`. Jede Frage hat `id`, `label` und `type`
(`text`, `number`, `select`, `radio`, `multi`, `textarea`, `scale` …); `required:true` macht sie zur Pflichtfrage.

## Datenschutz
Alles läuft lokal im Browser. Es werden keine Daten an einen Server übertragen.

## Artefakt-Version (claude.ai)
`artifact/selbstauskunft.html` ist eine angepasste Fassung für claude.ai-Artefakte. Dort sind Druck, `mailto:`-Links und
direkte Downloads gesperrt. Stattdessen läuft der Download über die Speicherfunktion der Plattform, mit Kopieren als Ausweichlösung.
Externe Personen können in einem Artefakt keine Daten speichern. Antworten kommen deshalb auch hier per Datei bzw. E-Mail zurück.
