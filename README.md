# Felidae Phylogenetic Analysis

Course:
Cell and Molecular Biology Laboratory

Group Number: 1


Members:
- Ansag,Eugene Kim
- Estrevillo, Gedden
- Lisondra, Ray Gee
- Martinez, Jen Marie
- Ortega, Jerson Lloyd

Taxonomic Group:
Felidae

Gene Used:
COI

This repository contains the documentation of our phylogenetic analysis conducted using NCBI and Galaxy.

## Project Overview

Reconstructing evolutionary relationships among taxa is a fundamental objective of systematic biology, providing crucial insights into lineage divergence, adaptive radiation, and biodiversity. Modern molecular phylogenetics relies on nucleotide sequence variation in targeted genetic markers to infer common ancestry across evolutionary time scales. 

Among these markers, the mitochondrial cytochrome c oxidase subunit I (COI/COX1) gene is widely utilized because of its maternal inheritance, low rate of recombination, and optimal balance between conserved and variable regions. These characteristics make COI a valuable molecular marker for species identification through DNA barcoding and for investigating evolutionary relationships among closely related taxa.

This study addresses the primary biological question: To what extent can mitochondrial COX1 nucleotide sequences accurately infer the phylogenetic relationships among selected species of the family Felidae? By evaluating the resulting phylogenetic tree, the study also examines the strengths and limitations of using a single mitochondrial marker for evolutionary inference.

## Taxonomic Group

This study examines the evolutionary relationships among selected members of the family Felidae using mitochondrial COX1 gene sequences. The ingroup consists of three species from the genus *Felis* (*Felis catus*, *Felis chaus*, and *Felis silvestris*) and two species from the genus *Panthera* (*Panthera pardus* and *Panthera tigris*). *Vulpes vulpes* (red fox) was included as the outgroup to root the phylogenetic tree.

Taxonomic Hierarchy

Kingdom: Animalia

Phylum: Chordata

Class: Mammalia

Order: Carnivora

Family: Felidae

Genera: *Felis*, *Panthera*

Species Included

*Felis catus* (Domestic cat)

*Felis chaus* (Jungle cat)

*Felis silvestris* (European wildcat)

*Panthera pardus* (Leopard)

*Panthera tigris* (Tiger)

Outgroup: *Vulpes vulpes* (Red fox)

## Methods 

**Reconstructing Evolutionary Relationships Using Mitochondrial COX1**

Objective: Retrieve authentic mitochondrial cytochrome c oxidase subunit I (COI/COX1) sequences from NCBI, align them in Galaxy, examine a consensus sequence, construct a phylogenetic tree, and compare the resulting relationships with published studies.

**Sequence Retrieval from NCBI**

Mitochondrial cytochrome c oxidase subunit I (COX1) nucleotide sequences were retrieved from the National Center for Biotechnology Information (NCBI) Nucleotide database. Each target species was searched individually using the organism name together with the keywords "COX1" and "mitochondrion." Sequence records were verified to ensure they corresponded to the mitochondrial COX1 gene, represented homologous regions, and had comparable sequence lengths. The accession number, sequence length, and record title of each selected sequence were recorded. All sequences were downloaded in FASTA format without modifying the nucleotide sequences.
            
**Data Preparation in Galaxy**

