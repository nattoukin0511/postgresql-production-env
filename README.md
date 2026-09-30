#概要

PostgreSQLを単体で構築し、データベース作成、ユーザー作成、権限付与、接続確認実施

#1. 構築手順
 #PostgreSQLインストール
  sudo apt update
  sudo apt install postgresql postgresql-contrib

 #サービス起動確認
  systemctl status postgresql
 
 #PostgreSQLへ接続
  sudo -u postgres psql

 #データベース作成
　CREATE DATABASE testdb;

 #ユーザー作成
　CREATE USER testuser WITH PASSWORD 'password';

 #権限付与
　GRANT ALL PRIVILEGES ON DATABASE testdb TO testuser;

 #接続確認
　\conninfo

 #バージョン確認
　SELECT version();

 #POSTGRE抜ける
　\q

 #POSTGRE状態確認
　systemctl status postgresql


#2.発生したエラー

※今回は発生なし


#3.修正ファイル

※今回は設定ファイルの修正なし


#4学んだこと
　PostgreSQLはDBとユーザーを分けて管理する。
　CREATE DATABASEでデータベースを作成できる。
　CREATE USERで接続ユーザーを作成できる。
　GRANTでデータベース権限を付与できる。
　psqlを利用してPostgreSQLへ接続できる。
　systemctlによりPostgreSQLサービスの状態を確認できる



