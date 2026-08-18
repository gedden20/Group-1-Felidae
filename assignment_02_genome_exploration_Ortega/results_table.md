Assignment 02: Genome Exploration II

Species: Felis chaus (Jungle Cat)
Assembly Accession: GCA_019924945.1 

Objective: Evaluate assembly contiguity, sequence-length distributions, filtering thresholds, and small open reading frames (ORFs) using Galaxy tools.

Tools & Parameters Used

FASTA Statistics: Evaluated initial genome continuity, GC content, and summary statistics.

Compute sequence length: Calculated length in base pairs for each scaffold.

Sort: Sorted sequence lengths descending to isolate the top 5 largest chromosome-scale scaffolds.

Filter sequences by length: Evaluated the effect of excluding sequences < 10,000 bp.

getorf: Predicted candidate ORFs on target scaffold JAEQMW010000115.1 (scaffold_116) with parameters:

Minimum size: 300 bp (100 amino acids)

What to output: Translation of regions between START and STOP codons
Biological Interpretation

The Felis chaus genome assembly demonstrates high contiguity and chromosome-scale completeness rather than high fragmentation. With a total length of approximately 2.43 Gb (2,428,394,365 bp) distributed across only 53 scaffolds, the continuity metrics are notably robust: the assembly achieves an N50 of 140.55 Mb with an L50 of 7, and the largest scaffold reaches 240.01 Mb. These values indicate that half of the total genome sequence is captured in just seven large chromosome-length scaffolds. Furthermore, short sequences contribute minimally to the total assembly, with the shortest sequence measuring 17.25 kb. The overall GC content is 41.79%, consistent with typical mammalian genomic compositions. Finally, the small ORF exploration identified 2 candidate ORFs on chromosome A1 (CM034416.1), demonstrating how ab initio codon searches locate potential translation segments. However, this method is limited because it identifies theoretical reading frames without accounting for eukaryotic intron splicing, regulatory machinery, or verified in vivo transcription.
