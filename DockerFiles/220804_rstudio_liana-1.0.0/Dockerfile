FROM bioconductor/bioconductor_docker:RELEASE_3_14

# location for mounting
#RUN mkdir /home/rstudio/data

RUN R -e 'install.packages(c("Seurat","tidyverse", "ggrepel", "cowplot", "remotes", "ggpubr", "BiocManager", "devtools"))'


RUN R -e 'devtools::install_github("saezlab/liana")' 

RUN R -e 'remotes::install_github("saeyslab/nichenetr", quiet = TRUE)'
