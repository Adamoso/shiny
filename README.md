Docker for xai2shiny applications
=======================

This is a Dockerfile for xai2shiny R package applications. It is heavily based on [rocker/shiny](https://hub.docker.com/r/rocker/shiny) with added necessary packages for xai2shiny applications:
- "shiny", "shinyjs", "shinyBS", "shinydashboard", "shinycssloaders", "shinyWidgets", "DALEX" and "ggplot2".

## Example:

This Dockerfile is specifically created to be run with the R package xai2shiny, but can be used manually in specific cases.
In order to do so, run.

```sh
docker run --rm -p 3838:3838 adamoso/xai2shiny
```

And to run the application itself.

```sh
docker run --rm -p 3838:3838 \
    -v /srv/shinyapps/:/srv/shiny-server/ \
    -v /srv/shinylog/:/var/log/shiny-server/ \
    adamoso/xai2shiny
```

## Logs

Logs for the applications are kept in '/var/log/shiny-server' directory.
