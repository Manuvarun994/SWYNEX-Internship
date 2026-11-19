# SWYNEX-Bioinformatics-Internship
- **Intern Name:** Manuvarun Chekrapu
- **Intern ID:** SWX-2026-002655
- **Domain:** Bioinformatics Internship
- **Internship Duration:** October 16, 2026 – November 15, 2026

---

## 📊 Task 1: Dataset Details
- **Dataset File:** `data_summary.tsv`
- **Target Organism:** *Escherichia coli* str. K-12 substr. MG1655
- **Assembly Name:** `ASM584v2` (Reference Genome)
- **Accession IDs:**
  - **NCBI RefSeq Assembly:** `GCF_000005845.2` (Chromosome: `NC_000913.3`)
  - **GenBank Assembly:** `GCA_000005845.2` (Chromosome: `U00096.3`)
- **Source Repository:** NCBI Genome Database
- **BioProject ID:** `PRJNA225` | **BioSample ID:** `SAMN02604091` | **SRA:** `SRS6067201`
- **Submitter:** University of Wisconsin / NCBI RefSeq

---

## 🧹 Task 2: Data Cleaning & Basic Analysis
- **Objective:** Perform data cleaning, handle missing values, and extract fundamental structural and assembly statistics from biological datasets.
- **Data Cleaning Workflow (`Data Cleaning.ipynb`):**
  - Loaded and inspected `data_summary.tsv` across GenBank and RefSeq assembly records.
  - Handled missing metadata values by imputing `Organism Common Name` (`K-12 substr. MG1655`).
  - Verified structural consistency and generated an initial comparative bar chart (`Bar_Plot.png`).

### Technical Specifications & Assembly Statistics
| Metric Parameter | Value / Description |
| :--- | :--- |
| **Genome Size** | ~4.64 Mb (Total chromosome size: 4,641,652 bp) |
| **Contig N50** | 4,641,652 bp (Complete Genome) |
| **Taxonomy ID** | 511145 |
| **Total Genes** | 4,651 genes (4,290 protein-coding genes) |
| **Gene Density** | 1,002.0 genes/Mb |
| **GC Content** | 51% |
| **Assembly Level** | Complete Genome |
| **Submission Date** | 2013-09-26 |

---

## 📈 Task 3: Visualization & Scientific Interpretation
- **Objective:** Generate publication-grade scientific visualizations (`SWYNEX-Visualization & Interpretation.ipynb`) and evaluate what the visual results do and do not prove.

### 1. Annotated Gene Count Comparison (`1_Gene_Count_Comparison.png`)
- **What it displays:** Side-by-side comparison of total annotated genes between GenBank (`GCA_000005845.2`) and NCBI RefSeq (`GCF_000005845.2`).
- **What this DOES prove:** Exact cross-database concordance—both primary archival (GenBank) and curated reference (RefSeq) records report **4,651** total annotated genes for *E. coli* str. K-12 substr. MG1655, confirming complete agreement on total gene count.
- **What this DOES NOT prove:** It does *not* prove whether individual genes are actively transcribed or translated in living cells under specific environmental conditions, nor does it break down internal biotype proportions (protein-coding genes vs. non-coding RNAs and pseudogenes).

### 2. Assembly Completeness & Contiguity (`2_Assembly_Contiguity.png`)
- **What it displays:** Comparison of Total Genome Size (`4.64 Mb`) against Contig N50 (`4.64 Mb`) across both database records.
- **What this DOES prove:** Complete, gapless single-chromosome contiguity—because Contig N50 equals the full chromosome length (`4,641,652 bp`), the assembly represents a single continuous circular chromosome with zero unresolved scaffolding gaps.
- **What this DOES NOT prove:** High structural contiguity does *not* guarantee zero single-nucleotide base-calling errors, nor does it account for structural or plasmid variations present in other clinical or environmental *E. coli* isolates.

