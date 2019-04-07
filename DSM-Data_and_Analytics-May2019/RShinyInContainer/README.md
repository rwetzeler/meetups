# R Shiny in Containers

Build the image
`docker build -t "meetups/shiny_wordcloud" .`

Run the container from your newly built image
`docker run --rm -p 80:80 meetups/shiny_wordcloud`