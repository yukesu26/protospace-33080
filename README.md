# テーブル設計

## users テーブル

| Column     | Type   | Options     |
| --------   | ------ | ----------- |
| email      | string | null: false |
| password   | string | null: false |
| name       | string | null: false |
| profile    | text   | null: false |
| occupation | text   | null: false | 
| position   | text   | null: false |


## prototypes テーブル

| Column     | Type       | Options                        |
| ------     | ---------- | ------------------------------ |
| user       | references | null: false, foreign_key: true |
| concept    | text       | null: fails                    |
| title      | string     | null: fails                    |
| catch_copy | text       | null: fails                    |




## comments テーブル

| Column    | Type       | Options                        |
| -------   | ---------- | ------------------------------ |
| text      | text       | null: false                    |
| user      | references | null: false, foreign_key: true |
| prototype | references | null: false, foreign_key: true |