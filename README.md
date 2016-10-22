#DB設計

##テーブル

* users
* groups
* messages

##アソシエーション

###userモデル

* has_many :messages
* belongs_to :group

###groupモデル

* has_many :users
* has_many :messages

###messageモデル

* belongs_to :user
* belongs_to :group

##テーブルのカラム(カラムの型)

###usersテーブル

* name(string) null: false
* group_id(integer)
* deviseによるカラム諸々

###groupsモデル

* name(string) null: false

###messagesモデル

* body(text) add_index
* image(string) add_index
* user_id(integer)
* group_id(integer)
