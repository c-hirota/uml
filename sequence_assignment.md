``` mermaid
sequenceDiagram
    participant ユーザ
    participant Vue
    participant Laravel
    participant Database
    ユーザ->>+Vue: ログインボタンクリック
    Vue->>+Laravel: ログインAPI
    Laravel->>+Database: SQL
    Note right of Database: 認証テーブル参照
    Database->>-Laravel: Result
    alt ログイン成功
    Laravel->>Vue: success
    else 失敗
    Laravel->>Vue: failure
    end
    deactivate Laravel
    Vue->>-ユーザ: 結果表示
```