# Narratologies of Transmedia Networks — Digital Appendix

This repository contains the interactive digital appendix for the doctoral dissertation:

**Narratologies of Transmedia Networks**  
Author: **Richárd Fejes**  
Supervisor: **Dr. Gábor Tamás Molnár**  
Eötvös Loránd University Doctoral School of Literary Studies, 2025

The appendix provides interactive charts, tables, and network visualizations derived from the research dataset. These tools allow users to explore, sort, and analyze narrative and transmedia network data.

---

## 📂 Repository Structure

- **`index.html`**  
  Main landing page for the appendix. Loads `EMH_cleaned_nodes_2025.xlsx` and displays it as an interactive searchable table using DataTables.

- **`chart1.html`**  
  Displays a pie chart of **Percentages of Narrative Instance Ownership** (Figure 1).  
  - Data source: `emh_data.json`  
  - Processing: Groups owners with less than 3% share into an **"Other"** category.
  - Built with Chart.js.

- **`parse_xlsx.py`**  
  Python script to:
  1. Load `EMH_cleaned_nodes_2025.xlsx`
  2. Clean the `owner` field (trim whitespace, remove empty values)
  3. Export to JSON (`emh_data.json`)

- **`emh_data.json`**  
  Processed dataset used by charts for visualization.

- **`EMH_cleaned_nodes_2025.xlsx`**  
  Primary dataset for EverymanHYBRID node data.

- **Other HTML files** (e.g., `chart2.html`, `chart3.html`, `chart4.html`, `chart5.html`, `the_beast_map.html`, etc.)  
  Each corresponds to a separate figure in the appendix, such as:
  - Fluctuations of narrative voices (absolute and percentage)
  - Platform/channel usage
  - Interactive network maps
  - Node/edge tables for **EverymanHYBRID** and **The Beast ARG**

---

## 📊 Figures

1. **Figure 1:** Percentages of Narrative Instance Ownership  
   Formula:  
   ```
   (owner count / total count) × 100%
   ```  
   Minor owners (<3%) grouped into "Other".

2. **Figures 2–3:** Fluctuation of Dominating Voices (Absolute / Percentages)

3. **Figures 4–5:** Channel Usage (Absolute / Percentages)

4. **Network Maps:** Interactive Cytoscape.js-based visualizations with tooltips, filtering, and grouping.

5. **Data Tables:** Searchable/sortable tables for node and edge data.

---

## ⚙️ Technology Stack

**Frontend:**  
- HTML5, CSS, JavaScript

**Libraries:**  
- [Chart.js](https://www.chartjs.org/) — Data visualizations  
- [DataTables](https://datatables.net/) — Interactive tables  
- [Cytoscape.js](https://js.cytoscape.org/) — Network visualizations  
- [SheetJS](https://sheetjs.com/) — Excel parsing

**Backend/Data Processing:**  
- Python + Pandas (`parse_xlsx.py`) for data cleaning and transformation.

---

## 🚀 Usage

### 1. Local Deployment
Clone the repository:
```bash
git clone https://github.com/afejesrichard/elte.transmedia.git
```
Open any `.html` file in your browser.

> **Note:** Some visualizations require running from a local HTTP server (e.g., `python -m http.server`) due to browser fetch restrictions.

### 2. Data Processing
To regenerate `emh_data.json` from the Excel file:
```bash
pip install pandas openpyxl
python parse_xlsx.py
```

---

## 📄 License
This repository and its contents are part of the doctoral dissertation *Narratologies of Transmedia Networks*.  
Please contact the author for permissions regarding reuse.
