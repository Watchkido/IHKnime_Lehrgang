📘 Dokumentationsleitfaden für Flowcharts & KNIME-Workflows (Data Analytics)
🎯 Zweck des Leitfadens

Dieser Leitfaden soll sicherstellen, dass:

Workflows verständlich, wartbar und reproduzierbar sind

Teammitglieder Prozesse nachvollziehen können

Übergaben und Reviews effizient funktionieren

zukünftige Anpassungen ohne Risiko möglich sind

1️⃣ Allgemeine Projekt-Dokumentation
1. Projektsteckbrief

Kurze Übersicht, gern auf 1 Seite:

Projektname

Zielsetzung / Business Problem

Owner / Verantwortliche

Datenquellen

Hauptoutputs (Dashboards, Modelle, Reports)

Stakeholder

Version / Datum

2. Datenbeschreibung

Für alle verwendeten Datensätze:

Name und Speicherort

Format (CSV, SQL etc.)

Quelle (intern, extern, API etc.)

Update-Zyklus / Refresh

Schema (Spalten, Datentypen)

Relevante Qualitätsprobleme

Zugriffsrechte / Sensitivität

2️⃣ Dokumentation von Flowcharts / Prozessdiagrammen
1. Ziel des Flowcharts

Beschreibe kurz:

Was zeigt das Diagramm?

Was soll damit erreicht werden?

Wo im übergeordneten Prozess befindet es sich?

2. Konventionen

Leg Standard-Icons / Farben fest:

Blau: Dateninput

Gelb: Transformation / Verarbeitung

Grün: Output / Ergebnisse

Rot: Fehlerbehandlung

Orange: Entscheidungen

→ Optional kannst du eine kleine Legende am Rand einbauen.

3. Detail-Kommentare

Jedes Element sollte enthalten:

klare Bezeichnung

kurze Beschreibung (1–2 Sätze)

Verweise auf KNIME-Knoten (falls relevant)

4. Versionierung

Im Flowchart dokumentieren:

Versionsnummer

Datum

Ersteller / Reviewer

3️⃣ KNIME-Workflow Dokumentation
🔧 A. Struktur & Naming Conventions
1. Ordner- und Workflowstruktur

Empfohlen:

/01_raw
/02_preprocessing
/03_feature_engineering
/04_modeling
/05_evaluation
/06_output
/99_archive

2. Benennung von Knoten

Kurze, klare, sprechende Namen:

Beispiel	Schlecht	Gut
Node Name	"Node 45"	"Remove Outliers"
Metanode	"Metanode1"	"Customer Cleaning Pipeline"

Regel:
➡️ Verb + Objekt („Calculate Mean“, „Join Customer Data“)

🗂️ B. Metanodes & Components

Jede Metanode/Component enthält:

Beschreibung der Funktion

Input/Output-Spezifikation

Parameterbeschreibung

Risiken oder bekannte Probleme

Beispieloutput (falls sinnvoll)

📝 C. Dokumentation innerhalb des Workflows
1. Annotationen

Nutze die eingebaute Kommentarfunktion mit:

grauen Boxen für Kontext

gelbe Boxen für wichtige Hinweise

rote Boxen für Risiken / Fehlerquellen

2. Start-Annotation

Am Anfang des Workflows:

Workflow-Zweck

Erwartete Inputs

Hauptoutputs

Version & Datum

3. Abschnittskommentare

Vor jedem Block:

Kurze Übersicht (z. B. „Datenbereinigung“)

Auflistung der wichtigsten Schritte

📊 D. Parameter- & Modell-Dokumentation
1. Parameterliste

Tabellarisch:

Parameter	Wert	Beschreibung	Warum?
Min Frequency	5	Filter	Entfernt seltene Kategorien
2. Machine Learning Modelle

Für jedes Modell:

Modelltyp

Train/Test-Split

Featureliste

Hyperparameter

Performance-Metriken

Interpretationshinweise

Version des Trainingsdatensatzes

4️⃣ Reproduzierbarkeit & Governance
1. Code / Workflow Versionierung

