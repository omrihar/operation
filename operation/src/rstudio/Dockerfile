FROM rocker/tidyverse

RUN mkdir -p /home/user/.rstudio/monitored/user-settings/

RUN apt-get update &&  \
    apt-get install -y libmagick++-dev

RUN R -e "install.packages('viridis',dependencies=TRUE, repos='http://cran.rstudio.com/')"
RUN R -e "install.packages('hrbrthemes',dependencies=TRUE, repos='http://cran.rstudio.com/')"
RUN R -e "install.packages('gghighlight',dependencies=TRUE, repos='http://cran.rstudio.com/')"
RUN R -e "install.packages('pander',dependencies=TRUE, repos='http://cran.rstudio.com/')"
RUN R -e "install.packages('showtext',dependencies=TRUE, repos='http://cran.rstudio.com/')"
RUN R -e "install.packages('reactable',dependencies=TRUE, repos='http://cran.rstudio.com/')"
RUN R -e "install.packages('ggridges',dependencies=TRUE, repos='http://cran.rstudio.com/')"
RUN R -e "install.packages('magick', dependencies=TRUE, repos='http://cran.rstudio.com/')"
RUN R -e "install.packages('ggimage', dependencies=TRUE, repos='http://cran.rstudio.com/')"
RUN R -e "devtools::install_github('ThinkR-open/remedy')"

RUN cd /usr/share/fonts && git clone https://github.com/Ben8t/fonts.git
RUN fc-cache -f -v

COPY ./user-settings /home/user/.rstudio/monitored/user-settings/user-settings

