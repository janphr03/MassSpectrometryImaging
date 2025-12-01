# Gewebestrukturierung durch unüberwachtes Lernen auf MSI-Daten

**Autor:innen:** Jan Herrmann, Alexander Maximow  
**Thema:** Unüberwachtes Lernen (Clustering, PCA, NMF) auf Massenspektrometrie-Imaging (MSI) zur automatischen Gewebesegmentierung und als Basis für Lebensmittel­authentifizierung.

---

## Projektüberblick

Dieses Repository demonstriert einen vollständigen Workflow für MSI-Daten (`ims_cube.mat`):

1. **Datenverständnis**
   - Visualisierung einzelner m/z-Kanäle als 2D-Bilder  
   - Beispiel-Spektrum eines Pixels  
   - Globales mittleres Spektrum + Standardabweichung

2. **Datenaufbereitung (Preprocessing)**
   - Medianfilter pro Kanal  
   - TIC- oder L2-Normierung  
   - Log-Transformation  
   - Signal-zu-Rausch-Filterung (SNR)  
   - Spaltenweise Standardisierung (Z-Score)

3. **Clustering (K-Means)**
   - K-Means auf Rohdaten vs. normierten Daten  
   - Visualisierung als Clusterbild (128 × 128)  
   - Interpretation der Cluster als Gewebestrukturen

4. **Dimensionsreduktion / Modellierung**
   - PCA inkl. Varianzkurve und Auswahl der Komponenten via 95%-Threshold  
   - NMF mit 4 Komponenten: räumliche Muster + Basis-Spektren

5. **Business-Use-Case**
   - Skizze eines Data Product Canvas für Lebensmittelauthentifizierung (z. B. Honig, Olivenöl)
   - Idee: Unüberwachte Lernmethoden als SaaS-Lösung zur Betrugserkennung

---

## Datensatz

- Datei: `ims_cube.mat`
- Variable: `ims_cube`
- Form: `(128, 128, 191)`  
  - `128 × 128` = räumliche Pixel  
  - `191` = m/z-Kanäle (Lasereinstellungen / Spektralkanäle)
- Typ: `float64`

> **Hinweis:** Aus lizenzrechtlichen Gründen ist die Datei nicht Teil des Repos.  
> Lege `ims_cube.mat` einfach ins Projektwurzelverzeichnis oder passe den Pfad im Code an.

---

## 🛠️ Installation

Voraussetzung:  
- Python ≥ 3.9  
- `pip` oder `conda`

### 1. Repository klonen

```bash
git clone <DEIN_REPO_LINK>.git
cd <DEIN_REPO_ORDNER>



Diese README wurde mit Hilfe von KI erstellt
