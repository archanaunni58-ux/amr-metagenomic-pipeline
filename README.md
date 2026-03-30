# Metagenomic AMR Analysis Pipeline

This pipeline performs end-to-end analysis of shotgun metagenomic sequencing data for the identification of antimicrobial resistance (AMR) genes. It integrates preprocessing, assembly, taxonomic classification, functional annotation, and AMR detection.

---

## Workflow

1. Download sequencing data (SRA Toolkit)
2. Convert SRA files to FASTQ format
3. Quality control and trimming (fastp)
4. Host DNA removal (Kneaddata)
5. Assembly of reads into contigs (MetaSPAdes)
6. Taxonomic classification (Kraken2)
7. Functional annotation (DIAMOND BLASTx)
8. Visualization (MEGAN)
9. AMR gene identification (RGI)

---

## Tools Used

- SRA Toolkit (prefetch, fasterq-dump)
- fastp
- Kneaddata
- MetaSPAdes
- Kraken2
- DIAMOND
- MEGAN
- RGI (CARD database)

---

## Input

- List of SRA accession numbers (selected_files.txt)
- Paired-end sequencing data

---

## Output

- Quality-filtered reads
- Host-removed reads
- Assembled contigs
- Taxonomic classification reports
- Functional annotation files
- AMR gene prediction results

---

## Usage

Run the pipeline using:

```bash
bash amr_pipeline.sh
