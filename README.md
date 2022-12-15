# ngs-pipe

Part 2 (chromID):
[click here to view chromid analysis html file](https://htmlpreview.github.io/?https://github.com/ioneliabuzatu/ngs-pipe/blob/main/chromid_analysis.html)

The analysis consits of:

    0. Data and task
        - download it
        - get fastqc files
        - quality control
    1. Reads downsampling (later use)
        - to 7M
    2. Trimming
        stats after trimming
    3. Alignment
        - stats after alignment
    4. Remove Duplicates
    5. Remove blacklist sequences
    6. Peak Calling
         - convert broadPeaks to bed format
    7. Genome Wide Coverage Plot
        - IGV
    8. Heatmaps peaks
         - visualize the peak calling bed files
    9. Compare peaks - author vs reproduced
    10. Redo comparison after removing duplicates and blacklist
    

Part 1 (tutorial):
[click here to see tutorial data analysis HTML file](https://htmlpreview.github.io/?https://github.com/ioneliabuzatu/ngs-pipe/blob/main/ngs_pipeline.html)

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
    8. Differential Analysis [e.g. find markers]
    
    
