FROM r-base

MAINTAINER damian.schaerli@jls.ch

RUN R -e 'install.packages("plumber")'

ADD addition.R .

EXPOSE 8000

ENTRYPOINT ["R", "-e", "pr <- plumber::plumb(commandArgs()[4]); pr$run(port=8000)"]
CMD ["addition.R"]
