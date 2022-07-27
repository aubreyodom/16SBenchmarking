
# Metagenomic profiling pipelines improve taxonomic classification for 16S amplicon sequencing data

This respository contains and links to relevant files for the Faits and Odom-Mabey et al. 16S pipeline benchmarking paper.

## Adapted reference libraries

### SILVA 138 Indices
- QIIME 2 SILVA indices were obtained from the [QIIME 2 website.](https://docs.qiime2.org/2022.2/data-resources/?highlight=silva)
- Mothur SILVA indices were obtained from the [Mothur website.](https://mothur.org/wiki/silva_reference_files)
- Kraken 2 SILVA indices were obtained from the [Index Zone.](https://benlangmead.github.io/aws-indexes/k2)
- PathoScope SILVA indices were custom-configured, and are available in this repository in the folder "PS_SILVA."

### Kraken Standard
- The Kraken Standard indices was originally downloaded on 8/20/2020. This library may be downloaded from the [Index Zone](https://benlangmead.github.io/aws-indexes/k2) under the header "Older Kraken 2 / Bracken Refseq indexes." The relevant Standard library is listed under the date 9/19/2020.
- Note that this library is comparable to the PathoScope RefSeq 2020 library used in the paper.

### Greengenes 13_8
- QIIME 2 Greengenes indices were obtained from the [QIIME 2 website.](https://docs.qiime2.org/2022.2/data-resources/?highlight=greengenes)
- Mothur Greengenes indices were obtained from the [Mothur website.](https://mothur.org/w/images/6/68/Gg_13_8_99.taxonomy.tgz/)
- PathoScope Greengenes indices were custom-configured, and are available in this repository in the folder "PS_GG."
- Kraken 2 Greengenes indices were obtained by running the following code:

```
# The DBNAME variable is the name of a folder to which the library will be saved
kraken2-build --db ${DBNAME} --special greengenes --threads 1
```
### RefSeq
- PathoScope RefSeq libraries were custom-configured, and are available in this repository in the folder "PS_RefSeq_2018" and "PS_RefSeq_2020."
- Updated RefSeq indices may be obtained by using the `download_refseq()` function from the [MetaScope package](https://compbiomed.github.io/metascope-docs/index.html).
