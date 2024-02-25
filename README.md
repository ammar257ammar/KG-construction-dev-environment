
# Knowledge Graph Construction with More Semantics And Less Code

## Introduction

Research generates a massive amount of data on a daily basis. In contrast, a knowledge graph is a
graph-structured data model that stands out in integrating heterogeneous data and depicting connections
between its entities. Large volumes of data can greatly benefit from knowledge graphs, which streamline
data organization and facilitate efficient searching and querying. Linked data, the basis of the semantic
web, represents a valuable design approach to construct knowledge graphs, as it not only embraces open
standards but also contributes to data FAIRness.


To go from datasets in common formats to linked data knowledge graphs, a series of steps (i.e.
workflow) need to be performed, called an ETL workflow (Extract, Transform, Load). Moreover, different
technical skills are needed to carry on this process. For example, knowing how to read, parse and
manipulate different data formats like tables (CSV, TSV, XLSX), JSON, relational databases and APIs (i.e extraction). Then,
the programming skills to transform and convert the data into linked data (i.e transformation). Finally,
the technical knowledge of triple stores to store and query the knowledge graph (i.e load). Therefore,
the steep learning curve and the diverse set of coding skills and tools to create knowledge graphs pose a
major barrier to the wider adoption of such an approach by the scientific community.


To address this challenge, this tutorial will walk the reader through the process of constructing
semantic knowledge graphs from scratch using LinkedPipes ETL. LinkedPipes is a browser-based tool
that provides a visual, drag-and-drop interface for creating ETL workflows that integrate heterogeneous
data sources into a linked data knowledge graph. It cuts down the necessary amount of coding and uses
SPARQL for transformation which is the same language used to query the resulting knowledge graph.
This tutorial begins with introducing SPARQL and RDF, guiding the reader from basics to advanced
SPARQL usage. Next, it will demonstrate how to get started with the portable environment for building
and querying knowledge graphs using Docker. This containerized setup simplifies technical complexities
of installing and setting up the individual tools. Next, it will discuss a data model for bioassay data including different entity types like: proteins, cell lines, chemicals, organisms, and dataset provenance. We’ll emphasize the importance
of data provenance for enhancing FAIRness. Using the semantic model, we’ll convert an input dataset to
RDF, extend it with external sources like UniProt, WikiPathways, and ChEMBL, and load the resulting
knowledge graph into a triple store. Lastly, readers will learn to write SPARQL queries to answer
bio-chemical questions, with examples showcasing the power of knowledge graphs in data integration
and modeling.



## Getting Started


### Requirements

1. In order to get started with this tutorial, you need a ready docker installation on your machine.
Follow the Docker installation instructions relevant to your operating system through the official Docker website:
[https://docs.docker.com/engine/install/](https://docs.docker.com/engine/install/)

1. You will also need Docker Compose to be install. Depending on your operating system and Docker installtion, you may already have Docker Compose installed. You can check that by run either the following commands:

```bash
docker compose version
``` 

```bash
docker-compose -v
``` 

If neither of the previous commands showed the version of Docker Compose, then you need to install it, following the instructions on the official Docker website:

[https://docs.docker.com/compose/](https://docs.docker.com/compose/)


### Start the local development environment

1. Download this repository to your computer, unzip the download zip file and navigate to its location from the command line. You can also clone this repository using the "git clone" command if you prefer this approach.


1. For linux users (probably Mac users too, though not tested on Mac), once you are inside the folder in terminal, run the following command (enter your password when requested):
```bash
sudo chown 5987:5987 -R data-output/
```
This command will make sure LinkedPipes ETL has the permission to write output files to this folder.

1. Run one of the following command (depending on which command worked for you in the last step of the requirements section

```bash
docker-compose up -d
```
Or

```bash
docker compose up -d
```

### Follow the tutorial slides



## Have Fun!!


[![CC BY-SA 4.0][cc-by-sa-shield]][cc-by-sa]

This work is licensed under a
[Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg



