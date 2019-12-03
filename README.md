# README

This repository contains the dataflow and scripts I used to process the COI metabarcode reads in the paper Porter and Hajibabaei, 2019 "What’s in a name?  Barcodes, mini-barcodes, metabarcodes".

Infiles and scripts can be downloaded from https://github.com/terrimporter/PorterHajibabaei_DNAbarcodes/releases .

## Infiles

Taxonomically assigned data were obtained for ESVs (LV2016_2.tar.gz) and for OTUs (LV2016_4.tar.gz) from the publication Porter et al., 2019 SciRep at https://github.com/terrimporter/PorterEtAl2019grid. 

Taxonomic information from BOLD data releases (iBOL_phase2.0_COI.tsv to iBOL_phase_6.50_COI.tsv) was obtained from http://v3.boldsystems.org/index.php/datarelease and parsed to include only taxonomic information from sequences at least 500 bp in length and with no more than 3 ambiguous bases (headers.txt).

Taxonomic information from eukaryote COI sequences mined from the NCBI nucleotide database [April 2019] and parsed to include only taxonomic information from sequences at least 500 bp in length with no ambiguous bases (headers2.txt).

Taxonomic information from BOLD data releases and eukaryote COI sequences (headers3.txt).

A summary report of the BOLD data releases, eukaryote COI NCBI nucleotide sequences, and the combined dataset (dbase_rank.csv). 

ESVs taxonomically assigned using a reference database based on BOLD data releases only (cat.denoised.out_BOLD).

ESVs taxonomically assigned using a reference database based on eukaryote COI sequences from the NCBI nucleotide database only (cat.denoised.out_NCBI).

ESVs taxonomically assigned using a reference database based on BOLD+NCBI COI sequences (cat.denosied.out_NCBI_BOLD_merged).

## Scripts

Fig 2 - richness.R uses LV2016_2.csv and LV2016_4.csv and produces richness.pdf

Fig 3 - composition.R uses LV2016_2.csv and LV2016_4.csv and produces composition_method.pdf

Fig 4 - composition.R uses LV2016_2.csv and LV2016_4.csv and also produces composition_marker_family.pdf (and composition_marker_genus.pdf).

Fig 5 - betadiv.R uses LV2016_2.csv and LV2016_4.csv and can produce scree plots, stress plots, and NMDS_procrustes.pdf .

Fig 6 - databaseResolution.R uses headers.txt, headers2.txt, and headers3.txt to calculate the values in dbase_rank.csv .  Also uses dbase_rank.csv as well as cat.denoised.out_BOLD, cat.denoised.out_NCBI, and cat.denoised.out_NCBI_BOLD_merged to produce database_rank.pdf .

## References

Porter, T.M., Morris, D.M., Basiliko, N., Hajibabaei, M., Doucet, D., Bowman, S., Emilson, E.J.S., Emilson, C.E., Chartrand, D., Wainio-Keizer, K., Seguin, A., Venier, L.  (2019) Variations in terrestrial arthropod DNA metabarcoding methods recovers robust beta diversity but variable richness and site indicators.  Scientific Reports, 9: 18218.

## Acknowledgements

I would like to acknowledge funding from the Canadian government from the Genomics Research and Development Initiative (GRDI), Metagenomics-Based Ecosystem Biomonitoring (EcoBiomics) project.

Last updated: December 3, 2019
