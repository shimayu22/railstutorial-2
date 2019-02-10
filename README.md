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

2019/02/10
2.2
toy_appフォルダに遷移してからコマンドを打つこと

演習
1.
<p id="notice">User was successfully created.</p>
↓リロード後
<p id="notice"></p>

2.
名前だけ入る（チェック処理がない）

3.
そのまま入る（チェック処理がない）

4.
Are you sure?のことなのか、単にUser was successfully destroyed.って出ることなのか

2.2.2
MVCとRESTの話

2.3

演習
わからなかった
https://qiita.com/mochikichi321/items/afc685412409ac6112ad
ここを参考にした

2.3.4
(Rubyでは継承関係を<記号で表現します)

モデルの継承関係と同様に、UsersコントローラもMicropostsコントローラも最終的には
ActionController::Baseという基本クラスを継承しています。このため、どちらのコントローラも
モデルオブジェクトの操作や、送られてくるHTTP requestのフィルタリング、
ビューをHTMLとして出力などの多彩な機能を実行できるようになっています。
Railsのコントローラは必ずApplicationControllerを継承しているので、
Applicationコントローラで定義したルールは、
アプリケーションのすべてのアクションに反映されます。

2.5
リスト 1.15: クラウドIDE上でHerokuをインストールするコマンド
$ source <(curl -sL https://cdn.learnenough.com/heroku_install)