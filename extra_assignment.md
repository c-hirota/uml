# extra assignment

```mermaid
erDiagram
    PLAYOFFGROUND }|--|{ ROUNDSTATS: ""
    PLAYOFFGROUND {
        number team1-ID
        number team2-ID
        timestamp start-time
        timestamp end-time
        number round-number
    }
    ROUNDSTATS {
        number ID
        number shoot-number
        number goal-leader-ID
        number assist-leader-ID
        number penalty-leader-ID
        number plus-minus-leader-ID
        number face-off-leader-ID
        number shoot-leader-ID
    }
    PLAYOFFGROUND }|--|{ USERSTATS: ""
    USERSTATS {
        number ID
        number round-ID
        number goal-leader-ID
        number assist-leader-ID
        number penalty-leader-ID
        number plus-minus-leader-ID
        number face-off-leader-ID
        number shoot-leader-ID
        number shoot-number
        number user-ID
    }
    PLAYOFFGROUND ||--|{ HOCKEYGAMES: ""
    HOCKEYGAMES {
        number ID
        number round-ID
        timestamp start-time
        string explanation
        number team1-ID
        number team2-ID
    }
    HOCKEYGAMES }|--|{ HOCKEYTEAMS: ""
    HOCKEYTEAMS {
        number ID
        string full-name
        image logo
        number team-ID
    }
    HOCKEYGAMES }|--|{ USERSCORES: ""
    USERSCORES {
        number ID
        number game-ID
        number team1-score
        number team2-score
        number user-ID
    }
    HOCKEYGAMES }|--|| GAMESCORES: ""
    GAMESCORES {
        number ID
        number team1-score
        number team2-score
    }
    HOCKEYTEAMS ||--|{ HOCKEYTEAMPLAYERS: ""
    HOCKEYTEAMPLAYERS {
        number ID
        number team-ID
        string first-name
        string family-name
        number uniform-number
        string manipulation
    }
    USERSTATS }|--o| USER: ""
    USER {
        number ID
        string user-name
        string password
    }
    USER ||--|| USERINFO: ""
    USERINFO {
        number ID
        string first-name
        string family-name
        string email
        number round1-point
        number round2-point
        number round3-point
        number round4-point
    }
    USER |o--|{ USERSCORES: ""
```
