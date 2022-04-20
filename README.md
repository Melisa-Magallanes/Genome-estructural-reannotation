# Genome-estructural-reannotation
Pipeline to reannotate an existant genome with RNAseq data as evidence

# Contents
# RNAseq sample preparation

In order to check RNA seq samples quality, first some parameters should be analyzed through FastQC
https://www.bioinformatics.babraham.ac.uk/projects/fastqc/

The total FastQC results can be aggregated using MultiQC
https://github.com/ewels/MultiQC

The adapter contamination should be removed with an adapter trimmer of reads such us TrimGalore
https://github.com/FelixKrueger/TrimGalore

# De novo transcriptome assembly
Trinity assembles transcript sequences from llumina RNA-Seq data. If your job is going to run on a server we suggest better use the Docker image with no additional installation required
https://github.com/trinityrnaseq/trinityrnaseq/wiki/Trinity-in-Docker

example command: 
Trinity --seqType fq --samples_file samples.txt --SS_lib_type RF --CPU 60 --max_memory 450G

where samples.txt is a tab-delimited text file indicating biological replicate relationships

# Transcriptome annotation
https://github.com/Trinotate/Trinotate
trinotateR is an R package to summarize annotation reports from Trinotate.
https://github.com/cstubben/trinotateR


# Genome re-annotation
Funannotate is a genome prediction, annotation, and comparison software package. It was originally written to annotate fungal genomes (small eukaryotes ~ 30 Mb genomes), but has evolved over time to accomodate larger genomes. 
https://github.com/nextgenusfs/funannotate

We strongly encourage you to follow the tutorial as described here, don't skip any step 
https://funannotate.readthedocs.io/en/latest/tutorials.html#tutorials

As we recommended for Trinity, the Funannotate docker image will be the best option to run jobs in remote servers

And luckily you will finally have as a result a better genome annotation at the end.
# Aditional tools
https://github.com/nanoporetech/spliced_bam2gff
https://github.com/DaehwanKimLab/hisat2
https://github.com/gpertea/stringtie

# Citation 
