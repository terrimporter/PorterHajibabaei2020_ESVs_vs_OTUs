# README

This repository contains the dataflow and scripts used to process the COI metabarcode reads in the paper Porter and Hajibabaei, 2020 "Putting COI Metabarcoding in Context: The Utility of Exact Sequence Variants (ESVs) in Biodiversity Analysis". Frontiers in Ecology and Evolution, In press.

Infiles and scripts can be downloaded from https://github.com/terrimporter/PorterHajibabaei2020_ESVs_vs_OTUs/releases/tag/v1.1.0 .

## Infiles

Taxonomically assigned data were obtained for ESVs (LV2016_2.tar.gz) and for OTUs (LV2016_4.tar.gz) from the publication Porter et al., 2019 SciRep at https://github.com/terrimporter/PorterEtAl2019grid . 

Taxonomically assigned data (taxonomy.matrix) were obtained from the publication Hajibabaei et al., 2019 PLoS ONE at https://github.com/Hajibabaei-Lab/HajibabaeiEtAl2019 .

headers.txt parsed from:
Taxonomic information from BOLD data releases (iBOL_phase2.0_COI.tsv to iBOL_phase_6.50_COI.tsv) was originally obtained from http://v3.boldsystems.org/index.php/datarelease and parsed to include only taxonomic information from sequences at least 500 bp in length and with no more than 3 ambiguous bases.

headers2.txt parsed from:
Taxonomic information from eukaryote COI sequences mined from the NCBI nucleotide database [April 2019] and parsed to include only taxonomic information from sequences at least 500 bp in length, with no ambiguous bases, and complete binomial species names.  Records were checked for human and bacterial contaminants.  Eukaryotes only.

headers3.txt parsed from:
Taxonomic information from BOLD data releases and eukaryote COI sequences.  Parsed to include only taxonomic information from sequences at least 500 bp in length, with no more than 3 ambiguous bases, and complete binomial species names.

## Scripts

Fig1_richness.R uses LV2016_2.csv and LV2016_4.csv and produces Fig1.pdf

Fig2_composition.R uses LV2016_2.csv and LV2016_4.csv and produces Fig2.pdf

Fig3_heatmap.R uses taxonomy.matrix and produces Fig3.pdf

Fig4_NMDS_procrustes.R uses LV2016_2.csv and LV2016_4.csv and produces Fig4.pdf

Fig5_databaseResolution.R uses headers.txt, headers2.txt, and headers3.txt to produce Fig5.pdf 

## References

Hajibabaei et al., 2019. COI metabarcoding primer choice affects richness and recovery of indicator taxa in freshwater systems. PLoS ONE 14(9): e0220953.

Porter, T.M., Morris, D.M., Basiliko, N., Hajibabaei, M., Doucet, D., Bowman, S., Emilson, E.J.S., Emilson, C.E., Chartrand, D., Wainio-Keizer, K., Seguin, A., Venier, L.  (2019) Variations in terrestrial arthropod DNA metabarcoding methods recovers robust beta diversity but variable richness and site indicators.  Scientific Reports, 9: 18218.

## Acknowledgements

I would like to acknowledge funding from the Canadian government from the Genomics Research and Development Initiative (GRDI), Metagenomics-Based Ecosystem Biomonitoring (EcoBiomics) project.

Last updated: July 23, 2020
