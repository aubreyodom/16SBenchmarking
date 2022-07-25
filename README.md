
# Benchmarking analysis pipelines and reference libraries for profiling 16S amplicon sequencing data using mock microbial communities

This respository contains and links to relevant files for the Faits and Odom-Mabey et al. 16S pipeline benchmarking paper.

# Adapted reference libraries

## RefSeq

## SILVA 138 Indices
- QIIME 2 SILVA libraries were obtained from the (QIIME 2 website.)[https://docs.qiime2.org/2022.2/data-resources/?highlight=silva]
- Mothur SILVA libraries were obtained from the (Mothur website.) [https://mothur.org/wiki/silva_reference_files/]
- Kraken 2 SILVA libraries were obtained from the (Index Zone.)[https://benlangmead.github.io/aws-indexes/k2]
- PathoScope SILVA indices were custom-configured, and are available in this repository in the folder "PS_SILVA."

## Kraken Standard
- The Kraken Standard library was originally downloaded on 8/20/2020. This library may be downloaded from the (Index Zone)[https://benlangmead.github.io/aws-indexes/k2] under the header "Older Kraken 2 / Bracken Refseq indexes." The relevant Standard library is listed under the date 9/19/2020.
- Note that this library is comparable to the PathoScope RefSeq 2020 library used in the paper.

## Greengenes 13_8
- QIIME 2 Greengenes libraries were obtained from the (QIIME 2 website.)[https://docs.qiime2.org/2022.2/data-resources/?highlight=greengenes]
- Mothur Greengenes libraries were obtained from the (Mothur website.)[https://mothur.org/w/images/6/68/Gg_13_8_99.taxonomy.tgz/]
- PathoScope Greengenes indices were custom-configured, and are available in this repository in the folder "PS_GG."
-Kraken 2 Greengenes indices were obtained by running the following code:

```
# Load software
module load python3
cd ~/kraken2-2.1.2

DBNAME="/restricted/projectnb/pathoscope/work/tyler/MethodsAnalyses/Kraken/KrakenGG13_8"

kraken2-build --db ${DBNAME} --special greengenes --threads 8
```

## RefSeq
- PathoScope RefSeq libraries were custom-configured, and are available in this repository in the folder "PS_RefSeq_2018" and "PS_RefSeq_2020."
- Current indices (which were not used in our paper) may be obtained by using the download_refseq() from the MetaScope package.
