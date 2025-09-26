
# Data processing and quality control

## Data processing

[FastQC](http://www.bioinformatics.babraham.ac.uk/projects/fastqc/) (ver 0.11.8)  was used to evaluate the overall quality of the downloaded data, followed by the use of  [Trimmomatic](http://www.usadellab.org/cms/?page=trimmomatic)  to remove vector sequences and low-quality bases. <!--Sequences shorter than 2/3 of the original read length were removed from subsequent analysis.--> The remaining sequences were referred to as `clean data` and used for subsequent analysis.

[Seqtk](https://github.com/lh3/seqtk) was used to convert sequences from FASTQ to FASTA.

## Quality control

Two rounds of quality control procedures were applied.  
First, for the 16S data, samples (runs) with less than 20,000 `clean reads` were removed from subsequent analysis, and marked as "failed QC (QC status = 0)" in **GMrepo**.

Then, after taxonomy assignment, samples containing only a single taxon (i.e., a species or genus accounting for more than 99.99 percent of total abundance) were marked as "failed QC (QC status = 0)".

## Taxonomic assignment to the sequenced reads

For `16S amplicon sequences`, [QIIME2](https://qiime2.org/) was used to analyze the obtained `clean data` and assign taxonomic classification information to the reads.  
`ASV` (Amplicon Sequence Variant) instead of `OTU` (Operational Taxonomic Units) results were used, as the former can provide more precise measurement of sequence variation and allow easier comparisons between different studies (tractability and reproducibility). [Wikipedia: ASV](https://en.wikipedia.org/wiki/Amplicon_sequence_variant)  
Relative abundances were then calculated for each sample, summing to 100%.

For whole genome (i.e., metagenomic or mNGS) sequences, [MetaPhlAn4](http://segatalab.cibio.unitn.it/tools/metaphlan2/) was used with default parameters for the taxonomic classification of the sequencing reads.

## Identification of taxon co-occurrence

Co-occurred taxa can be functionally relevant. In **GMrepo**, co-occurred taxon pairs were identified for health and each disease separately.

Two taxa (i.e., either two species or two genera) were considered **co-occurred** in a disease (e.g., Crohn's disease) associated samples if they met **all** the following criteria:

- A `Fisher's exact test` was used to calculate the odds of the two taxa to co-occur in the disease-associated samples/runs based on their presence/absence information.  
  A taxon was considered present in a sample/run if its relative abundance was higher than 0.01%.  
  A p-value and odds ratio (OR) were reported for each pair. Pairs with p-value < 0.05 were selected.  
  The `fisher.test()` function implemented in R was used.

- `Pearson correlation` analysis was applied to the relative abundances of the two taxa in disease-associated samples. Pairs with a p-value < 0.05 were selected.

- `Spearman correlation` analysis was also applied to the relative abundances of the two taxa in disease-associated samples. Pairs with a p-value < 0.05 were selected.

