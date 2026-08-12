
# Assignment 02: Genome Exploration II

- **Species:** *Panthera tigris* (Tiger)
- **Assembly Accession:** GCA_018350175.1 (isolate Pt1)
- **Objective:** Evaluate assembly contiguity, sequence-length distributions, filtering thresholds, and small open reading frames (ORFs) using Galaxy tools.

## Tools & Parameters Used
- **FASTA Statistics:** Evaluated initial genome continuity, GC content, and summary statistics.
- **Compute sequence length:** Calculated length in base pairs for each scaffold.
- **Sort:** Sorted sequence lengths descending to isolate the top 5 largest chromosome-scale scaffolds.
- **Filter sequences by length:** Evaluated the effect of excluding sequences < 10,000 bp.
- **EMBOSS getorf:** Predicted candidate ORFs on target scaffold `JAEQMW010000115.1` (scaffold_116) with parameters:
  - Minimum size: 300 bp (100 amino acids)
  - What to output: Translation of regions between START and STOP codons

## Biological Interpretation
The *Panthera tigris* genome assembly demonstrates high contiguity and chromosome-scale completeness rather than high fragmentation. With a total length of approximately 2.41 Gb distributed across only 74 scaffolds, the continuity metrics are notably robust: the assembly achieves an N50 of 146.94 Mb with an L50 of just 7, and the largest scaffold reaches 238.22 Mb. These values indicate that half of the total genome sequence is captured in only seven large chromosome-length scaffolds. Furthermore, short sequences contribute minimally to the total assembly; applying a 10 kb filtering threshold filtered out zero scaffolds since the shortest sequence in the entire assembly is 42.56 kb. The overall GC content is 41.64%, consistent with typical mammalian genomic compositions. Finally, the small ORF exploration identified 526 candidate ORFs (≥ 300 bp) on scaffold JAEQMW010000115.1, demonstrating how ab initio codon searches locate potential translation segments. However, this method is limited because it identifies all theoretical reading frames without accounting for eukaryotic intron splicing, regulatory machinery, or verified in vivo transcription.
