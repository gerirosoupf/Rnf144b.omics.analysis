FROM rocker/binder:4.2.1
LABEL maintainer='Gerard Romero <gerard.romero02@estudiant.upf.edu>'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}

RUN wget https://github.com/gerirosoupf/Rnf144b.omics.analysis/raw/master/DESCRIPTION && R --vanilla -s -e "options(repos = list(CRAN = 'http://cran.rstudio.com'));  install.packages('renv'); renv::restore()"

RUN rm DESCRIPTION.1; exit 0