Git oder KNIME Server verwenden

Commit Messages nach Standard:
feat: added outlier filter
fix: corrected wrong join condition

2. Datenversionierung

Input-Datasets mit Zeitstempel ablegen

Wichtige Datensnapshots im Projekt speichern

3. Logging

Mindestens:

Workflow-Run

verwendete Datenversion

Erstellte Outputs

Warnungen / Fehler

5️⃣ Übergabe-Dokumentation (für Team oder Kunden)
Kurz-Report (1–3 Seiten)

Was macht der Workflow?

Welche Daten?

Wie wird er ausgeführt?

Welche Outputs entstehen?

Wo liegen Stolperfallen?

Technische Übergabe

KNIME-Workflow (.knwf)

README

Beispiel-Dataset

Beispiel-Output

6️⃣ Vorlagen / Templates
README-Template
# Projektname

## 1. Ziel
<Kurze Beschreibung>

## 2. Datenquellen
- <Datenquelle 1>
- <Datenquelle 2>

## 3. Workflowbeschreibung
<1–2 Absätze>

## 4. Ordnerstruktur
<Struktur>

## 5. Ausführung
- Schritt 1 …
- Schritt 2 …

## 6. Outputs
- <Output 1>
- <Output 2>

## 7. Version
v1.0 – <Datum>
Autor: <Name>





[Start]
   |
   v
[Load Raw Data]
   |
   v
[Check Schema]
   |
   v
[Data Cleaning?] ----No----> [Proceed]
       | 
      Yes
       |
       v
[Handle Missing Values]
   |
   v
[Remove Duplicates]
   |
   v
[Outlier Detection]
   |
   v
[Data Transformation Needed?] ---No---> [Proceed]
                |
               Yes
                |
                v
[Feature Engineering]
   |
   v
[Train/Test Split]
   |
   v
[Model Training]
   |
   v
[Model Evaluation]
   |
   v
[Export Results / Dashboard]
   |
   v
[End]



1. Beispiel-Flowchart (Data Cleaning & Analysis in KNIME)

Du kannst dieses Flowchart 1:1 in Draw.io, Miro, PowerPoint oder Visio nachbauen.

[Start]
   |
   v
[Load Raw Data]
   |
   v
[Check Schema]
   |
   v
[Data Cleaning?] ----No----> [Proceed]
       | 
      Yes
       |
       v
[Handle Missing Values]
   |
   v
[Remove Duplicates]
   |
   v
[Outlier Detection]
   |
   v
[Data Transformation Needed?] ---No---> [Proceed]
                |
               Yes
                |
                v
[Feature Engineering]
   |
   v
[Train/Test Split]
   |
   v
[Model Training]
   |
   v
[Model Evaluation]
   |
   v
[Export Results / Dashboard]
   |
   v
[End]


Legende (konform zu Leitfaden):
🟦 Input / Datenquellen
🟨 Transformation / Prozess
🟩 Output
🟥 Entscheidung
🟧 Modellierung

⭐ 2. Word-/PDF-Vorlage – Dokumentationsleitfaden (kompletter Text zum Kopieren)

Du kannst diesen Inhalt direkt in Word, Google Docs oder PDF übernehmen.

DOKUMENTATIONSLEITFADEN – Data Analytics & KNIME Workflow
1. Projektdetails

Projektname:

Version:

Datum:

Autor:

Kurzbeschreibung (max. 5 Sätze):

2. Datenübersicht
Datensatz	Quelle	Format	Update-Zyklus	Sensitivität	Beschreibung
3. Workflow-Zweck

Beschreibe:

Was tut der Workflow?

Welche Hauptoutputs werden erzeugt?

Für wen ist der Workflow gedacht?

4. Workflow-Überblick

Kurzer Abschnitt (1–2 Absätze):

Welche Schritte enthält der Prozess?

Welche Logik steckt dahinter?

Wie ist der Workflow strukturiert?

Optional: Flowchart einfügen.

