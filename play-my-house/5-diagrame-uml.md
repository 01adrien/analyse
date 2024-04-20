<link rel="stylesheet" href="style.css"/>

[<span class="icon-big">&#8592;</span>](./2-analyse.md)


```mermaid
    ---
title: play my house app diagramme de classe 
---
classDiagram
    note "test note"
    User "1" <--> "0..*" Instrument
    Instrument "1" <--> "0..*" Reservation 
    note for Reservation "note for Reservation"

    class Reservation {
        id: int
        start: Date
        end: Date
        user: User
        instrument: Instrument
    }

    class User {
        id: int
        lname: String 
        fname: String 
        password: String 
        telephone: String
        email: String 
        adress: String 
        role: UserRole
        Image: image
    }

    class UserRole {
        id: int
        name: String
    }

    class Instrument {
        id: int 
        name: String 
        description: String 
        createdAt: Date 
        user: User
        images: Array<Image>
    }



    class Image {
        id: int
        url: String
        type: ImageType
    }

    class ImageType {
        id: int
        name: String
    }

```