# Start from an image containing R, rmarkdown stuff and shiny server
FROM flaviobarros/shiny-wordcloud
 
# Install packages required by my app
RUN R -e "install.packages(c('shiny', 'rmarkdown', 'tm', 'wordcloud', 'memoise'), repos='http://cran.rstudio.com/')"
 
 
# Remove Shiny example inherited from the base image
RUN rm -rf /srv/shiny-server/*
 
 
# Copy the source code of the app from my hard drive to the container (in this case we use the app "wordcloud" from http://shiny.rstudio.com/gallery/word-cloud.html)
COPY wordcloud/* /srv/shiny-server/
 
 
# Start the server with the container
CMD ["/usr/bin/shiny-server.sh"]