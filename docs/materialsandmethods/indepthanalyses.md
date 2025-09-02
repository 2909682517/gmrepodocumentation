
# Identification of disease markers in curated projects

> *Note: This is an* `ongoing effort` *and the results are available for a limited number of projects; more will be added as analyses proceed.*

## Overview

Marker identification was performed for `selected projects` referred to as  [curated projects](https://gmrepo2025.humangut.info:8443/data/curatedProjects) in **GMrepo**.  
These projects were selected based on the following criteria (in addition to available manpower and time):

- High-quality meta-data with clearly defined diseases and healthy controls
- High-quality sequence data
- Sufficient numbers of both cases and controls, usually more than 10 per group

## Marker taxa

A `marker taxon` refers to a genus or species that shows significantly different abundances between two groups  
(e.g., cases vs. controls or disease stages such as adenoma vs. CRC), identified using  
`LEfSe (Linear discriminant analysis effect size)`  
[PMID: 21702898](https://www.ncbi.nlm.nih.gov/pubmed/21702898)

Marker taxa were identified on a per-project basis.  
Please consult the [All marker taxa page](https://gmrepo2025.humangut.info:8443/taxon/marker) for more information.

## Curated projects

In **GMrepo**, manual curation was performed for selected projects in order to:

- Select usable runs with clearly defined phenotypes
- Merge multiple runs corresponding to the same sample and calculate taxon abundances per sample (instead of per run)
- Group samples according to their phenotypes
- Identify marker taxa between phenotype groups of interest, e.g., CRC vs. Health

<!--Curated projects are highlighted with a ✔️ symbol.  -->
In addition to project meta-data and run tables, curated project pages also include:

- A list of curated samples and their corresponding phenotypes and runs
- Marker taxa identified between pairs of phenotypes (referred to as [phenotype comparisons](https://gmrepo2025.humangut.info:8443/phenotypes/comparisons))  

Marker taxa are shown in both table and boxplot views.



For curated projects with more than two phenotype groups, e.g.:

- Healthy controls
- Adenoma
- Colorectal cancer (CRC)

Multiple phenotype comparisons can be performed, such as:

- Healthy control  vs  CRC
- Healthy control  vs  Adenoma
- Adenoma  vs  CRC

This enables identification of marker taxa across different disease stages.
<!--
See [PRJEB6070](https://gmrepo.humangut.info/data/project/PRJEB6070) for an example.


---

So far, **GMrepo** includes:

- 299 [curated projects](https://gmrepo2025.humangut.info:8443/data/curatedProjects), 
- 81 [diseases](https://gmrepo2025.humangut.info:8443/phenotypes/comparisons), 
- 31,085 samples.

-->