### 3. Prokaryotic Genome Compactness (`3_Gene_Density.png`)
- **What it displays:** Computed gene density (`1,002.0 genes/Mb`) derived from total gene count divided by total sequence length in megabases.
- **What this DOES prove:** High coding compactness typical of bacterial genomes (~1 gene per kilobase of DNA), demonstrating efficient genomic organization compared to eukaryotic organisms.
- **What this DOES NOT prove:** Gene density per megabase treats every gene as an equal unit count and does *not* quantify the exact base-pair percentage of coding sequences versus non-coding intergenic regions.

---

## 📄 Task 4: Final Bioinformatics Report
**Title:** Comparative Assembly, Structural Annotation & Quality Assessment of *Escherichia coli* str. K-12 substr. MG1655 (`ASM584v2`)

### 1. Research Question
How consistent are primary archival (GenBank: `GCA_000005845.2`) and curated reference (NCBI RefSeq: `GCF_000005845.2`) genome assembly records for *Escherichia coli* str. K-12 substr. MG1655 (`ASM584v2`) across structural contiguity, annotated gene composition, prokaryotic coding compactness, and automated genome quality benchmarks (CheckM and Average Nucleotide Identity)?

### 2. Methods
1. **Dataset Acquisition & Metadata Curation:**
   - Retrieved paired reference assembly summary records (`data_summary.tsv`) from the NCBI Genome Database (`BioProject: PRJNA225`, `BioSample: SAMN02604091`, `Taxonomy ID: 511145`), originally submitted by the University of Wisconsin on September 26, 2013 (`ASM584v2`, superseding `ASM584v1`).
2. **Data Preprocessing & Cleaning (`Data Cleaning.ipynb`):**
   - Loaded and audited `data_summary.tsv` in Google Colab using Python (`pandas`).
   - Imputed missing `Organism Common Name` values (`K-12 substr. MG1655`) and standardized numerical sequence length, Contig N50, and gene annotation fields.
3. **Quantitative Analysis, Quality Benchmarking & Visualization (`SWYNEX-Visualization & Interpretation.ipynb`):**
   - Computed genome size in megabases ($\text{Mb}$) and prokaryotic gene density ($\text{genes/Mb}$).
   - Cross-referenced NCBI Prokaryotic Genome Annotation Pipeline (PGAP) CheckM (v1.2.4) completeness/contamination metrics and Average Nucleotide Identity (ANI) taxonomic validation.
   - Generated high-resolution (300 DPI) comparative figures (`1_Gene_Count_Comparison.png`, `2_Assembly_Contiguity.png`, and `3_Gene_Density.png`) using `matplotlib` and `seaborn`.

### 3. Results
| Metric Parameter | NCBI RefSeq (`GCF_000005845.2`) | GenBank (`GCA_000005845.2`) | Scientific Interpretation |
| :--- | :--- | :--- | :--- |
| **Assembly Name & Level** | `ASM584v2` — Complete Genome | `ASM584v2` — Complete Genome | Single circular chromosome with zero gaps |
| **Chromosome Accession** | `NC_000913.3` | `U00096.3` | 1 chromosome, 1 scaffold, 1 contig (`0` unlocalized) |
| **Total Sequence / Ungapped Length** | 4,641,652 bp (~4.64 Mb) | 4,641,652 bp (~4.64 Mb) | 100% ungapped sequence length parity across archives |
| **Contig N50 / Scaffold N50** | 4,641,652 bp (~4.64 Mb) | 4,641,652 bp (~4.64 Mb) | `Contig L50 = 1` & `Scaffold L50 = 1` (gapless contiguity) |
| **GC Content** | 51% | 51% | Characteristic *E. coli* genomic base composition |
| **Total Annotated Genes** | 4,651 | 4,651 | Exact cross-database gene model concordance |
| **Protein-Coding Genes** | 4,290 (92.24%) | 4,290 (92.24%) | Remaining 361 genes represent non-coding RNAs & pseudogenes |
| **Computed Gene Density** | 1,002.0 genes/Mb | 1,002.0 genes/Mb | High bacterial coding compactness (~1 gene per kb) |

