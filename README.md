# DB設計

## usersテーブル

|Column|Type|Options|
|------|----|-------|
|username|integer|null: false|
|mail|integer|null: false|
|password|integer|null: false|

### Association
- has_many :post
- has_many :user-name


## postsテーブル

|Column|Type|Options|
|------|----|-------|
|user-id|integer|null: false, foreign-key:true|
|text|text|null: false|
|created-at|string|null: false|

### Association
- belongs_to :post


## user-groupsテーブル

|Column|Type|Options|
|------|----|-------|
|user-id|integer|null: false, foreign-key:true|
|group-id|integer|null: false, foreign-key:true|


### Association
- belongs_to :user
- belongs_to :group



## groupsテーブル

|Column|Type|Options|
|------|----|-------|
|user-id|integer|null: false, foreign-key:true|
|group-id|integer|null: false, foreign-key:true|
|groupname|integer|null: false|


### Association
- has_many :user-groups


