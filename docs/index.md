
# Welcome to **GMrepo**

**GMrepo** is a curated database of human gut metagenomes. Please choose a topic on the left navigation panel to continue.

## Citation

Please cite our latest publication if you find this resource useful:

[Dai, D. *et al.* "GMrepo v2: a curated human gut microbiome database with special focus on disease markers and cross-dataset comparison". *Nucleic Acids Res* (2022). Volume 50, Issue D1, Pages D777–D784.](https://doi.org/10.1093/nar/gkab1019)

<!--
### Previous version(s):

[Dai, D. *et al.* "GMrepo v2: a curated human gut microbiome database with special focus on disease markers and cross-dataset comparison". *Nucleic Acids Res* (2022). Volume 50, Issue D1, Pages D777–D784.](https://doi.org/10.1093/nar/gkab1019)

[Wu, S. *et al.* "GMrepo: a database of curated and consistently annotated human gut metagenomes". *Nucleic Acids Res* (2020).](https://doi.org/10.1093/nar/gkz764)

## What's new

### Nov 25, 2020

Added new pages:

* [Curated projects](https://gmrepo2025.humangut.info:8443/data/curatedProjects)
* [Phenotype comparisons](https://gmrepo2025.humangut.info:8443/phenotypes/comparisons)
* [Marker taxa](https://gmrepo2025.humangut.info:8443/taxon/marker)
-->
## Aims and features of **GMrepo**

### Capture the full dynamics of human gut microbes

With **GMrepo**, we aim to capture the full dynamics of the microbes living in the human gut, including their:

* abundances and prevalence,
* associations with [human health and diseases](https://gmrepo2025.humangut.info:8443/phenotypes), and
* co-occurrences,

all of which can be further stratified by using manually curated metadata:

* population (country),
* gender,
* age,
* body mass index, and
* many other available metadata.

### Emphasize on data quality and re-usability

With **GMrepo**, we emphasize **data quality** and **re-usability** (i.e., availability of the host metadata).
We thus:

* manually extracted and curated relevant metadata (most of the time with difficulties) from public databases and related publications;
* consistently re-annotated all data using state-of-the-art methods (see the [Materials and methods](materialsandmethods/dataprocessingandqc.md) page for details);
* applied vigorous quality control (QC) methods and stringent criteria to the data, in order to include only high quality data, but nonetheless kept the metadata of the samples and runs in our database.

### Make relevant information easier to find

In order to further facilitate users to find data of interest, we equipped **GMrepo** with a [graphical query builder (data selector)](https://gmrepo2025.humangut.info:8443/home) to help users create complex and flexible queries with a few clicks. So far the data selector allows users to filter samples and runs by related technical metadata such as `experiment type (16S or Metagenomics)`, `number of sequenced reads`, and host-related metadata, including related phenotype (`disease or health`), `age`, `sex`, and `BMI (body mass index)`. More filters will be added in the future.

For example, the screenshot below shows how to search for samples (runs) that:

* were taken from healthy individuals aged 18–25 years with a BMI between 18.5 and 24.9, **and**
* were sequenced by either 16S **or** metagenomics.

![Query builder example](images/index/query_builder_example2.png)

See [Use the graphic data selector](usage/graphicdataselector.md) for details and more examples.

