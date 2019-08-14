# OpenRQM System Architecture

This repository contains the architecture of the OpenRQM System.



- [OpenRQM System Architecture](#openrqm-system-architecture)
  - [System Overview](#system-overview)
  - [API specification](#api-specification)


## System Overview

The OpenRQM System contains of a server which exposes the OpenRQM REST API and several clients which use it.

The OpenRQM project specifies only the REST API and provides a server and client implementation to demonstrate it.

This way many different implementations can be created which are interoperable.

```plantuml
@startuml
caption OpenRQM Deployment Diagram

skinparam monochrome true
skinparam componentStyle uml2

scale max 650 width

package "Server" {
    database "Database" as db
    component "OpenRQM Server" as s

    db -(0- s
}

package "Client" {
    component "OpenRQM Client" as c

}

package "Client 2" {
    component "OpenRQM Client" as c2

}

interface "REST API" as api


s -- api
c --( api
c2 --( api

@enduml
```

## API specification
