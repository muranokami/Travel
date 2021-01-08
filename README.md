#  DB設計

##  account table

| Column             | Type   | Options                   |
|--------------------|--------|---------------------------|
| email              | string | null: false, unique: true |
| nickname           | string | null: false               |
| encrypted_password | string | null: false               |
| birthday           | date   | null: false               |
| first_name         | string | null: false               |
| last_name          | string | null: false               |
| first_name_kana    | string | null: false               |
| last_name_kana     | string | null: false               |
| profile            | text   | null: false               |

### Association

- has_many :calenders table
- has_many :comments

##  calenders table

| Column                 | Type       | Options                        |
|------------------------|------------|--------------------------------|
| name                   | string     | null: false                    |
| day                    | integer    | null: false                    |
| action                 | integer    | null: false                    |




### Associationx

- belongs_to :account
- has_many :comments

## comments table

| Column           | Type       | Option                         |
|------------------|------------|--------------------------------|
| user             | references | null: false, foreign_key: true |
| text             | references | null: false, foreign_key: true |

### Association

- belongs_to :account
- has_many :calender

アプリケーション名
Travel

アプリケーション概要
旅行に一緒に同行する人と相談しながら、プランを立てることができる

