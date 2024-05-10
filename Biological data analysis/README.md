# Prostate Cancer Transcriptome Analysis

## Table of Contents
- [Project Overview](#project-overview)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Findings](#findings)

### Project Overview
This data analysis project aims to uncover molecular mechanisms underlying disease progression and treatment 
resistance of Prostate Cancer.

### Data Sources

Genomic data:  Transcripts data were obtained from an RNA-seq experiment. Available as 'RNA_expressions.RDS' file.

### Tools

- R - Data cleaning - Data Analysis - Creating reports

### Data cleaning/ Preparation

In the initial phase, we performed the following tasks:
1. Data loading and inspection
2. Data normalization

### Exploratory Data Analysis

EDA involved exploring the transcript data to answer key questions, such as:

- Are the sample groups clustered as the way we expect?
- What are the differential expressed (DE) genes between the two sample groups?
- Any interesting biological information derived from KEGG analysis that can be relevant to 
 the differences between PC and CRPC?

### Data analysis

Include some interesting code/ features work with

### Findings

The analysis results are summarized as follow:

Differential espression analysis was carried out using DESqe. Student t’test was chosen for the statistical
 test.
![volcano plot displaying genes with differences of means and -log10(p_vlaues)](https://github.com/chinguyen19/Bioinformatics-projects/assets/66997827/09b32518-6940-43a7-aeb5-7c1539f8887e)

PCA analysis was performed to visualize the variance per component. Different level of espression for the two groups was clearly observed. 
![heatmap](https://github.com/chinguyen19/Bioinformatics-projects/assets/66997827/767a7076-7397-4fb3-99ae-de200d4a85f2)

 KEGG pathway enrichment is performed using the list of differentially expressed genes identified implying potential biological processes
 associated with the observed gene expression change. 
 
![enriched pathways](https://github.com/chinguyen19/Bioinformatics-projects/assets/66997827/a41f7091-60a7-4b47-92eb-a01475de51d0)

There are 2 samples (PC 6864 and PC 9324) from PC group that fell far away from their group, which is confirmed by the following PCA analysis. Thus, these 2 samplesare outliers which can represent different in biological sense compared to the PC group. According to the Cancer research, it is likely that these samples share the molecular characteristics with CRPC because of some specific genetic alterations that might lead to different molecular pathways.
