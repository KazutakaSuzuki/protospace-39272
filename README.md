# テーブル設計
## usersテーブル

| Column              | Type   | Options                   |
| ------------------- | -------| ------------------------- |
| email               | string | NULL: false, unique: true |
| encrypted_password  | string | NULL: false               |
| name                | string | NULL: false               |
| profile             | text   | NULL: false               |
| occupation          | text   | NULL: false               |
| position            | text   | NULL: false               |

## prototypeテーブル

| Column     | Type       | Options                       |
| ---------- | ---------- | ----------------------------  |
| title      | string     | NULL:false                    |
| catch_copy | text       | NULL:false                    |
| concept    | text       | NULL:false                    |
| user       | references | NULL:false, foreign_key: true |


## commentsテーブル

| Column    | Type       | Options                       |
| --------  | ---------- | ----------------------------- |
| content   | text       | NULL:false                    |
| prototype | references | NULL:false, foreign_key: true |
| user      | references | NULL:false, foreign_key: true |

