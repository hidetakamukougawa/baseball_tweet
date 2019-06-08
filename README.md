# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

## tweetsテーブル

|Column|Type|Options|
|------|----|-------|
|text|text|null: false|
|image|string|null: false|
|user_id|references|foreign_key: true|

### Association
- belongs_to :user
- has_many :comments

## usersテーブル
|Column|Type|Options|
|------|----|-------|
|nickname|string|null: false, unique: true|
|email|string|null: false, unique: true|

### Association
- has_many: tweets
- has_many: comments

## commentsテーブル

|Column|Type|Options|
|------|----|-------|
|text|text|null: false|
|user_id|references|foreign_key: true|
|tweet_id|references|foreign_key: true|



