# ngs-pipe

[click here to see data analysis HTML file](https://htmlpreview.github.io/?https://github.com/ioneliabuzatu/ngs-pipe/blob/main/ngs_pipeline.html)

The analysis consits of:

    1. Data
        - Download samples form SRA database
        - Get fastq file and split each paired-read in left and right read
    2. Quality Control [see if you need to remove some reads]
    3. Alignment
        - align each replicate sample to reference genome [bowtie2 -> sam file output!]
        - spike-in calibration [for later use to normalize - bowtie2 -> sam file output! - optional]
        - alignment statistics
        - visualize sequencing depth an alignment stats
        - remove duplicates [based on quality control and alignment outputs - optional] 
        - fragments size analysis
    4. SAM -> BED conversion
        - bin samples into 500 bp [output bed file]
        - assess replicates reproducibility
    5. Spike-in calibration [bed -> bedgraph]
        - get seqdepth for each sample
        - generate normed bedgraph file formats 
        - analysis and visualiaze scale factor effect
    6. Peak Calling [bedgraph -> peaks]
    7. Visualization 
        - igv visualization [bedgraphs(normed) into igv]
        - heatmap peaks
    8. Diffenrential Analysis [e.g. find markers]