# tasic2018_scrnaseq_pipeline

This single cell RNA-seq pipeline includes Quality Control, rRNA filtering, Genome Alignment using STAR and estimates gene expression levels by GenomeAlignment Package in R. 

This pipeline adapted from following study: [Paper](https://www.nature.com/articles/s41586-018-0654-5)

##### Steps:
  1. For Quality Control, we use FastQC to create qc outputs. There are optional read quality filtering (trimmomatic), read quality trimming (trimmomatic), adapter removal (cutadapt) processes available.
  2. STAR is used to count or filter out common RNAs (eg. rRNA, miRNA, tRNA, piRNA etc.). 
  3. STAR is used to align RNA-Seq reads to a genome. 
  4. SummarizeOverlaps is used to calculate gene counts. 

##### Program Versions:
  - Star v2.6.1 # don't upgrade me - 2.7X indices incompatible with iGenomes.
  - r-base=4.0.0
  - Samtools v1.3
  - Bedtools v2.29.2
  - Ucsc-wigToBigWig v377
  - Macs2 v2.1.2

##### Pipeline Container:
  * Docker: dolphinnext/tasic2018\_scrnaseq\_pipeline:1.0
  * GitHub: dolphinnext/tasic2018\_scrnaseq\_pipeline
