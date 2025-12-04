# Lipid-Gene Sankey Analysis Tool

Interactive Streamlit app for generating Sankey diagrams linking lipid classes to gene expression changes in White vs Beige adipocytes.

## Installation

```bash
pip install -r requirements.txt
```

## Usage

```bash
streamlit run lipid_gene_sankey_app.py
```

## Input Files

**Transcriptome CSV:**
- Column 1: Gene IDs (e.g., SampleID)
- Remaining columns: Expression values with prefixes like `Hannah_Beige_1`, `Hannah_White_1`

**Lipid CSV:**
- Column 1: Lipid names (e.g., PC 16:0, TG 18:1)
- Remaining columns: Intensity values with prefixes like `Beige_1`, `White_1`

## Parameters

- **Gene log2FC Threshold**: Minimum fold-change to consider genes significant (default: 1.5)
- **Lipid log2FC Threshold**: Minimum fold-change to consider lipids significant (default: 0.8)
- **Top Genes to Display**: Number of top genes to show in Sankey (default: 40)

## Outputs

- **Interactive Sankey Diagram**: HTML file showing lipid class → regulation direction → top genes
- **Summary Statistics**: CSV with gene/lipid counts by regulation direction
- **Flow Data**: CSV with all Sankey node connections and values

## Customization

Adjust column name prefixes in the sidebar to match your data format.

---
**TeSlaa X Kapelczak Metabolomics**
