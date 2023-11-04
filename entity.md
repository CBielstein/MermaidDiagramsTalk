# Entity Relationship Diagram

Mermaid Entity Relationship Diagram for modeling data or models.
Often used to describe relational databases.

## Entities and Attributes

```mermaid
erDiagram
    PERSON {
        string name
        string email
    }

    TALK {
        string title
    }

    ROOM {
        int number
    }
```

## Relationships

```mermaid
erDiagram
    PERSON {
        string name
        string email
    }

    TALK {
        string title
    }

    ROOM {
        int number
    }

    TALK }o--o{ PERSON: attendees
    TALK }o--|| PERSON: presenter
    TALK }o--|| ROOM: location
```

Cardinality:

* `|o`: Zero or one
* `||`: Exactly one
* `}o`: Zero or more
* `}|`: One or more
