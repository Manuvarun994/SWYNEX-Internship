# SWYNEX-Data-Cleaning-and-Basic-Analysis

* **Intern Name:** Manuvarun Chekrapu
* **Intern ID:** SWX-2026-002655
* **Domain:** Bioinformatics Internship
* **Task Objective:** Perform data cleaning, handle missing values, extract fundamental structural and assembly statistics, and generate visualizations from biological datasets.

---

## 📊 Dataset Details

* **Dataset File:** `data_summary.tsv`
* **Target Organism:** *Escherichia coli* str. K-12 substr. MG1655
* **Accession IDs:**
  * **NCBI RefSeq Assembly:** `GCF_000005845.2`
  * **GenBank Assembly:** `GCA_000005845.2`
* **Source Repository:** NCBI Genome Database
* **BioProject ID:** `PRJNA225`
* **Submitter:** University of Wisconsin / NCBI RefSeq

---

## 🔬 Technical Specifications & Assembly Statistics

| Metric Parameter | Value / Description |
| :--- | :--- |
| **Genome Size** | ~4.64 Mb (Total chromosome size: 4,641,652 bp) |
| **Contig N50** | 4,641,652 bp (Complete Genome) |
| **Taxonomy ID** | 511145 |
| **Total Genes** | 4,651 genes |
| **Assembly Level** | Complete Genome |
| **Submission Date** | 2013-09-26 |

---

## 🛠️ Repository Contents

* **`Data Cleaning.ipynb`**: Google Colab notebook featuring data loading, inspection, missing value handling (`Organism Common Name` cleaning), and summary statistics.
* **`data_summary.tsv`**: The raw dataset containing GenBank and RefSeq assembly summaries.
* **`Bar_Plot.png`**: Visualization comparing the total gene count across assembly sources (`GenBank` vs. `RefSeq`).
