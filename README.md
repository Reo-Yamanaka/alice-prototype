# DB設計

## Tweets Table

| Column        | Type         | Option             |
|---------------|--------------|--------------------|
| name          | string       | null: false        |
| text          | string       | null: false        |
| image         | text         | null: false        |

### Association

* has_one: users
* has_many: comments


## Users Table

| Colum              | Type         | Option              |
|--------------------|--------------|---------------------|
| email              | string       |
| encrypted_password | string       |

### Association

* has_many: tweets
* has_many: comments 


## Comments Tables

| Column        | Type         | Option              |
|---------------|--------------|---------------------|
| user_id       | integer      |
| tweet_id      | integer      | 
| text          | text         | nul: false          |

### Association

* 