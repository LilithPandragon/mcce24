# LaTeX-Vorlage - Thesis Book

## Übersicht

Diese LaTeX-Vorlage wurde exakt an die Word-Vorlage für Masterarbeiten an der Hochschule Burgenland angepasst. 
Alle Formatierungen entsprechen den Vorgaben der Word-Vorlage 12-10-2025.

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
\newcommand{\universityCityCountry}{Hochschule-Burgenland, Eisenstadt, Österreich}
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

