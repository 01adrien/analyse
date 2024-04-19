<link rel="stylesheet" href="style.css"/>

[<span class="icon-big">&#8592;</span>](./2-analyse.md)


```mermaid
    ---
title: play my house app diagramme de classe 
---
classDiagram
    note "test note"
    User <|-- Instrument
    Instrument <|-- Reservation 
    note for Reservation "note for Reservation"


    class Reservation {
        +int id
        +Date start
        +Date end
    }

    class User {
        +int id
        +String lname
        +String fname
        +String password
        +String telephone
        +String adress
    }

    class Instrument {
        +int id
        +String name
        +String description
        +Date createdAt
    }

```