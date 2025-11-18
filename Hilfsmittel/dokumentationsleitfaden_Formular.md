# Dokumentationsleitfaden – KNIME & Data Analytics

## 1. Projektbeschreibung

**Projektname:**  
**Version:**  
**Autor:**  
**Zielsetzung (kurz):**  
**Stakeholder:**  

---

## 2. Datenübersicht

| Datensatz | Quelle | Format | Update | Sensitivität | Beschreibung |
|-----------|--------|--------|--------|--------------|--------------|
| customers_raw | CRM | CSV | wöchentlich | intern | Kundendaten |

---

## 3. Workflow-Übersicht

Kurzbeschreibung, wie der Prozess funktioniert.

*Flowchart einfügen (bereits geliefert).*

---

## 4. Abschnittsdokumentation

### 4.1 Datenbereinigung

- **Missing Value Handling** (mean / mode)
- **Duplikate entfernen**
- **Outlier Handling**

### 4.2 Feature Engineering

- **Encoding**
- **Normalisierung**
- **Feature-Erzeugung**

### 4.3 Modellierung

- **Random Forest**
  - Parameter: Trees = 100

---

## 5. Risiken & Hinweise

- Join Keys können zu leeren Zeilen führen
- Modell benötigt Normalisierung
- Encoding abhängig von Kategorien

---

## 6. Versionierung

**Commit Regeln:**

```
feat: new cleaning step
fix: adjusted model threshold
refactor: reorganized workflow
```

---

## 7. Anhänge

Screenshots, Output-Beispiele etc.

---

# KNIME Workflow Dokumentation (PDF-Version)

## Titelblatt

**KNIME WORKFLOW DOKUMENTATION**

- **Projekt:** __________________
- **Version:** __________________
- **Autor:** __________________
- **Datum:** __________________

---

## Inhaltsverzeichnis

1. Projektbeschreibung
2. Datenüberblick
3. Workflow-Ziele
4. Prozessübersicht
5. KNIME Workflow-Details
6. Modellierung
7. Risiken
8. Versionierung
9. Anhänge

---

*Seiten 3–10: Inhalt identisch zu den obigen Abschnitten, formatiert für PDF-Export.*
