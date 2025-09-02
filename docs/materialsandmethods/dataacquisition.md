
## Raw sequencing data

Raw data, including sequences in FASTQ format were obtained from the following public databases:

* <a href="https://www.ebi.ac.uk/ena/browse" target="_blank">ENA (European Nucleotide Archive)</a> at <a href="https://www.ebi.ac.uk/" target="_blank">EBI (European Bioinformatics Institute)</a> of <a href="https://www.embl.de/" target="_blank">EMBL (European Molecular Biology Lab)</a>,
* <a href="https://www.ncbi.nlm.nih.gov/sra" target="_blank">SRA (Sequence Read Archive) database</a> at <a href="https://www.ncbi.nlm.nih.gov/" target="_blank">NCBI (National Center for Biotechnology Information)</a>,
* <a href="https://www.hmpdacc.org/" target="_blank">HMP (Human Microbiome Project)</a>, 
* <a href="http://americangut.org/" target="_blank">AGP (American Gut Project)</a>.

Data were downloaded using <a href="https://github.com/enasequence/enaBrowserTools" target="_blank">enaBrowserTools</a> and <a href="https://github.com/ncbi/sra-tools" target="_blank">SRA-Tools</a> facilitated by Aspera (a high-speed data transfer tool).

## Meta data

Meta-data were first extracted using in-house R/Python scripts and then manually curated at least two-rounds to ensure the quality. Meta-data curation was not painless because sometimes such information were often incomplete, misplaced or even completely missing. Very often we had to consult the description of the samples, supplementary data of related publications or sometimes even the authors.

Technical meta-data extracted include:

* experiment type (16S or Metagenomics),
* sequencing devices / instruments, 
* number of obtained sequencing reads.

Host-related, biological-relevant meta-data extracted include:

* disease or health of the host (refered as to <code>phenotype</code> in our database),
* age,
* sex,
* BMI (body mass index), 
* antibiotic usage.

More meta-data will be added in the future.

