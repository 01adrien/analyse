<link rel="stylesheet" href="style.css"/>

[<span class="icon-big">&#8592;</span>](./2-analyse.md)

Le diagramme UML est utilise pour representer les differentes classes et leurs attributs ( eventuellement les methodes).<br>
Ainsi que les relations d'heritage.<br>
On l'utlise pour decouper le programme en differentes classes / fonctionnalitees
<br>
<br> 

```mermaid
    ---
title: play my house app UML
---
classDiagram
    User "1" -- "0..*" Instrument
    Instrument "1" -- "0..*" Reservation 
    User "1" -- "0..*" Message
    UserRole "1..*" -- "1" User
    InstrumentFamily "1" -- "1..*" Instrument
    InstrumentBrand "1" -- "1..*" Instrument
    InstrumentType "1" -- "1..*" Instrument
    Image "1" -- "1" User
    Instrument "1" -- "1..5" Image
    Instrument "1..*" -- "1" InstrumentStatus
    Instrument "1" -- "1..*" Creneau

    note for InstrumentStatus "En attente
                                Refus
                                Accepte"
    note for UserRole "musicien
                        proprietaire
                        admin"

    class Reservation {
        id: Int
        start: Date
        end: Date
        user: User
        instrument: Instrument
    }

    class User {
        id: Int
        lastName: String 
        firstName: String 
        password: String 
        telephone: String
        email: String 
        adress: String 
        role: Array [UserRole]
        image: Image
    }

    class Message {
        id: Int
        recipient: User
        sender: User
        content: String
        date: Date
    }

    class Instrument {
        id: Int 
        name: String 
        description: String 
        createdAt: Date 
        user: User
        images: Array [Image]
        family: InstrumentFamily
        timeline: Array [Creneau]
        type: InstrumentType
        brand: InstrumentBrand

    }

    class Creneau {
        id: Int
        day: Date
        start: Int
        end: Int
    }

    class UserRole {
        id: Int
        name: String
    }

    class InstrumentFamily {
        id: Int
        name: String
    }

    class InstrumentType {
        id: Int
        name: String
    }

    class InstrumentBrand {
        id: Int
        naem: String
    }

    class InstrumentStatus {
        id: Int
        name: String
    }

    class Image {
        id: Int
        url: String
    }


```