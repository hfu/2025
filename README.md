# UNVT POD, QMP, and Fusion

This document describes the UNVT POD (United Nations Vector Tile Toolkit Portable Option D), QMP (Quick Mapping Project), and Fusion initiatives, planned for the summer and winter of 2025 by the Smart Maps Group of the UN Open GIS Initiative. Through these projects, we aim to improve map utilization in resource-constrained environments, rapidly enhance maps through OpenStreetMap (OSM), and integrate diverse data sources.

## UNVT POD: United Nations Vector Tile Toolkit Portable Option D

### Purpose of UNVT POD

To provide map access to users with limited resources who require the latest cloud-native technologies in environments with unstable or unavailable internet connections.

### Technical Concept

### Features of UNVT POD

* Portable and self-contained system
* Usable in offline environments
* Utilizes the latest vector tile technology
* Low cost to build and operate
* Designed for one to four users per unit

### Tools used

#### geospatial

* [Tippecanoe](https://github.com/felt/tippecanoe) - A tool to build vector tile sets from large (or small) collection of GeoJSON, FlatGeobuf, or CSV features.
    * Reasoning: Proven, high-performance tool for efficient vector tile generation.
* [go-pmtiles](https://github.com/protomaps/go-pmtiles)
    * Reasoning: Library for efficient processing of PMTiles format data, with high performance expected from Go language.

#### web frontend

* [MapLibre GL JS](https://maplibre.org/maplibre-gl-js-docs/) - A JavaScript library for displaying interactive maps in web browsers.
    * Reasoning: High performance and flexibility, enabling modern map representations. Open-source with active community development.

#### web backend

* [Martin](https://github.com/maplibre/martin) - A high-performance server for serving vector tiles.
    * Reasoning: High performance and scalability, suitable for cloud-native environments.
* [Caddy](https://caddyserver.com/) - A powerful, adaptable, and easy-to-use web server.
    * Reasoning: Modern web server features such as automatic HTTPS and ease of configuration, reducing operational costs.


#### system

* [Git](https://git-scm.com/) - A distributed version control system.
    * Reasoning: Essential tool for development version control, collaboration, and backups.
* [tmux](https://github.com/tmux/tmux) - A terminal multiplexer.
    * Reasoning: Efficiently manages multiple terminal sessions, streamlining development and operations.
* [Pkl](https://pkl-lang.org/) - Configuration that is Programmable, Scalable, and Safe. 
    * Reasoning: MapLibre Style description, a map styling configuration in JSON for vector tile, is complex in many cases. We use the Pkl language to nicely manage the complexity of the style description. 
* [jq](https://jqlang.org/) - A lightweight and flexible command-line JSON processor
    * Reasoning: Versatile and powerful tool for efficient processing of JSON data.

## QMP (Quick Mapping Project)

### Purpose of QMP

To rapidly respond to specific map enhancement needs through OpenStreetMap (OSM).

### Technical Concept

#### Proposed Process

1.  Requests to add to or modify a map in a specific area are registered on GitHub Issues.
2.  The tag #qmp is added to the OSM changeset. [Rapid](https://rapideditor.org/) might be a tool of choice for mapping. 

#### Features

### Handling as OpenStreetMap Organized Editing

* QMP may fall under the category of OSM Organized Editing.
* Depending on the project's scale and impact, it may be necessary to reach an agreement with the OSM community in advance.
* This project aims to promote casual participation while respecting OSM community guidelines and considering appropriate procedures as needed.

## Fusion: Integration of Vector Tile Data

### Purpose of Fusion

In addition to data generated and provided by UNVT POD and QMP, Fusion aims to integrate vector tile data from various public organizations and projects to provide more comprehensive map information that meets user needs.

### Technical Concept

* **Integration of Diverse Data Sources**: Utilize vector tile data provided by public organizations such as the Geographical Survey Institute of Japan (GSI) and GISTDA (Thailand).
* **Flexible Data Selection on the Client-Side**: Construct a system that allows users to freely combine necessary data layers according to their needs.
* **Utilization of PMTiles**: Efficiently distribute and utilize vector tile data from different sources in PMTiles format.

### Features of Fusion

* **Comprehensive Map Information**: By combining multiple data sources, Fusion provides detailed and multifaceted information that cannot be obtained from a single data source.
* **Adaptability to User Needs**: Users can freely select and customize data according to their intended use.
* **Collaboration Between Public and Private Data**: Combining reliable data provided by public organizations with open data such as OSM improves data quality and freshness.

## Synergistic Effects of UNVT POD, QMP, and Fusion

* **Data Provision**: OSM data updated and improved by QMP can be provided not only as vector tile data available for UNVT POD, but also utilized as a data source for Fusion. This allows the results of QMP activities to be used in environments with limited internet connectivity, and by a wider range of users.
* **Sharing of Needs**: QMP activities can be based on specific map needs in the areas where UNVT POD is deployed, and can also be useful in selecting data for integration in Fusion. This enhances the practicality of UNVT POD and Fusion, and contributes to the lives of local residents.
* **Flexible Data Utilization**: The Fusion concept, in addition to UNVT POD and QMP, enables the free combination of PMTiles provided by various entities according to client needs. This allows users to obtain optimal map information.
