# README

## users テーブル

| Column     | Type   | Options     |
| ---------- | ------ | ----------- |
| email      | string | null: false |
| password   | string | null: false |
| name       | string | null: false |
| profile    | text   | null: false |
| occupation | text   | null: false |
| position   | text   | null: false |

### Association
- has_many :comment



## comments テーブル

| Column    | Type       | Options     |
| --------- | ---------- | ----------- |
| text      | text       | null: false |
| user      | references | null: false |
| prototype | prototype  | null: false |

### Association
- belongs_to :users

## prototypes テーブル

| Column     | Type       | Options     |
| ---------- | ---------- | ----------- |
| title      | string     | null: false |
| catch_copy | references | null: false |
| concept    | text       | null: false |
| user       | references | null: false |


### Association
