# huedseqs
 #### As we all know, it is very valuable and difficult to work with patient samples in cognitive disorders such as ASD and Alzheimer's. Therefore, it is very important to reach accurate and interpretable results quickly, to be universally applicable to the analyzes and to routinely apply these analyzes in terms of providing new opportunities for the treatment of these diseases.
 #### We have created this tool that combines the protocol and tools used for RNA samples collected and isolated for children with ASD and control groups that we work with in our own laboratory.And because we love color visualizations at the end, we named this tool "huedseqs"
 #### We created this tool to achieve a standard for all filters and analysis, and to use it for follow-up work in our own laboratory. The steps to follow are as follows;
 1. Obtained raw Fastq Files
 2. Quality control by using Fastp tool
 3. SAM file formation by using BWA
 4. BAM file formation by using Samtools
 5. Indexing BAM file by using Samtoools
 6. Transcript expression Quantification
 7. Differential Expression Analysis
 8. Functional Annotation Analysis
 9. Heatmap formation
 10. Visualization by using MLCut

 ### The details of these steps are as follows:
 #### Quality Control by using fastp 
 The tool [fastp](https://github.com/OpenGene/fastp#fastp) will be used for quality control and threshold value will be taken greater than 30. 
 #### SAM and BAM file formation
 The fastq files of the samples that passed the quality control are aligned to the reference genome (GRCh38.p13 (GCA_000001405.28) with the Burrows-Wheeler Alignment (BWA-mem) tool and files in the Sequence Alignment Map (SAM) format are obtained by using [BWA tool](https://github.com/lh3/bwa).
 #### Indexing BAM files
 These files are converted to Binary Alignment Map (BAM) format using SAMtools and then the obtained BAM files are indexed (by coordinate) with [SAMtools](http://www.htslib.org). 
 #### Transcript Expression Quantification
 Different methods can be used for transcript expression quantification, and the [RSEM](https://github.com/deweylab/RSEM) tool is used for standardization and ease of use.
#### Functional Annotation Analysis
For functional annotation, the [GO FEAT](https://github.com/fabriciopa/gofeat) tool is used for all of us to use it easily and for interface convenience.
#### Visualization
Finally, the [MLCUT](https://bivi.co/visualisation/mlcut) tool is used to further enrich the visualization. 
 
 
