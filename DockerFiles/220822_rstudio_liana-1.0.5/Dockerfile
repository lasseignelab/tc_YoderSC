FROM bioconductor/bioconductor_docker:RELEASE_3_14

# location for mounting
#RUN mkdir /home/rstudio/data


##----------------------------------------------------------------------------##
## (SOME) R PACKAGES
##----------------------------------------------------------------------------##

RUN R -e 'install.packages(c("Seurat","tidyverse", "ggrepel", "cowplot", "remotes", "ggpubr", "BiocManager", "devtools", "harmony", "pheatmap", "clustree", "enrichR"))'


RUN R -e 'devtools::install_github("saezlab/liana")' 

RUN R -e 'remotes::install_github("saeyslab/nichenetr", quiet = TRUE)'

RUN R -e 'devtools::install_github("ririzarr/rafalib")' 


##----------------------------------------------------------------------------##
## SYSTEM PACKAGES
##----------------------------------------------------------------------------##

RUN apt-get update --yes && \
  apt-get upgrade --yes

RUN apt-get install --yes \
  python-dev \
  python3-pip \
  python3-dev \
  python3-pip \
  python3-tk


RUN apt-get install --yes \
  libcurl4-openssl-dev \
  libssl-dev \
  libcairo2-dev libxt-dev \
  libxml2-dev \
  libudunits2-dev \
  libhdf5-dev \
  libv8-dev \
  libgdal-dev \
  xorg libx11-dev libglu1-mesa-dev \
  samtools libboost-all-dev \
  libgsl-dev

##----------------------------------------------------------------------------##
## PYTHON PACKAGES
##----------------------------------------------------------------------------##


RUN pip3 install leidenalg



