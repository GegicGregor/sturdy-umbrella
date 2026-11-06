# Data Model

Replace the example with your own model. Requirements: at least 3 entities, one 1:N and one M:N relationship.

```mermaid
erDiagram
    User ||--o{ Location : "has"
    User ||--o{ Reservation : "makes"
    Location ||--o{ Court : "contains"
    Court ||--o{ Reservation : "has"
    Court ||--o{ Court_Sport : "has"
    Sport ||--o{ Court_Sport : "has"

    User {
        INT id PK
        VARCHAR(45) email
        VARCHAR(255) password
        VARCHAR(45) fname
        VARCHAR(45) lname
    }

    Location {
        INT id PK
        INT street_number
        VARCHAR(255) street_name
        VARCHAR(255) city
        INT post_code
        INT User_id FK
    }

    Reservation {
        INT id PK
        TIME time
        DATE date
        INT User_id FK
        INT Court_id FK
    }

    Court {
        INT id PK
        VARCHAR(45) name
        TIME open
        TIME close
        INT limit
        INT Location_id FK
    }

    Sport {
        INT id PK
        VARCHAR(255) name
    }

    Court_Sport {
        INT Sport_id PK,FK
        INT Court_id PK,FK
    }
```

## Entities

| Entity | Description | Important rules / constraints |
|--------|-------------|-------------------------------|
| User | Stores basic info for users |  |
| Location | Stores basic info for locations | User_id represents the locations owner(user) |
| Reservation |  |  |
| Court |  |  |
| Sport | Sports each court can be played on |  |
| Court_Sport |  |  |

## Business rules
<!-- e.g. "A room cannot have two bookings that overlap in time." -->
