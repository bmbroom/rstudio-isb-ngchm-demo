FROM b.gcr.io/isb-cgc-public-docker-images/r-examples:latest

RUN Rscript -e 'devtools::install_github("bmbroom/tsvio",ref="stable")' \
            -e 'devtools::install_github("bmbroom/NGCHMR",ref="beta")' \
            -e 'devtools::install_github("bmbroom/ISB-CGC-utils",ref="master")' \
            -e 'devtools::install_github("rstats-db/bigrquery")'
