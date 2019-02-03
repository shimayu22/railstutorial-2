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

2019/02/03
2.1までやった

各ユーザーには、重複のない一意のキーとなるinteger型のID番号 (idと呼びます) を割り当て、
このIDに加えて一般公開されるstring型の名前 (name)、そして同じくstring型のメールアドレス (email) を持たせます。

マイクロポストのデータモデルはユーザーよりもさらにシンプルです。
idとマイクロポストのテキスト内容を格納するtext型のcontentだけで構成されています1。
しかし実際には、マイクロポストをユーザーと関連付ける (associate) 必要があります。
そのため、マイクロポストの投稿者を記録するためのuser_idも追加します。