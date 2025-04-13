# UNVT POD, QMP, and Fusion Initiatives

The Smart Maps Group of the UN Open GIS Initiative is planning the UNVT POD, QMP, and Fusion initiatives for the summer and winter of 2025. These projects aim to enhance map usability in areas with limited resources, enable rapid map improvements through OpenStreetMap (OSM), and integrate various data sources.

We have a [scratchpad](https://hackmd.io/@smartmaps/2025) for the project on HackMD. 

## UNVT POD: United Nations Vector Tile Toolkit Portable Option D

### Purpose of UNVT POD

UNVT POD aims to provide map access to users with limited resources, utilizing the latest cloud-native technologies in environments with unstable or unavailable internet connections.

### Technical Concept

UNVT POD is designed as a portable and self-contained system that can function offline. It will use the latest vector tile technology and is intended to be cost-effective to build and operate, supporting one to four users per unit.

### Key Features of UNVT POD

* Portable and self-contained system
* Usable in offline environments
* Based on the latest vector tile technology
* Low cost to build and operate
* Designed for small groups of users (1-4 per unit)

### Tools Used

The following tools will be used in the development of UNVT POD:

#### Geospatial

* [Tippecanoe](https://github.com/felt/tippecanoe): This tool will be used to build vector tilesets from GeoJSON, FlatGeobuf, or CSV data.
    * Reasoning: Tippecanoe is a proven, high-performance tool for efficient vector tile generation.
* [go-pmtiles](https://github.com/protomaps/go-pmtiles): This tool will be used for efficient processing of PMTiles data.
    * Reasoning: go-pmtiles provides high performance due to the efficiency of the Go programming language.

#### Web Frontend

* [MapLibre GL JS](https://maplibre.org/maplibre-gl-js/docs/): This JavaScript library will be used to display interactive maps in web browsers.
    * Reasoning: MapLibre GL JS offers high performance and flexibility for modern map representations. It is open-source, with an active community.

#### Web Backend

* [Martin](https://[github.com/maplibre/martin): This server will be used to serve vector tiles with high performance.
    * Reasoning: Martin is designed for high performance and scalability, making it suitable for cloud-native environments.
* [Caddy](https://caddyserver.com/): This web server will be used for its power, adaptability, and ease of use.
    * Reasoning: Caddy offers modern web server features, such as automatic HTTPS and simplified configuration, which helps to reduce operational costs.

#### System

* [Git](https://git-scm.com/): This distributed version control system will be used.
    * Reasoning: Git is essential for development version control, collaboration, and backups.
* [tmux](https://github.com/tmux/tmux): This terminal multiplexer will be used.
    * Reasoning: tmux helps to efficiently manage multiple terminal sessions, streamlining development and operations.
* [Pkl](https://pkl-lang.org/): This configuration language, which is programmable, scalable, and safe, will be used.
    * Reasoning: MapLibre style descriptions (in JSON) can be complex. Pkl will help manage this complexity.
* [jq](https://jqlang.org/): This lightweight and flexible command-line JSON processor will be used.
    * Reasoning: jq is a versatile and powerful tool for efficient processing of JSON data.

## QMP (Quick Mapping Project)

### Purpose of QMP

The Quick Mapping Project (QMP) aims to enable rapid responses to specific map enhancement needs using OpenStreetMap (OSM).

### Technical Concept

The proposed process for QMP is as follows:

1.  Requests to add or modify map data in a specific area will be registered on GitHub Issues.
2.  The tag #qmp will be added to the OSM changeset. The [Rapid](https://rapideditor.org/) editor may be used for mapping.

### Handling as OpenStreetMap Organized Editing

* QMP may be categorized as an OSM Organized Editing activity.
* Depending on the project's scope and impact, it might be necessary to coordinate with the OSM community beforehand.
* This project seeks to encourage broad participation while adhering to OSM community guidelines and establishing appropriate procedures as needed.

## Fusion: Integration of Vector Tile Data

### Purpose of Fusion

In addition to data from UNVT POD and QMP, Fusion aims to integrate vector tile data from various public organizations and projects. This will provide more comprehensive map information to meet diverse user needs.

### Technical Concept

* **Integration of Diverse Data Sources**: Fusion will utilize vector tile data from public organizations, such as the Geographical Survey Institute of Japan (GSI) and GISTDA (Thailand).
* **Flexible Data Selection on the Client-Side**: The system will allow users to freely combine necessary data layers based on their specific requirements.
* **Utilization of PMTiles**: PMTiles format will be used to efficiently distribute and utilize vector tile data from different sources.

### Key Features of Fusion

* **Comprehensive Map Information**: By combining multiple data sources, Fusion will offer detailed and multifaceted information that may not be available from a single source.
* **Adaptability to User Needs**: Users will be able to select and customize data according to their intended use.
* **Collaboration Between Public and Private Data**: Combining reliable data from public organizations with open data, such as OSM, can improve data quality and freshness.

## Synergistic Effects of UNVT POD, QMP, and Fusion

* **Data Provision**: OSM data that is updated and improved through QMP can be provided as vector tile data for UNVT POD and also used as a data source for Fusion. This allows QMP results to be used in environments with limited internet connectivity and by a wider range of users.
* **Sharing of Needs**: QMP activities can address specific map needs in areas where UNVT POD is deployed. QMP can also help in the selection of data for integration in Fusion. This will enhance the practicality of UNVT POD and Fusion, and contribute to the well-being of local residents.
* **Flexible Data Utilization**: The Fusion concept, in conjunction with UNVT POD and QMP, enables users to combine PMTiles from various entities, based on client needs. This will allow users to obtain optimal map information.

