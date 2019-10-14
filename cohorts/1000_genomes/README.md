# 1000 genomes sample quality control and outlier identification
* Here we are doing some basic QC and identifying samples with large chromosomal anomolies for use in testing. 
* We are mostly doing direct analysis on normalized, binned depth data
* The methods here follow from Canvas CNV calling depth binning convention, updated to fit within the (very similar) Dragen CNV calling paradigm. For a detailed description of the Canvas depth binning method see Section 5.1 of the software design description ([link](https://github.com/Illumina/canvas/raw/master/SoftwareDesignDescription.pdf)).  

This repository contains a number of descriptive pages with methods as well as plots of flagged samples. Data files accompany this repository, which give more detailed and programatically accessable information. If any additional details are required, please post an issue on the github issue tracker page, and we will do our best to respond as soon as reasonable.  

_All filters used on this dataset are summarized in: [data/filters.csv](./data/filters.csv)._


####  [Sample metadata](./1kg_sample_metadata.md)
This contains sample-level informtion about the cohort. This includes:
* Genome-wide coverage information
* Quantification of replication timing and GC bias
* Quantification of depth variance
* A list of 92 samples filtered due to having a high depth variance  

####  [Chromosome level events](./chromosome_level_events.md)
This contains a summary of large events int he cohort. This includes:
* Per sample, chromosome level coverage
* Karyotype-band level coverage
* 28 samples with a full chromosomal alteration (autosomes only, [plots of samples](./chromosome_level_events_trisomies.md))
* 67 samples with large chromosomal alteration spanning at lease two bands (autosomes only, [plots of samples](./band_level_events.md))   

#### [Sex chromosome events](./sex_chrom_overview.md)  
This is a summary of sex chromosome coverage across the cohort. This includes: 
* Sample sex chromsome coverage
* 7 male samples with y-chromosome dropout ([plots of samples](./y_chrom_dropout.md))
* 3 male samples with mosaic y-chromosome gain ([plots of samples](./y_chrom_gain.md))
* 32 female samples with x-chromosome dropout ([plots of samples](./x_chrom_loss.md))
* 5 female samples with x-chromosome gain ([plots of samples](./x_chrom_gain.md))

#### [Uniparental isodisomy events](1kg_sample_UPD.md) 
This is a list of 5 curated samples with UPD or mosaic UPD. 
