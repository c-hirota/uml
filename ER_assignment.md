``` mermaid
    erDiagram
        STUDENT ||--o{ COURSE:""
        COURSE ||--o{ CLASS:""
        STUDENT }|--o{ CLASS:""
        STUDENT {
            number id
            string name
            string email
            string address
        }
        COURSE {
            number id
            string course_name
            string title
            number points
        }
        CLASS {
            number id
            string class_name
            number num_resistered
            timestamp class_date_time
        }
```