FROM rocker/r2u:22.04

COPY 'renv/profiles/lesson-requirements/renv.lock' .

RUN Rscript -e '\
  install.packages(c("sandpaper", "varnish", "pegboard", "tinkr"), repos = c("https://carpentries.r-universe.dev/", getOption("repos")));\
  renv::restore(lockfile = "renv.lock")\
'