5. Struktur (Ordner & KNIME-Teile)
5.1 Ordnerstruktur
/01_raw
/02_preprocessing
/03_feature_engineering
/04_modeling
/05_evaluation
/06_output
/99_archive

5.2 KNIME Workflow-Struktur
Abschnitt	Beschreibung	Wichtige Knoten	Outputs
6. Knoten- und Component-Dokumentation

Für jeden Teil:

Beispiel:

Metanode: Customer Cleaning
Zweck: Entfernt Fehler, Duplikate, formatiert Daten
Inputs: customers_raw
Outputs: customers_clean
Parameter:

Missing Value Threshold: 30%

Outlier Method: IQR (1.5)

7. Modell-Dokumentation (falls relevant)
Modelltyp	Parameter	Featureliste	Trainingsdatenversion	Performance	Kommentar
8. Ausführung

Schritt 1: Daten bereitstellen

Schritt 2: Workflow starten

Schritt 3: Outputs prüfen

Schritt 4: Ergebnisse exportieren

9. Risiken & Stolperfallen

Daten können fehlen wenn …

Join-Key empfindlich gegenüber …

Modell abhängig von …

Workflow scheitert wenn …

10. Versionierungshinweise

Commit-Format:

feat: added cleaning pipeline  
fix: corrected join key  
refactor: reorganized modeling section  

11. Anhänge

Beispiel-Output

Screenshots

Flowchart

⭐ 3. Checkliste für Workflow-Reviews

Perfekt für dich oder Teamkollegen – Häkchenliste:

✔ Struktur

 Workflow folgt einer klaren Sektionierung

 Benennung der Knoten ist einheitlich

 Keine unbenannten Knoten

 Alle Metanodes haben Beschreibung

✔ Daten

 Alle Datenquellen dokumentiert

 Eingangsdatensatz validiert

 Missing Values behandelt

 Duplikate geprüft

✔ Logik

 Jeder Prozessschritt ist nachvollziehbar

 Join Keys klar dokumentiert

 Ausreißer-Handling korrekt

 Transformationen erklärt

✔ Parameter

 Alle wichtigen Parameter dokumentiert

 Defaults bewusst gewählt

 Modellparameter nachvollziehbar

✔ Annotationen in KNIME

 Jeder Abschnitt hat Annotation

 Startbereich erklärt Zweck

 Risiken markiert

 Outputs klar benannt

✔ Ausgabedaten

 Outputs sauber formatiert

 Dateinamen konsistent

 Ergebnisse plausibilisiert

✔ Reproduzierbarkeit

 Versionen dokumentiert

 Eingangsdatensatz gespeichert

 Zufallsseed gesetzt (falls CI/ML)

 Ausführungsschritte beschrieben

⭐ 4. Beispiel-KNIME-Workflow mit Kommentaren (zum Nachbauen)

Nach KNIME-Logik aufgebaut:

[Input Section]
  - File Reader (customers_raw.csv)
  - Annotation: "Rohdaten – keine Änderungen!"

[Validation Section]
  - Table Schema Inspector
  - Missing Value Counter
  - Annotation: "Validierung, bevor wir mit Cleaning starten"

[Cleaning Section]
  - Missing Value Node (Mean for numeric, Most frequent for categorical)
  - Duplicate Row Filter
  - String Manipulation (trim, lowercase)
  - Numeric Outliers (IQR)
  - Annotation: "Datenbereinigung Teil 1"

[Feature Engineering Section]
  - Math Formula (new features)
  - One-Hot Encoding
  - Normalization
  - Annotation: "Neue Variablen für Modell"

[Split Section]
  - Partitioning (70/30)
  - Annotation: "Train/Test Split, Seed = 42"

[Model Section]
  - Random Forest Learner
  - Random Forest Predictor
  - Annotation: "Modelltraining + Anwendung"

[Evaluation Section]
  - Scorer (Accuracy, Precision, Recall)
  - ROC Curve
  - Annotation: "Modellbewertung"

[Output Section]
  - Excel Writer (results.xlsx)
  - Annotation: "Finale Ergebnisse"