``` mermaid
erDiagram
    STUDENT ||--o{ COURSE
    STUDENT {
        number id
        string name
        string email
        string address
    }
    COURSE ||--o{ CLASS
    COURSE {
        number id
        string course_name
        string title
        number points
    }
    STUDENT }|--o{ CLASS
    CLASS {
        number id
        string class_name
        number num_resistered
        timestamp class_date_time
    }
```