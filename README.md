# GOST Dashboard service

The `GOST` service provides an [OGC SensorThings API](http://www.opengeospatial.org/standards/sensorthings) (STA) REST service based
on [Geodan GOST Server](https://github.com/gost/server). The GOST Dashboard provides an admin web UI
to manage Resources (Things, Sensors, etc) in the GOST server.

## Hosting

The Docker Image is hosted 
as: [smartemission/se-gostdashboard at DockerHub](https://hub.docker.com/r/smartemission/se-gostdashboard).

## Environment

No environment vars need to be set at this moment.

## Architecture

The image includes the official Geodan GOST Dashboard Docker Image overlayed with
the SE config file and `overrides`. The overrides are some `.html` file currently needed
to enable the Dashboard to run behind a proxy like Traefik or a K8s Ingress Proxy like
[described in this issue](https://github.com/gost/dashboard-v2/issues/2). 

Uses the [GOST Dashboard V2](https://github.com/gost/dashboard-v2)  and its related Docker Image 
the [GOST Dashboard V2 Docker Image](https://store.docker.com/community/images/geodan/gost-dashboard-v2).

GOST Dashboard used to be part of the GOST Server but since GOST v0.4 it has 
been moved to a separate repo and Docker Image. First as `gost/dashboard` (Angular),
now as `gost/dashboard-v2` (developed with Web Components and Polymer)

## Links

* SE Platform doc: http://smartplatform.readthedocs.io/en/latest/
* OGC SensorThings API Standard: http://www.opengeospatial.org/standards/sensorthings
* GOST Server - https://github.com/gost/server
* GOST DB - https://github.com/gost/gost-db
* GOST Dashboard - https://github.com/gost/dashboard-v2