The downloaded FASTA sequences were uploaded to the Galaxy platform (https://usegalaxy.org) using a dedicated analysis history. Individual FASTA files were combined into a single multi-FASTA dataset containing one sequence for each species. FASTA headers were renamed with short, unique species labels to improve readability in the final phylogenetic tree while preserving the original sequence data.
     
**Multiple Sequence Alignment**

Because the MUSCLE alignment tool was unavailable on the Galaxy server, multiple sequence alignment was performed using MAFFT, an alternative alignment program integrated into Galaxy. The combined multi-FASTA dataset was used as the input, and the default alignment parameters were applied. The resulting alignment was inspected to confirm that homologous nucleotide positions were properly aligned and to identify any sequences with poor alignment, excessive missing data, incorrect orientation, or evidence of non-homologous regions. The finalized aligned dataset was used for all subsequent analyses.
        
**Consensus Sequence Generation**

A consensus sequence was generated from the MAFFT alignment using the consensus sequence tool available in Galaxy with the default majority-rule settings. The resulting consensus sequence was examined to determine its length and to identify conserved and variable nucleotide sites across the aligned sequences. The consensus sequence served only as a summary of the alignment and was not used for phylogenetic tree construction.
      
**Phylogenetic Tree Construction**

Phylogenetic relationships among the selected taxa were inferred using the FastTree tool in Galaxy. The aligned COX1 nucleotide sequences produced by MAFFT were used as the input, with nucleotide sequence analysis selected where applicable. FastTree generated a phylogenetic tree in Newick format, which was visualized using a compatible tree viewer. Species labels were checked for clarity, and the designated outgroup was used to aid in rooting and interpreting the evolutionary relationships among the sampled taxa.

## Figures

A consensus mitochondrial COX1 gene sequence derived from multiple Felidae species, representing the most frequent nucleotide at each aligned position.

<img
            width="490" height="240" alt="consensus_sequence" src="https://github.com/user-attachments/assets/5d910b0a-6a03-45a4-834f-12736990512b" 
            />

***Figure 1.*** Consensus sequence 

Phylogenetic tree showing the evolutionary relationships among Felidae species based on mitochondrial COX1 gene sequence similarities.

<img 
            width="810" height="441" alt="Phylogenetic_tree" src="https://github.com/user-attachments/assets/8dd3312f-0952-49ce-add2-bf5d11f57564" 
            />

***Figure 2.*** Phylogenetic tree

A Galaxy workflow showing the steps used to analyze COX1 sequences, including alignment, consensus sequence, and phylogenetic tree creation.

<img 
            width="1874" height="1280" alt="Galaxy_workflow" src="https://github.com/user-attachments/assets/41087e6f-91fb-47c0-a4b1-d6fe86b937b4" 
            />

***Figure 3.*** Galaxy workflow


## Discussion & Comparison with Published Studies

To evaluate the accuracy of the phylogenetic relationships inferred from the mitochondrial cytochrome c oxidase subunit I (COX1) gene, the resulting phylogenetic tree was compared with the phylogenomic study of Li et al. (2016), which reconstructed the evolutionary history of extant Felidae using genome-wide nuclear DNA, complete mitochondrial genomes, and sex chromosome markers. Unlike the present study, which relied solely on a single mitochondrial marker (COX1), Li et al. (2016) employed a comprehensive genomic dataset to resolve evolutionary relationships and investigate the effects of historical hybridization among felid lineages.

The COX1 phylogenetic tree recovered two well-supported monophyletic clades corresponding to the genera *Felis* and *Panthera*. The *Felis* clade comprised *Felis chaus*, *Felis silvestris*, and *Felis catus*, whereas the *Panthera* clade consisted of *Panthera tigris*, *Panthera uncia*, and *Panthera pardus*. This topology is consistent with the phylogeny presented by Li et al. (2016), which recognized both genera as distinct evolutionary lineage within the family Felidae. The placement of *Vulpes vulpes* outside the Felidae clade further supports the use of the red fox as an appropriate outgroup for rooting the phylogenetic tree.

Within the *Felis* clade, the present study recovered *Felis silvestris* and *Felis catus* as sister taxa, supported by a local support value of 0.994, while *Felis chaus* diverged earlier within the clade. This relationship agrees with Li et al. (2016), who identified domestic cats and wildcats as members of the Domestic Cat lineage and demonstrated their close evolutionary affinity using genome-scale molecular data. The concordance between the COX1 phylogeny and the genome-wide analysis indicates that the mitochondrial COX1 gene effectively resolves evolutionary relationships among closely related members of the genus *Felis*.

Similarly, the *Panthera* clade was recovered as a distinct monophyletic lineage. In the present analysis, *Panthera uncia* and *Panthera pardus* formed a sister group with a support value of 0.859, whereas *Panthera tigris* diverged earlier within the clade. This overall grouping agrees with Li et al. (2016), which consistently recognized *Panthera* as a natural evolutionary lineage. However, Li et al. (2016) reported that the internal relationships among *Panthera* species may vary depending on whether mitochondrial or nuclear genomic datasets are analyzed because ancient hybridization and incomplete lineage sorting have influenced the evolutionary history of the genus. Consequently, slight differences in the branching order among *Panthera* species between the two studies are expected.

The observed similarities indicate that the mitochondrial COX1 gene retains sufficient phylogenetic signal to recover the major evolutionary divisions within Felidae, particularly at the genus level. Nevertheless, several methodological differences explain the minor discrepancies between the present study and the published phylogeny. First, the current analysis utilized only a single mitochondrial locus inherited maternally, whereas Li et al. (2016) integrated information from genome-wide nuclear markers, complete mitochondrial genomes, and sex chromosomes, providing substantially greater phylogenetic resolution. Second, the published study included 38 extant felid species, while the present analysis examined only six felid species and one canid outgroup, limiting taxonomic representation. Finally, Li et al. (2016) demonstrated that historical hybridization among ancestral felid lineages contributed to discordance between mitochondrial and nuclear phylogenies, a phenomenon that cannot be fully resolved using a single mitochondrial marker.

Overall, the COX1-based phylogenetic tree generated in the present study is highly consistent with the comprehensive phylogenomic framework proposed by Li et al. (2016). Both studies support the separation of *Felis* and *Panthera* into distinct monophyletic lineages and the close relationship between *Felis catus* and *Felis silvestris*. The minor differences observed within the *Panthera* clade most likely reflect the greater resolving power of genome-wide datasets compared with a single mitochondrial gene. Thus, despite its limited genetic scope, the COX1 marker proved effective for reconstructing the major evolutionary relationships among the selected felid species.

### Utility, Limitations, and Caveats of Using COX1 Alone

The COX1 gene is widely accepted as a useful marker for DNA barcoding because it is easy to amplify, shows relatively high variation between species but low variation within species, and is backed by large reference databases. Studies also support its usefulness as a fast and practical first-step tool for species identification in many animal groups.

However, there is also strong disagreement about using COX1 alone for phylogenetic inference. Many authors note that mitochondrial markers can give misleading results when there is introgression, hybridization, incomplete lineage sorting, or the presence of nuclear mitochondrial pseudogenes (NUMTs), because the resulting gene tree may not match the true species tree. In some taxa, COX1 also performs poorly because it does not provide enough resolution or does not amplify consistently, which limits its usefulness outside standard barcoding contexts.

The main limitation of COX1 is that it is a single mitochondrial locus, so it reflects only the maternal lineage and not the full evolutionary history of an organism. Because mitochondrial DNA is non-recombining and maternally inherited, it can be useful for simplifying analyses, but it can also bias interpretation when species histories are complex. COX1 is also subject to functional constraints because it encodes part of a protein involved in respiration, which means its sequence evolution is not always neutral and may be affected by selective pressure.

For these reasons, the most supportable conclusion is that COX1 is excellent for preliminary identification and biodiversity screening, but it should not be used alone for strong phylogenetic conclusions. Many studies recommend combining COX1 with nuclear markers or multilocus datasets to improve accuracy and reduce the risk of misleading results.

## References

Chee S. Y. (2015). Limitations of cytochrome oxidase I for the barcoding of Neritidae (Mollusca: Gastropoda) as revealed by Bayesian analysis. *Genetics and Molecular Research : GMR*, 14(2), 5677–5684. https://pubmed.ncbi.nlm.nih.gov/26125766/


Lee, S., Chesters, D., & Vogler, A. P. (2026). Organelle genomes as universal standard for phylogenetics: a sociotechnical perspective. *Trends in ecology & evolution*, 41(5), 395–403. https://doi.org/10.1016/j.tree.2026.01.004


Li, G., Davis, B. W., Eizirik, E., & Murphy, W. J. (2016). Phylogenomic evidence for ancient hybridization in the genomes of living cats (Felidae). *Genome Research*, 26(1), 1–11. https://doi.org/10.1101/gr.186668.114


National Center for Biotechnology Information. Nucleotide: FJ185310.1 *Felis catus* cytochrome c oxidase subunit I (COX1) gene, partial cds; mitochondrial. Accessed [July 28, 2026]. https://www.ncbi.nlm.nih.gov/nuccore/FJ185310.1


National Center for Biotechnology Information. Nucleotide: OR150429.1 *Felis chaus* isolate JC1 cytochrome c oxidase subunit I (COX1) gene, partial cds; mitochondrial. Accessed [July 28, 2026]. https://www.ncbi.nlm.nih.gov/nuccore/OR150429.1


National Center for Biotechnology Information. Nucleotide: OR178528.1 *Felis silvestris* isolate T2211 cytochrome c oxidase subunit I (COX1) gene, partial cds; mitochondrial. Accessed [July 28, 2026]. https://www.ncbi.nlm.nih.gov/nuccore/OR178528.1


National Center for Biotechnology Information. Nucleotide: PP527113.1 *Panthera pardus* voucher 28OY cytochrome c oxidase subunit I (COX1) gene, partial cds; mitochondrial. Accessed [July 28, 2026]. https://www.ncbi.nlm.nih.gov/nuccore/PP527113.1


National Center for Biotechnology Information. Nucleotide: KP992945.1 *Panthera tigris* isolate PT1 cytochrome oxidase subunit I (COX1) gene, partial cds; mitochondrial. Accessed [July 28, 2026]. https://www.ncbi.nlm.nih.gov/nuccore/KP992945.1


National Center for Biotechnology Information. Nucleotide: ON377296.1 *Panthera uncia* isolate MGL-306 cytochrome c oxidase subunit I (COX1) gene, partial cds; mitochondrial. Accessed [July 28, 2026]. https://www.ncbi.nlm.nih.gov/nuccore/ON377296.1


National Center for Biotechnology Information. Nucleotide: PP527100.1 *Vulpes vulpes* voucher 1HQU cytochrome c oxidase subunit I (COX1) gene, partial cds; mitochondrial. Accessed [July 28, 2026]. https://www.ncbi.nlm.nih.gov/nuccore/PP527100.1


‎‎Pentinsaari, M., Salmela, H., Mutanen, M., & Roslin, T. (2016). Molecular evolution of a widely-adopted taxonomic marker (COI) across the animal tree of life. *Scientific Reports*, 6, Article 35275. https://doi.org/10.1038/srep35275


Souza, H. V., Marchesin, S. R. C., & Itoyama, M. M. (2016). Analysis of the mitochondrial COI gene and its informative potential for evolutionary inferences in the families Coreidae and Pentatomidae (Heteroptera). *Genetics and Molecular Research*, 15(1), Article gmr.15017428. https://pubmed.ncbi.nlm.nih.gov/26909963/


Yu, J., Yu, X., Bi, W., Li, Z., Zhou, Y., Ma, R., ... & Liu, J. (2025). Mitogenome diversity and phylogeny of Felidae species. *Diversity*, 17(9), 634.https://www.semanticscholar.org/paper/Mitogenome-Diversity-and-Phylogeny-of-Felidae-Yu-Yu/a214e798a96cbf5a03629ab7b59137856634d3bc



