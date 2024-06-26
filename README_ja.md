# WordPressテーマ開発環境

![docker-wordpress](https://github.com/khalednigrou/docker-wordpress/assets/4309858/70c4ec01-8498-4c7f-94ff-a85f6bf40ce0)

[Read in English](./README.md) | [Lire en Français](./README_fr.md)

このプロジェクトは、WordPressプロジェクトのためのテーマ開発を簡素化するために、Dockerベースの環境を提供します。事前に設定された`docker-compose.yml`ファイルを利用して、WordPressインスタンス、MySQLデータベース、およびデータベース管理のためのphpMyAdminを、隔離されたコンテナ内でセットアップします。

## はじめに

この開発環境を使用するには、以下の手順に従ってください：

1. **リポジトリを** あなたのローカルマシンにクローンします。

2. **プロジェクトディレクトリに移動します**。`docker-compose.yml`ファイルが位置しています。

3. **テーマファイルを** `wp-projects`フォルダに追加します。このフォルダはWordPressコンテナにマウントされ、WordPressがあなたのテーマを認識して使用できるようになります。

4. **`.env.example`ファイルを** `.env`にコピーし、必要に応じて環境変数を変更します。

   ```sh
   cp .env.exemple .env  
   ```

5. **コンテナを開始します**。ターミナルで以下のコマンドを実行します：

   ```sh
   docker-compose up -d
   ```

6. **WordPressにアクセスします**。ウェブブラウザで`http://localhost:8080`に移動します。ここで、テーマをアクティベートして開発を開始できます。

7. **phpMyAdminにアクセスします**。`http://localhost:8081`に移動します。このインターフェースを使用して、WordPressデータベースを管理します。

## 重要な注意点

- MySQLデータベースの認証情報およびその他の環境変数は、`.env`ファイルで定義されています。これらの値は、あなたのニーズに応じて変更できます。

- `wp-projects`フォルダは、`.gitignore`ファイルで指定されているようにGitによって無視されます。これにより、テーマファイルが誤ってバージョン管理にコミットされることがありません。

- コンテナを停止するには、ターミナルで`docker-compose down`を実行します。

この環境は、WordPressテーマの開発プロセスを簡素化するために、すぐに使用できるWordPressセットアップを提供します。`wp-projects`フォルダにテーマを追加し、コンテナ化された環境でテーマの構築を開始してください。


