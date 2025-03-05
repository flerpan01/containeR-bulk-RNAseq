# README

Singularity image with pre-installed libraries for running bulk RNA-seq analysis

The included libraries:

#### Visualisation

+ ggplot2
+ ggrepel
+ ggsignif
+ cowplot
+ RColorBrewer
+ patchwork
+ ComplexHeatmap

#### Differential gene expression analysis

+ edgeR
+ DESeq2

#### Gene and genome annotation

+ [clusterProfiler](https://www.bioconductor.org/packages/release/bioc/html/clusterProfiler.html)
+ [ReactomePA](https://bioconductor.org/packages/release/bioc/html/ReactomePA.html)
+ biomaRt
+ [org.Mm.eg.db](https://bioconductor.org/packages/release/data/annotation/html/org.Mm.eg.db.html)
+ [org.Hs.eg.db](https://bioconductor.org/packages/release/data/annotation/html/org.Hs.eg.db.html)
+ tximport

#### Utility

+ gtools
+ tools
+ scales
+ data.table
+ forcats
+ openxlsx

---

## Build

Use the definition file to build locally:

```sh
apptainer build bulk-RNAseq.sif bulk-RNAseq.def
```

## Deploy

Pre-build image can be downloaded from the [Cloud Library](https://cloud.sylabs.io/library):

```sh
apptainer pull library://flerpan01/singularity-r/bulk-rnaseq:latest
```

>Note, with apptainer the [remote singularity host](https://apptainer.org/docs/user/latest/endpoint.html#restoring-pre-apptainer-library-behavior) might need to be added manually
>
>```sh
># list the remote URI
>singuliarty remote list
>
># add singularity cloud URI
>apptainer remote add --no-login SylabsCloud cloud.sycloud.io
>```