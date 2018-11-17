# README


## userテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|references|foreign_key: true|
|group_id|references|foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user


## groupテーブル

|Column|Type|Options|
|------|----|-------|
|name|sring|null: false, foreign_key: true|

### Association
- has_many :users
- has_many :groups

## messageテーブル

|Column|Type|Options|
|------|----|-------|
|text|string|
|image|string|
|group|references|foreign_key: true, index: true|
|user|references|foreign_key: true, index: true|

### Association
- belong_to :user
- belong_to :group


## group_userテーブル

|Column|Type|Options|
|------|----|-------|
|user|references|foreign_key: true|
|group|references|foreign_key: true|

### Association
- has_many :groups
- has_many :users, through: :gorup_users


* ...
