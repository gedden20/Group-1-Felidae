<div align="justify">
# Felidae Phylogenetic Analysis

Course:
Cell and Molecular Biology Laboratory

Group Number: one (1)
_____

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

This study examines the evolutionary relationships among selected members of the family Felidae using mitochondrial COX1 gene sequences. The ingroup consists of three species from the genus Felis (*Felis catus*, *Felis chaus*, and *Felis silvestris*) and two species from the genus Panthera (*Panthera pardus* and *Panthera tigris*). *Vulpes vulpes* (red fox) was included as the outgroup to root the phylogenetic tree.

Taxonomic Hierarchy

Kingdom: Animalia

Phylum: Chordata

Class: Mammalia

Order: Carnivora

Family: Felidae

Genera: Felis, Panthera

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

<img width="490" height="240" alt="consensus_sequence" src="https://github.com/user-attachments/assets/5d910b0a-6a03-45a4-834f-12736990512b" />

<img width="810" height="441" alt="Phylogenetic_tree" src="https://github.com/user-attachments/assets/8dd3312f-0952-49ce-add2-bf5d11f57564" />

<img width="644" height="513" alt="Galaxy_workflow" src="https://github.com/user-attachments/assets/6a285135-f671-4620-aa27-214e5ba240d9" />



<div align="justify">
