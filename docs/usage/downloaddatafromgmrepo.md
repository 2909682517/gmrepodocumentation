
# Data downloads


## Download processed data from **GMrepo**

| **File** | **Description** |
| -------- | --------------- |
| [Projects](https://gmrepo2025.humangut.info:8443/Downloads/SQLDumps/projects.txt.gz) | A list of projects and related information such as project description. |
| [Projects summary](https://gmrepo2025.humangut.info:8443/Downloads/SQLDumps/stats_by_phenotype_and_project.txt.gz) | A list of projects and information such as total numbers of associated runs, processed runs, valid runs and failed runs. |
| [All runs](https://gmrepo2025.humangut.info:8443/Downloads/SQLDumps/sample_to_run_info.txt.gz) | Information on runs/samples collected in this database, including their associated projects and other curated meta-data. | 
| [Processed runs](https://gmrepo2025.humangut.info:8443/Downloads/SQLDumps/samples_loaded.txt.gz) | A list of processed runs, tools used for analysis, and their QC statuses. |
| [Relative abundances](https://gmrepo2025.humangut.info:8443/Downloads/SQLDumps/species_abundance.txt.gz) | Relative abundances at species and genus levels in samples/runs that passed our QC criteria. |
| [Relative abundance summary](https://gmrepo2025.humangut.info:8443/Downloads/SQLDumps/species_abundance_summary.txt.gz) | Summary statistics on the taxonomic abundance data. |
| [Taxon co-occurrence data](https://gmrepo2025.humangut.info:8443/Downloads/SQLDumps/species_cooccurence.txt.gz) | Taxon co-occurrence in runs/samples of each phenotype, calculated separately for species and genus. |
| [Statistics by phenotype](https://gmrepo2025.humangut.info:8443/Downloads/SQLDumps/stats_by_phenotype.txt.gz) | Statistics by phenotype, including number of runs (with meta-data), processed/valid/failed runs, and number of associated species and genera. |
| [MySQL dump of the whole database](https://gmrepo2025.humangut.info:8443/Downloads/SQLDumps/gmrepo.sql.gz) | MySQL dump of all tables in the database. |
| [MeSH table](https://gmrepo2025.humangut.info:8443/Downloads/SQLDumps/mesh_data.txt.gz) | Medical Subject Headings (MeSH) data used in this study. |
| [NCBI taxonomy table](https://gmrepo2025.humangut.info:8443/Downloads/SQLDumps/superkingdom2descendents.txt.gz) | Reformatted NCBI taxonomy: taxon ID to scientific name and rank. |
<!-- | [Runs to phenotypes](https://gmrepo2025.humangut.info:8443/Downloads/SQLDumps/sample_to_disease_info.txt.gz) | All runs and their corresponding phenotypes (if any); one run/sample can be associated with multiple phenotypes. | -->

!!! note
    Please note that in the NCBI taxonomy database, two types of taxonomy IDs are used:
    
    - `taxon_id`: Internal unique ID used by NCBI taxonomy
    - `ncbi_taxon_id`: The *actual* NCBI taxonomy ID of a taxonomy entity

## Download raw sequence data

Due to limited hardware capacity, we do not offer raw sequence data downloads directly from our database.

Instead, users should download raw sequence reads from public databases such as the [SRA (Sequence Read Archive)](https://www.ncbi.nlm.nih.gov/sra) at NCBI (National Center for Biotechnology Information).

To do so:

- Copy & paste the run ID of interest into the "Search" box on the [SRA website](https://www.ncbi.nlm.nih.gov/sra)
- Visit the corresponding run page, and use download links provided
- Or use the "linkout" icon (available for each run ID in GMrepo) to go directly to the corresponding SRA run page

Alternatively, use command-line tools from the [SRA Toolkit](https://trace.ncbi.nlm.nih.gov/Traces/sra/sra.cgi?view=software) to download raw data in various formats. Common tools include:

- [`fastq-dump`](https://trace.ncbi.nlm.nih.gov/Traces/sra/sra.cgi?view=toolkit_doc&f=fastq-dump): download SRA data to a local directory. Usage:
  
  ```bash
  fastq-dump [options] <run_accession_id>
* [`prefetch`](https://trace.ncbi.nlm.nih.gov/Traces/sra/sra.cgi?view=toolkit_doc&f=prefetch): download SRA, dbGaP and ADSP data. Usage:
* 
  ```bash
  prefetch [options] <run_accession_id>
For more details, consult the [SRA Toolkit documentation](https://trace.ncbi.nlm.nih.gov/Traces/sra/sra.cgi?view=toolkit_doc).

<!-- 
## Programmable access

**GMrepo** also provides programmable access to most database contents via `RESTful APIs`.

Below are example codes in languages commonly used in our lab. Users of other languages can adapt from these examples or [contact us](https://gmrepo2025.humangut.info:8443/home) for help:

-   [R](https://github.com/evolgeniusteam/GMrepoProgrammableAccess/blob/master/programmable-access/R.md)
-   [Perl](https://github.com/evolgeniusteam/GMrepoProgrammableAccess/blob/master/programmable-access/perl.md)
-   [Python (2 & 3)](https://github.com/evolgeniusteam/GMrepoProgrammableAccess/blob/master/programmable-access/python.md)
 
See our [GitHub page](https://github.com/evolgeniusteam/GMrepoProgrammableAccess) for more details.
 -->
