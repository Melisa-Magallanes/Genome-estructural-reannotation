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
https://github.com/nextgenusfs/funannotate
https://github.com/nanoporetech/spliced_bam2gff
# Citation 
