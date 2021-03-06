## Microbiome analysis (V4 region of 16S rRNA gene) of Caribbean nursery-reared <i>Acropora cervicornis</i> 

### Essential Packages, see complete list in R script
* [dada2](https://bioconductor.org/packages/release/bioc/html/dada2.html)
* [phyloseq](https://joey711.github.io/phyloseq/) 
* [vegan](https://cran.r-project.org/package=vegan)
* [CoDaSeq](https://github.com/ggloor/CoDaSeq)

### Description
This project involves the analysis of microbiomes of ocean nursery-reared <i>Acropora cervicornis</i> at the Central Caribbean Marine Institute, looking at the distribution of microbiome content across coral colonies. The sequencing reads with primers and adaptors removed by cutadapt are available in NCBI’s Sequence Read Archive under Bioproject [PRJNA495377](https://www.ncbi.nlm.nih.gov/bioproject/PRJNA495377). This repository includes the R script to recreate the figures in Miller et al submitted to PeerJ, and the original metadata, ASV, and taxonomy tables from our analysis. The file of session information provides all of the versions of the packages used in R to complete the analysis in [Miller et al 2020](https://peerj.com/articles/9635/). The provided ASV and taxonomy tables are the original files provided by the dada2 analysis. The script includes using phyloseq to remove chloroplast and mitochondrial reads, as well as using R to fill in empty or "NA" cells in the taxonomy with the lowest taxonomy assignment available. Please note that if the dada2 analysis is repeated, it will result in a slightly different ASV table every time, although the overall interpretations will remain the same. Analysis includes determining the amplicon sequence variants (ASVs) with dada2, assigning taxonomy with the Silva database v.132, and community composition analysis with a combination of phyloseq, vegan, and CoDaSeq tools. The ANCOM function is used in R for community analysis (not available as an R package).
