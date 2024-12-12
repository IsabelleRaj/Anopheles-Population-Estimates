# Comparing estimates of historical and contemporary effective population size (_Ne_)

This repository contains all the code written for my biological sciences undergraduate final year project (FYP) at Imperial College London. The aim of this project is to use the genomic data from the _Anopheles gambiae_ 1000 Genomes (Ag1000G) Project phase 3 dataset from MalariaGEN to compare two estimates of _Anopheles coluzzii_ effective population sizes (_Ne_): historical and contemporary _Ne_.

Mosquitos of the _Anopheles gambiae species complex_ are vectors of diseases like malaria, a life-threatening disease with over millions of annual cases globally. Estimates of _Anopheles spp._ population sizes is key for vector control strategies e.g., to monitor the success of an intervention such as insectides, but also to determine the necessary amount of intervention required such as for gene-drive technology.

All code was run on R (version 3.6.1) or Python (version 3.9.13). The malariagen_data (version 3.0.0) (https://github.com/malariagen/malariagen-data-python) and scikit-allel (version 1.3.5) (https://github.com/cggh/scikit-allel) Python packages were used primarily. Pandas, Numpy and Matplotlib were also extensively used. 

Skills used: Data manipulation, creating functions, project documentation, mathematical operations, data visualisation.

## Description of Files
In the code folder, there are several notebook which perform a different task of the project. These are listed below:

### (1) - Exploring the metadata
* Install and import the MalariaGEN API (malariagen_data).
* Explore metadata and select the study location (*An.coluzzii* in Niono, Mali, 2013-2015).

### (2) - Diversity
* Compute average nucleotide diversity statistics for chosen samples.
* Conduct sliding window analysis on the X and 3R chromosomes.
* Calculate historical *Ne*.
#### (2.1) - Diversity: Number of sites
* Calculate the number of genetic sites used to compute the diversity statistics.

### (3) - Drift
* Filter SNPs (single nucleotide polymorphisms) for biallelic and non-rare sites, as well as sites to avoid linkage disequilibrium (LD).
* Calculate the temporal _Fa_ statistic.
* Calculate contemporary _Ne_.
#### (3.1) - Drift: Randomisation
* Perform a randomisation test to plot the distribution of _Fa_ statistics.
#### (3.2) - Drift: Confidence intervals (CI)
* Calculate confidence intervals for the _Fa_ statistics and contemporary _Ne_.

## Acknowledgments
My sincere thanks to Dr Vassiliki Koufopanou and Dr Tin-Yu Hui for their guidance throughout the project and also Dr Jon Brenas and Josh Reynolds for their coding-related assistance.

