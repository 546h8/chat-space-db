# DB設計

## usersテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|mail|integer|null: false|
|password|integer|null: false|

### Association
- has_many :posts


## postsテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key:true|
|text|text|null: false|
|img|string||
|created_at|string|null: false|

### Association
- belongs_to :user
- belongs_to :group


## user-groupsテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key:true|
|group_id|integer|null: false, foreign_key:true|


### Association
- belongs_to :user
- belongs_to :group





## groupsテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key:true|
|group_id|integer|null: false, foreign_key:true|
|name|string|null: false|


### Association
- has_many :user_groups
- has_many :posts