- **CheckM (v1.2.4) Quality Assessment:** Achieved **99.48% completeness** (89th percentile among *E. coli* RefSeq assemblies) and **0.15% contamination** on the PGAP marker set, confirming high assembly integrity.
- **Taxonomic Verification (ANI):** Status `OK` (`species_match`), exhibiting **99.46% Average Nucleotide Identity** (94.38% assembly coverage) against the *Escherichia coli* type strain (`GCA_000210475.1`).
- **Synthesis:** Both GenBank and RefSeq demonstrate complete structural and annotation agreement, establishing `ASM584v2` as a gapless, high-density prokaryotic reference standard.

### 4. Limitations
1. **Static Structural Blueprint vs. Dynamic Expression:** Assembly and annotation records confirm structural gene presence (`4,651` genes) but do not capture active transcription, translation, or condition-specific gene expression (which require RNA-Seq or proteomics).
2. **Aggregate Gene Density Simplification:** Expressing compactness as `1,002.0 genes/Mb` weights every annotated feature equally regardless of sequence length and does not separate exact coding base-pair coverage from non-coding intergenic regulatory regions.
3. **Laboratory Strain Domestication Bias:** *E. coli* K-12 substr. MG1655 is a domesticated, plasmid-free (`0` plasmids) laboratory reference strain that lacks virulence islands and mobile genetic elements common in wild-type or clinical *E. coli* isolates.
4. **Marker-Based Quality Estimation:** While CheckM reports 99.48% completeness and 0.15% contamination, marker-gene profiling cannot detect subtle single-nucleotide errors or small structural rearrangements outside conserved marker loci.

### 5. References
1. Blattner, F. R., Plunkett, G., Bloch, C. A., et al. (1997). The complete genome sequence of *Escherichia coli* K-12. *Science*, 277(5331), 1453–1462. https://doi.org/10.1126/science.277.5331.1453
2. Hayashi, K., Morooka, N., Yamamoto, Y., et al. (2006). Highly accurate genome sequences of *Escherichia coli* K-12 strains MG1655 and W3110. *Molecular Systems Biology*, 2, 2006.0007. https://doi.org/10.1038/msb4100049
3. Riley, M., Abe, T., Arnaud, M. B., et al. (2006). *Escherichia coli* K-12: a cooperatively developed annotation snapshot—2005. *Nucleic Acids Research*, 34(1), 1–9. https://doi.org/10.1093/nar/gkj405
4. Parks, D. H., Imelfort, M., Skennerton, C. T., Hugenholtz, P., & Tyson, G. W. (2015). CheckM: assessing the quality of microbial genomes recovered from isolates, single cells, and metagenomes. *Genome Research*, 25(7), 1043–1055. https://doi.org/10.1101/gr.186072.114
5. O'Leary, N. A., Wright, M. W., Brister, J. R., et al. (2016). Reference sequence (RefSeq) database at NCBI: current status, taxonomic expansion, and functional annotation. *Nucleic Acids Research*, 44(D1), D733–D745. https://doi.org/10.1093/nar/gkv1189
6. National Center for Biotechnology Information (NCBI). *Escherichia coli* str. K-12 substr. MG1655 genome assembly `ASM584v2` (`GCF_000005845.2` / `GCA_000005845.2`), BioProject `PRJNA225`.

---

## 🛠️ Repository Contents

### Task 2 Files
- `Data Cleaning.ipynb`: Google Colab notebook featuring data loading, inspection, missing value handling (`Organism Common Name` cleaning), and summary statistics.
- `data_summary.tsv`: Raw dataset containing GenBank and RefSeq assembly summaries.
- `Bar_Plot.png`: Initial visualization comparing total gene count across assembly sources (GenBank vs. RefSeq).

### Task 3 & Task 4 Files
- `SWYNEX-Visualization & Interpretation.ipynb`: Google Colab notebook generating publication-grade (`300 DPI`) visualizations using `pandas`, `matplotlib`, and `seaborn`.
- `1_Gene_Count_Comparison.png`: Bar plot comparing total annotated gene counts across GenBank and RefSeq.
- `2_Assembly_Contiguity.png`: Grouped bar plot comparing Total Genome Size vs. Contig N50 (`4.64 Mb`).
- `3_Gene_Density.png`: Bar plot illustrating prokaryotic gene density (`1,002.0 genes/Mb`).
- `README.md`: Complete end-to-end internship documentation and Final Bioinformatics Report (Tasks 1–4).
