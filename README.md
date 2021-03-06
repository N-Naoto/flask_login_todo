# 作った背景
ログイン機能が実装できれば、ものづくりの幅が広がると思い、作成しました。

# 使ったもの
ログイン機能のある、Todoアプリ。(レスポンシブ対応)
pythonのウェブアプリケーションフレームワークであるFlaskを使用。
Djangoもあったが、Flaskの方が個人開発向けとのことで採用。
PythonのORマッパーのsqlalchemyを使用して、CRUD処理を実装。
データベースにはMySQLを使用。
今回のアプリケーションの機能がシンプルなものだったため、処理の早いMySQLを採用。

# 作成期間
12日間

# 見てほしいところ
データーベースを利用したアプリケーションを作成するのが初めてな状態から、見せれる形まで作り切ることができた点。

# 苦労した点
行きあたりばったりの開発になってエラーとたくさん出会った。

ローカル環境からherokuでデプロイするまでにとても時間を使いました。
- sqlite3からMySQLに変更
- herokuにデプロイ時、パッケージのバージョンの違いでエラーの発生。
- デプロイできても、アプリケーションエラーで画面に表示されない。
- ログイン画面でデータベースを使おうとした際、繋がっていないとエラー。
- ログインしてしばらく立つと、セッションが切れてアプリが動かなくなる。

# 改善点
- テーブルの主キーであるIDが、項目を追加されるたびに10ずつ増えてしまう点。
- 会員登録の際、ユーザ名を空白にした状態でも、登録ができてしまう。
- 同様にパスワードを入力しなくても、登録できてしまう。
- MySQLを使用する際、サーバの接続が切れてしまうエラーが発生。
- 作るのが目的になっており、ユーザ目線での開発が足りていない。