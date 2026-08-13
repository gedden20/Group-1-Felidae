
# Assignment 02: Genome Exploration II

- **Species:** *Panthera tigris* (Tiger)
- **Assembly Accession:** GCA_018350175.1 (isolate Pt1)
- **Objective:** Evaluate assembly contiguity, sequence-length distributions, filtering thresholds, and small open reading frames (ORFs) using Galaxy tools.

## Tools & Parameters Used
- **FASTA Statistics:** Evaluated initial genome continuity, GC content, and summary statistics.
- **Compute sequence length:** Calculated length in base pairs for each scaffold.
- **Sort:** Sorted sequence lengths descending to isolate the top 5 largest chromosome-scale scaffolds.
- **Filter sequences by length:** Evaluated the effect of excluding sequences < 10,000 bp.
- **getorf:** Predicted candidate ORFs on target scaffold `JAEQMW010000115.1` (scaffold_116) with parameters:
  - Minimum size: 300 bp (100 amino acids)
  - What to output: Translation of regions between START and STOP codons

## Biological Interpretation
The *Panthera tigris* genome assembly demonstrates high contiguity and chromosome-scale completeness rather than high fragmentation. With a total length of approximately 2.41 Gb distributed across only 74 scaffolds, the continuity metrics are notably robust: the assembly achieves an N50 of 146.94 Mb with an L50 of just 7, and the largest scaffold reaches 238.22 Mb. These values indicate that half of the total genome sequence is captured in only seven large chromosome-length scaffolds. Furthermore, short sequences contribute minimally to the total assembly; applying a 10 kb filtering threshold filtered out zero scaffolds since the shortest sequence in the entire assembly is 42.56 kb. The overall GC content is 41.64%, consistent with typical mammalian genomic compositions. Finally, the small ORF exploration identified 526 candidate ORFs (≥ 300 bp) on scaffold JAEQMW010000115.1, demonstrating how ab initio codon searches locate potential translation segments. However, this method is limited because it identifies all theoretical reading frames without accounting for eukaryotic intron splicing, regulatory machinery, or verified in vivo transcription.

## Screenshots

<img width="1079" height="1236" alt="1000099752" src="https://github.com/user-attachments/assets/09658df5-d527-4dd9-bec7-6be9a7efa0b2" />

### Figure 1: Raw Genome FASTA Preview


<img width="1080" height="1361" alt="1000099777" src="https://github.com/user-attachments/assets/62857650-8573-4751-8e6f-bfc6124c19e1" />


### Figure 2: Original Assembly Statistics Summary

## Galaxy Reproducibility & Workflow

* **Shared Workflow Link:** [Panthera tigris Genome Exploration Workflow](https://usegalaxy.org/u/ged_den/w/panthera-tigris-genome-exploration-1)
* **Platform:** UseGalaxy.org
* **Description:** This workflow encapsulates all automated steps executed in Galaxy for the thenthera tigris* genome assembly exploration, length filtering, and ORF analysis.

