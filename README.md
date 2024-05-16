# Mary-s-todo-list
## ■サービス概要
「メリーさんのTodo管理アプリ」は、通常のTodoリストアプリとは異なり、日本の怪談「メリーさんの電話」をモチーフにしたユニークな体験を提供します。  
目標期限が過ぎたタスクがあると、メリーさんが徐々に近づいてくるようなメッセージと一緒にそのTodoが終わっていないことを伝えてくる仕組みです。  
通常のタスク管理じゃ物足りない、遊び要素が欲しいという人むけのタスク管理アプリです。  

## ■ このサービスへの思い・作りたい理由
私自身、ToDoリストを使う際に、難しいタスクを後回しにしたり、どうでもいいタスクまで追加してしまうことがよくありました。そんな経験から、効果的なタスク管理法を模索していたところ、「恐怖の一時間」という手法を知りました。

この「恐怖の一時間」というアイデアは、ToDoリストとは少し趣が異なりますが、恐怖を要素に取り入れるという着想に魅力を感じました。そこで、日本の怪談「メリーさんの電話」をモチーフにして、新しいToDoアプリを作成することにしました。

このサービスは、楽しさを感じながらタスク管理してもらうことを目指しています。  

## ■ ユーザー層について
ユニークなタスク管理アプリを探しているユーザー
怪談やホラーが好きなユーザー

## ■サービスの利用イメージ
ユーザーは通常のTodoリストと同様にタスクを追加します。
目標期限内で使う分には他のタスク管理アプリと特に変わりません。  
しかし、目標期限を過ぎたタスクがあると、メリーさんが未完了のタスクの状況によってユーザーにメッセージを送信します。  
メリーさんからの通知を受けて、ユーザーはタスクを完了させることでメリーさんを追い払います。  
メリーさんを追い払えずにタスクの最終完了期限が過ぎた場合、タスクを期間内に完了させるためのヒントやアドバイス情報を表示します。  

## ■ ユーザーの獲得について
コミュニティやSNSでの発信

## ■ サービスの差別化ポイント・推しポイント
ユニークな体験: 通常のTodoアプリとは異なる、メリーさんの通知機能が差別化ポイントです。  
怖さと楽しさのバランス: ユーザーは緊張感を味わいながらも楽しむことができます。

## ■ 機能候補
現状作ろうと思っている機能、案段階の機能をしっかりと固まっていなくても構わないのでMVPリリース時に作っていたいもの、本リリースまでに作っていたいものをそれぞれ分けて教えてください。
### 【MVPリリース】
* ユーザー登録機能
* ユーザー削除(退会)機能
* ユーザー情報機能
* ログイン機能
* ログアウト機能
* タスク管理機能（追加・編集・削除）
* Linebot用いた機能
  * タスク通知機能
  * メリーさんからのメッセージ機能


### 【本リリース】
* タスクの自動削除機能
* タスクの検索機能
* タスクの並べ替え機能
* 位置情報を取得するAPI（検討中）
    * メリーさんからのメッセージのため
* 利用規約
* プライバシーポリシー




## ■ 機能の実装方針予定
一般的なCRUD以外の実装予定の機能についてそれぞれどのようなイメージ(使用するAPIや)で実装する予定なのか現状考えているもので良いので教えて下さい。
* 一般的なTodoアプリ機能を実装
* バックグラウンドで目標期限を取得する機能を実装
* 通知機能を実装（Linebotを使用予定）
* 目標期限が過ぎた場合、UIを通常時から変更させる
* 位置情報を取得機能を実装しメッセージのバリエーションを増やす

## ■使用予定の技術スタック
### 開発環境
- Docker
- Docker Compose

### サーバサイド
- Ruby on Rails 7系
  - Ruby 3.2.2
  - Rails 7.0.4.3

### フロントエンド
- 初期リリースではRailsを使用
- React（Railsで全て作成し本リリース後に徐々に移行）
- CSSフレームワーク: Bootstrap 5系

### WebAPI
- LINE Messaging API
- Geolocation API (検討中)

### インフラ
- Webアプリケーションサーバ: Amazon EC2 または AWS Elastic Beanstalk
- ファイルサーバ: AWS S3
- セッションサーバ: Amazon ElastiCache for Redis
- データベースサーバ: Amazon RDS for PostgreSQL

### その他
- VCS: GitHub
- CI/CD: GitHub Actions

## ■画面遷移図
[Figma](https://www.figma.com/design/GyVsRGDJAEHDvSPuTnjwvn/Mary-s-todo-list?node-id=0%3A1&t=rRKr0DnFP1VOrjKy-1)

## ■ER図
[![Image from Gyazo](https://i.gyazo.com/36a089531dee7b7523965d409b2ca876.png)](https://gyazo.com/36a089531dee7b7523965d409b2ca876)