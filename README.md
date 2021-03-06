# PostGIS Baselayers

**This is a work in progress! Still hoping to improve it in the coming months, let me know if you like the idea.**

PostGIS Baselayers is a web application that connects to a PostGIS database and lets you automatically download and import a selection of popular open vector datasets (Natural Earth, GADM, Geonames, etc) into the database. It comes bundled with a Docker environment and a PostGIS database container to get up and running quickly.

The application and database works nicely as a standalone spatial database that you can run queries against, or you can load data from it directly using QGIS/GDAL tools.

![PostGIS Baselayers Homepage](docs/img/screenshot-home.png)

## Why

For a few years now I have had an assortment of different base layers lying around to help with making maps and visualizations, experimenting with PostGIS or QGIS, and for various other spatial analysis tasks. Having these datasets just sitting around in all sorts of different formats was a hassle, and I decided to put some time into a framework that would organize them. It's nice to have all these datasets available in a single PostGIS database that can be contributed to as well by others.

Installation of new datasets is a breeze with the installers, and having all the datasets in a single database lets you do all sort of fun queries across different datasets.

## Quick Start

Clone the repository with `https://github.com/kokoalberti/postgis-baselayers.git`, build the containers with `docker-compose build`, and start the service with `docker-compose up`. 

Once running, visit the management application in your browser at `http://localhost:8003/` and choose which datasets you want to install into the database. 

## Accessing Data

Once a dataset is installed, you can access the PostGIS database using the following credentials:

    Hostname: localhost
    Port: 35432
    Database name: postgis-database
    Username/password: postgis

See for some more examples:

* [QGIS](docs/QGIS.md)
* [GDAL/OGR](docs/GDALOGR.md)
* [PSQL](docs/PSQL.md)

## Datasets

Vector datasets currently available in PostGIS Baselayers are a selection of:

* [Geonames](app/datasets/geonames/)
* [GADM](app/datasets/gadm/)
* [Koeppen-Geiger Climate Classifications](app/datasets/koeppengeiger/)
* [Natural Earth](app/datasets/naturalearth/)

If there is a dataset you'd like to see included, please create an issue in the issue tracker, or have a look at [CONTRIBUTING.md](CONTRIBUTING.md) on how to add it yourself.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for more information.

## Issues

See the issue tracker for a list of issues and features.