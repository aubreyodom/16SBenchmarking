
# Metagenomic profiling pipelines improve taxonomic classification for 16S amplicon sequencing data

This respository contains links to relevant files for the Faits and Odom-Mabey et al. 16S pipeline benchmarking paper.

## Adapted reference libraries

### SILVA 138 Indices
- QIIME 2 SILVA indices were obtained from the [QIIME 2 website.](https://docs.qiime2.org/2022.2/data-resources/?highlight=silva)
- Mothur SILVA indices were obtained from the [Mothur website.](https://mothur.org/wiki/silva_reference_files)
- Kraken 2 SILVA indices were obtained from the [Index Zone.](https://benlangmead.github.io/aws-indexes/k2)
- PathoScope SILVA indices were custom-configured, and can be downloaded [here.](https://rutgers.box.com/s/njq1qc9bzawzs3a6513uihxxwgxu9qc5)

### Kraken Standard
- The Kraken Standard indices was originally downloaded on 8/20/2020. This library may be downloaded from the [Index Zone](https://benlangmead.github.io/aws-indexes/k2) under the header "Older Kraken 2 / Bracken Refseq indexes." The relevant Standard library is listed under the date 9/19/2020.
- Note that this library is comparable to the PathoScope RefSeq 2020 library used in the paper.

### Greengenes 13_8
- QIIME 2 Greengenes indices were obtained from the [QIIME 2 website.](https://docs.qiime2.org/2022.2/data-resources/?highlight=greengenes)
- Mothur Greengenes indices were obtained from the [Mothur website.](https://mothur.org/w/images/6/68/Gg_13_8_99.taxonomy.tgz/)
- PathoScope Greengenes indices were custom-configured, and can be downloaded [here.](https://rutgers.box.com/s/lqjxlub5wxgdlosbyk5sef7zug2nae5z)
- Kraken 2 Greengenes indices were obtained by running the following code:
```
# The DBNAME variable is the name of a folder to which the library will be saved
kraken2-build --db ${DBNAME} --special greengenes --threads 1
```
### RefSeq
- PathoScope RefSeq libraries were custom-configured.
- The RefSeq 2018 indices can be downloaded [here.](https://rutgers.box.com/s/z14lbdarbimull8q27fxay93yrh793cv)
- The RefSeq 2020 indices can be downloaded [here.](https://rutgers.box.com/s/b3fxv2n7ol4fcwmbe6ihmcq0eyb978lo)
- Up-to-date RefSeq indices may be obtained by using the `download_refseq()` function from the [MetaScope package](https://compbiomed.github.io/metascope-docs/index.html).
