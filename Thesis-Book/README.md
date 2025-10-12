# LaTeX-Vorlage für Masterarbeiten - Thesis Book

## Übersicht

Diese LaTeX-Vorlage wurde exakt an die Word-Vorlage für Masterarbeiten an der FH Burgenland angepasst. 
Alle Formatierungen entsprechen den Vorgaben der Word-Vorlage 12-10-2025.

## Formatierungsvorgaben (nach Word-Vorlage)

### Seitenlayout
- **Format:** A4
- **Seitenränder:**
  - Oben: 2,5 cm
  - Unten: 3,0 cm
  - Links: 3,0 cm
  - Rechts: 3,0 cm

### Schriftarten und Größen
- **Hauptschrift:** Times New Roman, 11 pt
- **Zeilenabstand:** Genau 12 pt (entspricht etwa 1,09 in LaTeX)
- **Textausrichtung:** Blocksatz

### Titelseite
- **Titel:** Times New Roman, 16 pt, Zeilenabstand 18 pt
- **Autoren:** Times New Roman, 12 pt, Zeilenabstand 14 pt
- **Institution:** Times New Roman, 10 pt, Zeilenabstand 11 pt

### Überschriften
- **Ebene 1:** Times New Roman, 11 pt, Großbuchstaben
- **Abstand vor:** 36 pt, **Abstand nach:** 6 pt

### Textformatierung
- **Erster Absatz nach Überschrift:** Keine Einrückung (linksbündig)
- **Folgeabsätze:** 0,4 cm Einzug
- **Aufzählungen:** Punkt (•), Einzug 0,63 cm

### Tabellen und Abbildungen
- **Tabellentext:** Times New Roman, 10 pt, Zeilenabstand 11 pt
- **Tabellenbeschriftung:** "Tab. X: Beschreibung", über der Tabelle
- **Abbildungsbeschriftung:** "Abb. X: Beschreibung", unter der Abbildung

### Literaturverweise
- **Format:** (Nachname Jahr)
- **Beispiele:** (Baumann 1994), (Baumann 1994, Steffen 1984)

## Verwendung der Vorlage

### 1. Hauptdatei
Die Hauptdatei ist `thesis-book.tex`. Diese enthält alle Formatierungseinstellungen und bindet die Kapitel ein.

### 2. Daten anpassen
In der Datei `01_data/yourData.tex` müssen folgende Informationen angepasst werden:

```latex
\newcommand{\typeOfWork}{Masterarbeit}
\newcommand{\titleToObtain}{Master of Science in Engineering}
\newcommand{\studyProgram}{Master Program Cloud Computing Engineering}
\newcommand{\yourNameInclTitle}{BSc Max Mustermann}
\newcommand{\yourMatNumber}{2210781666}
\newcommand{\supervisorNameInclTitle}{Univ.-Prof. Daisy Musterfrau}
\newcommand{\departmentName}{Department Informationstechnologie}
\newcommand{\yourThesisTitle}{Beispieltitel der Masterarbeit}
\newcommand{\thesisDate}{\ordinalnum{27} Juli 2024}
\newcommand{\universityCityCountry}{FH-Burgenland, Eisenstadt, Österreich}
```

### 3. Kapitel bearbeiten
Die Kapitel befinden sich im Ordner `thesis_book_chapters/`:

- `00_abstract_de.tex` - Kurzfassung
- `01_introduction.tex` - Einleitung und Problemhintergrund
- `02_relatedWork.tex` - Stand des Wissens / Stand der Technik
- `03_researchQuestion.tex` - Wissenschaftliche Fragestellung
- `04_methodologicalApproach.tex` - Forschungsmethodik
- `05_results.tex` - Ergebnisse
- `06_conclusionAndFutureWork.tex` - Schlussfolgerungen und Ausblick

### 4. Literaturverzeichnis
Die Literaturverweise werden in `references.bib` verwaltet. Die Formatierung erfolgt automatisch nach den Word-Vorgaben.

## Kompilierung

### Voraussetzungen
- LaTeX-Distribution (z.B. TeX Live, MiKTeX)
- biber (für Literaturverwaltung)

### Kompilierungsreihenfolge
```bash
pdflatex thesis-book.tex
biber thesis-book
pdflatex thesis-book.tex
pdflatex thesis-book.tex
```

### Automatische Kompilierung
```bash
latexmk -pdf -bibtex thesis-book.tex
```

## Wichtige Hinweise

### Formatierung
- Alle Formatierungen sind bereits korrekt eingestellt
- Änderungen an der Formatierung sollten nur in den Style-Dateien vorgenommen werden
- Die Word-Vorlage ist die verbindliche Referenz

### Literaturverweise
- Verwenden Sie `\citeref{key}` für Verweise im Text
- Format: (Nachname Jahr)
- Beispiel: `\citeref{mustermann2023}` → (Mustermann 2023)

### Tabellen und Abbildungen
- Verwenden Sie die bereitgestellten Umgebungen `thesistable` und `thesisfigure`
- Beschriftungen werden automatisch formatiert
- Nummerierung beginnt bei 1

### Aufzählungen
- Verwenden Sie die Umgebung `thesisitemize`
- Einzug und Formatierung sind bereits korrekt eingestellt

## Dateistruktur

```
Thesis-Book/
├── thesis-book.tex              # Hauptdatei
├── thesis-book.sty              # Style-Datei
├── 00_preamble/                 # Preamble-Dateien
│   ├── thesis-book.tex
│   ├── german.tex
│   └── english.tex
├── 01_data/                     # Dokumentdaten
│   └── yourData.tex
├── thesis_book_chapters/        # Kapitel
│   ├── 00_abstract_de.tex
│   ├── 01_introduction.tex
│   ├── 02_relatedWork.tex
│   ├── 03_researchQuestion.tex
│   ├── 04_methodologicalApproach.tex
│   ├── 05_results.tex
│   └── 06_conclusionAndFutureWork.tex
├── references.bib               # Literaturverzeichnis
└── README.md                    # Diese Datei
```

## Support

Bei Fragen zur Verwendung der Vorlage wenden Sie sich an den Betreuer der Masterarbeit oder an die IT-Abteilung der FH Burgenland.

## Version

Version 1.0 - Angepasst an Word-Vorlage 2025
