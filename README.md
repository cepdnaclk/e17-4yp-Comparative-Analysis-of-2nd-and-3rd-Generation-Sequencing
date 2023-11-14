# Comparative Analysis of 2nd and 3rd Generation Sequencing

# Table of contents

-  [Introduction](#introduction)
-  [Problem and Solution](#problem-and-solution)


# Introduction
---
![image](https://github.com/ShenalPerera/e17-4yp-Comparative-Analysis-of-2nd-and-3rd-Generation-Sequencing/assets/73387610/f7449cf4-7530-4665-9120-573d0720c39e)

## 1st Generation: Sanger Method
- **Technology:** Chain termination method
- **Read Length:** Typically around 500-1000 base pairs
- **Accuracy:** High
- **Speed:** Relatively slow and labor-intensive
- **Applications:** Initially used for small-scale sequencing projects and genome mapping

## 2nd Generation:
### - Illumina
- **Technology:** Sequencing by synthesis using reversible terminator chemistry
- **Read Length:** Short reads (up to a few hundred base pairs)
- **Throughput:** High, allowing for massive parallel sequencing
- **Applications:** Widely adopted for whole-genome sequencing, resequencing, and transcriptomics

### - Ion Torrent (Thermo Fisher)
- **Technology:** Proton detection based on pH changes during nucleotide incorporation
- **Read Length:** Short to medium reads
- **Throughput:** Moderate, suitable for various applications, including targeted sequencing

### - 454 GS Junior (Roche)
- **Technology:** Pyrosequencing
- **Read Length:** Longer reads than Illumina, but shorter than Sanger
- **Applications:** Initially popular for amplicon sequencing and small genome projects

## 3rd Generation:
### - PacBio (Pacific Biosciences)
- **Technology:** Single-molecule real-time (SMRT) sequencing
- **Read Length:** Very long reads (thousands of base pairs)
- **Throughput:** Moderate
- **Advantages:** Ability to sequence longer DNA fragments, useful for de novo genome assembly and structural variant detection

### - Oxford Nanopore
- **Technology:** Nanopore sequencing, measuring changes in electrical current as DNA passes through a nanopore
- **Read Length:** Long reads, potentially spanning entire genomes
- **Advantages:** Real-time sequencing, portability, and adaptability for various sample types
- **Applications:** Portable sequencing for fieldwork, long-read applications, and rapid diagnostics

## Summary:
- **1st Generation:** Sanger method with high accuracy but limited throughput.
- **2nd Generation:** Multiple platforms like Illumina, Ion Torrent, and 454 GS Junior, offering higher throughput with shorter reads.
- **3rd Generation:** PacBio and Oxford Nanopore with the ability to generate long reads, enabling more comprehensive genome analysis and real-time sequencing.




# DNA Sequencing and Analysis Pipeline

![image](https://github.com/ShenalPerera/e17-4yp-Comparative-Analysis-of-2nd-and-3rd-Generation-Sequencing/assets/73387610/685092f4-0440-4684-b41c-a2b5744593a0)


## 1. Data Acquisition
- **Process:** Obtain raw sequencing data from the sequencing platform (e.g., Illumina, PacBio, Oxford Nanopore).
- **Formats:** Data is typically in FASTQ format, containing short nucleotide sequences with associated quality scores.

## 2. Quality Control
- **Objective:** Assess and ensure the quality of the raw sequencing data.
- **Steps:**
  - Evaluate base quality scores to identify potential sequencing errors.
  - Remove or trim low-quality reads and adaptors.
  - Verify overall data quality metrics using tools like FastQC.

## 3. Reference-based or De Novo Assembly
### Reference-based:
- **Process:** Align sequenced reads to a known reference genome.
- **Tools:** Utilize aligners such as BWA, Bowtie, or HISAT2.
- **Applications:** Variant calling, resequencing, and identification of genomic variations.

### De Novo:
- **Process:** Assemble reads into contigs without relying on a reference genome.
- **Tools:** Assemblers like SPAdes, Velvet, or SOAPdenovo.
- **Applications:** Studying non-model organisms, identifying novel genomes, or in the absence of a reference genome.

## 4. Assembly Quality Assessment
- **Objective:** Evaluate the quality and completeness of the assembled genome.
- **Steps:**
  - Calculate metrics such as N50, representing the contig length at which 50% of the assembly is contained.
  - Assess the presence of gaps, misassemblies, and potential contamination.
  - Validate the assembly using tools like BUSCO to measure the completeness of conserved genes.

## 5. Additional Analyses (Optional)
- **Variant Calling:** Identify genetic variations, such as single nucleotide polymorphisms (SNPs) and insertions/deletions (indels).
- **Functional Annotation:** Annotate genes and predict their functions.
- **Comparative Genomics:** Compare genomes across different individuals or species.
- **Phylogenetic Analysis:** Reconstruct evolutionary relationships based on genetic data.

# Summary
The DNA sequencing and analysis pipeline involves acquiring raw data, performing quality control, choosing between reference-based or de novo assembly, and assessing the quality of the assembled genome. Additional analyses can be conducted to extract biological insights from the genomic data.

![image](https://github.com/ShenalPerera/e17-4yp-Comparative-Analysis-of-2nd-and-3rd-Generation-Sequencing/assets/73387610/a44a9d51-fc12-4a18-8ec4-b759d405ed4b)


# Problem and Solution
---

## Gaps between current studies
- Sequencing quality and coat
- Computational and time demands
- Application suitability
- Possibility and Feasibility

## Identified & proposed solution
_Having a completely unbiased comparative analysis for current 2nd-generation and 3rd-generation gene sequencing is critical for the area of bio-informatics, in terms of molecular biology_


