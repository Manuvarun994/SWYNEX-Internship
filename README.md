# SWYNEX-Data-Cleaning-and-Basic-Analysis

- **Intern Name:** Manuvarun Chekrapu
- **Intern ID:** SWX-2026-002655
- **Domain:** Bioinformatics Internship
- **Task Objective:** Perform data cleaning, handle missing values, extract fundamental structural and assembly statistics, and generate scientific visualizations with critical interpretations from biological datasets.

---

## 📊 Dataset Details
- **Dataset File:** `data_summary.tsv`
- **Target Organism:** *Escherichia coli* str. K-12 substr. MG1655
- **Accession IDs:**
  - **NCBI RefSeq Assembly:** `GCF_000005845.2`
  - **GenBank Assembly:** `GCA_000005845.2`
- **Source Repository:** NCBI Genome Database
- **BioProject ID:** `PRJNA225`
- **Submitter:** University of Wisconsin / NCBI RefSeq

---

## 🔬 Technical Specifications & Assembly Statistics

| Metric Parameter | Value / Description |
| :--- | :--- |
| **Genome Size** | ~4.64 Mb (Total chromosome size: 4,641,652 bp) |
| **Contig N50** | 4,641,652 bp (Complete Genome) |
| **Taxonomy ID** | 511145 |
| **Total Genes** | 4,651 genes |
| **Gene Density** | 1,002.0 genes/Mb |
| **Assembly Level** | Complete Genome |
| **Submission Date** | 2013-09-26 |

---

## 📈 Task 3: Visualization & Scientific Interpretation

### 1. Annotated Gene Count Comparison (`1_Gene_Count_Comparison.png`)
- **What it displays:** Side-by-side comparison of total annotated genes between GenBank (`GCA_000005845.2`) and NCBI RefSeq (`GCF_000005845.2`).
- **What this DOES prove:** Exact cross-database concordance—both primary archival (GenBank) and curated reference (RefSeq) records report **4,651** total annotated genes for *E. coli* str. K-12 substr. MG1655, confirming complete agreement on total gene count.
- **What this DOES NOT prove:** It does **not** prove whether individual genes are actively transcribed or translated in living cells under specific environmental conditions, nor does it break down internal biotype proportions (protein-coding genes vs. non-coding RNAs and pseudogenes).

### 2. Assembly Completeness & Contiguity (`2_Assembly_Contiguity.png`)
- **What it displays:** Comparison of Total Genome Size (`4.64 Mb`) against Contig N50 (`4.64 Mb`) across both database records.
- **What this DOES prove:** Complete, gapless single-chromosome contiguity—because `Contig N50` equals the full chromosome length (`4,641,652 bp`), the assembly represents a single continuous circular chromosome with zero unresolved scaffolding gaps.
- **What this DOES NOT prove:** High structural contiguity does **not** guarantee zero single-nucleotide base-calling errors, nor does it account for structural or plasmid variations present in other clinical or environmental *E. coli* isolates.

### 3. Prokaryotic Genome Compactness (`3_Gene_Density.png`)
- **What it displays:** Computed gene density (`1,002.0 genes/Mb`) derived from total gene count divided by total sequence length in megabases.
- **What this DOES prove:** High coding compactness typical of bacterial genomes (~1 gene per kilobase of DNA), demonstrating efficient genomic organization compared to eukaryotic organisms.
- **What this DOES NOT prove:** Gene density per megabase treats every gene as an equal unit count and does **not** quantify the exact base-pair percentage of coding sequences versus non-coding intergenic regions.

---

## 🛠️ Repository Contents

### Task 2: Data Cleaning & Basic Analysis
- **`Data Cleaning.ipynb`**: Google Colab notebook featuring data loading, inspection, missing value handling (`Organism Common Name` cleaning), and summary statistics.
- **`data_summary.tsv`**: Raw dataset containing GenBank and RefSeq assembly summaries.
- **`Bar_Plot.png`**: Initial visualization comparing total gene count across assembly sources (GenBank vs. RefSeq).

### Task 3: Visualization & Interpretation
- **`SWYNEX-Visualization & Interpretation.ipynb`**: Google Colab notebook generating publication-grade (`300 DPI`) visualizations using `pandas`, `matplotlib`, and `seaborn`.
- **`1_Gene_Count_Comparison.png`**: Bar plot comparing total annotated gene counts across GenBank and RefSeq.
- **`2_Assembly_Contiguity.png`**: Grouped bar plot comparing Total Genome Size vs. Contig N50 (`4.64 Mb`).
- **`3_Gene_Density.png`**: Bar plot illustrating prokaryotic gene density (`1,002.0 genes/Mb`).
