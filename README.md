# 🦟 Comparing estimates of historical and contemporary effective population size (_Ne_) of _Anopheles coluzzii_ 🦟

## Table of Contents
1. [Project Overview](#project-overview)
2. [Technical Setup](#technical-setup)
3. [Skills Used](#skills-used)
4. [Description of Files](#description-of-files)
5. [Acknowledgments](#acknowledgments)

## Project Overview
**This project aimed to derive two effective population sizes (_Ne_) estimates of _Anopheles coluzzii_ mosquitoes: historical _Ne_ and contemporary _Ne_, from genomic data.**

Mosquitos of the _Anopheles gambiae species complex_ are vectors of diseases like malaria, a life-threatening disease with over millions of annual cases globally. Estimates of _Anopheles spp._ population sizes is key for **vector control strategies** e.g., to monitor the success of an intervention such as insectides, but also to determine the necessary amount of intervention required such as for gene-drive technology.

## Installation
1. Open your command prompt.
2. Navigate to your desired directory.
3. Git clone this repository using the following command:
  ```bash
  git clone https://github.com/IsabelleRaj/Anopheles-Population-Estimates
  ```

## Usage
1. Open each notebooks:
  ```bash
  jupyter notebook "FYP - (1) Exploring the metadata.ipynb"
  jupyter notebook "FYP - (2) Diversity.ipynb"
  jupyter notebook "FYP - (2.1) Diversity number of sites.ipynb"
  jupyter notebook "FYP - (3) Drift.ipynb"
  jupyter notebook "FYP - (3.1) randomisation_F_R.ipynb"
  jupyter notebook "FYP - (3.2) CI_F (with Fa).ipynb"
  jupyter notebook "FYP - (3.2) CI_F.ipynb"
  ```

## Data Source
The genomic data was sourced from MalariaGEN's (_Anopheles gambiae_ 1000 Genomes (Ag1000G) Project phase 3 dataset)[https://www.malariagen.net/data_package/ag30-anopheles-gambiae-data-resource/], using the (MalariaGEN API)[https://malariagen.github.io/malariagen-data-python/latest/].  

 The aim of this project is to use the genomic data from the _Anopheles gambiae_ 1000 Genomes (Ag1000G) Project phase 3 dataset from MalariaGEN to compare two estimates of _Anopheles coluzzii_ effective population sizes (_Ne_): historical and contemporary _Ne_.


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
This project was conducted in 2023 for my BSc biological sciences final year project at Imperial College London. My sincere thanks to Dr. Vassiliki Koufopanou and Dr. Tin-Yu Hui for their invaluable guidance throughout the project. Thanks to Dr. Jon Brenas and Josh Reynolds for their assistance with coding.
