FROM b.gcr.io/isb-cgc-public-docker-images/r-examples:latest

ADD rsession.conf /etc/rstudio/rsession.conf

RUN Rscript -e 'devtools::install_github("bmbroom/tsvio",ref="stable")' \
            -e 'devtools::install_github("bmbroom/NGCHMR",ref="beta")' \
            -e 'devtools::install_github("bmbroom/ISB-CGC-utils",ref="beta")' \
            -e 'devtools::install_github("hadley/httr")' \
            -e 'devtools::install_github("rstats-db/bigrquery")'
