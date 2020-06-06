# DB設計

## usersテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|mail|integer|null: false|
|password|integer|null: false|

### Association
- has_many :posts
- has_many :user_groups
- has_many :groups, through: :user_groups

## postsテーブル

|Column|Type|Options|
|------|----|-------|
|user|references|null: false, foreign_key:true|
|text|text||
|img|string||
|created_at|string|null: false|

### Association
- belongs_to :user
- belongs_to :group


## user_groupsテーブル

|Column|Type|Options|
|------|----|-------|
|user|references|null: false, foreign_key:true|
|group|references|null: false, foreign_key:true|


### Association
- belongs_to :user
- belongs_to :group





## groupsテーブル

|Column|Type|Options|
|------|----|-------|
|user|references|null: false|
|group|references|null: false|
|name|string|null: false|


### Association
- has_many :user_groups
- has_many :users, through: :user_groups
- has_many :posts
