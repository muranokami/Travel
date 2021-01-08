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

URL
https://travel-32455.herokuapp.com/

テスト用アカウント
mail: test@test.com
password:223y5Wz

利用方法
ログイン機能をつけ誰が入ってきたかがわかるようにし、大勢のグループを作って旅行の計画を立てるために、カレンダー機能や、コミュニケーションをとるためのチャットをつけています。

目指した課題解決
今の現状、コロナウイルスの影響で外出などができない状況なので、コロナウイルスが収まり次第このアプリを使い旅行に行って欲しいと思い作成しました。

洗い出した要件	
 ユーザー機能や、コメント機能を、カレンダーの作成をしました。

実装した機能についてのGIFと説明
ユーザー機能を作らないと、誰と誰が話しているのかがわからなくなるから作りました。
カレンダー昨日は、旅行をいついくかをメモできるようにすることで計画を立てやすくしました。
コメント機能は集まってコミュニケーションをとる時に最適だと思ったから作成しました。

実装予定の機能
ブログ機能をつける予定 (他にもつけるかも)



