# DockerでSQL
PostgeSQLをDockerで実装してみた記録.  
Windows 10 pro, power shell, Ubuntu

1. PostgreSQLのimageを引っ張ってくる.
`docker pull postgres`をpower shellで入力する.

2. PostgreSQLの永続化
`docker volume create [適当な名前：ここでは例としてpostgres_data]`でvolume作成(power shell).

3. run
`docker run -p 5432:5432/tcp --name [コンテナ名：ここでは例としてpostgres_volume2] -e POSTGRES_PASSWORD=mypostgres -d -v postgres_data:/var/lib/postgresql/ postgres`をpower shellで入力.  
ポート指定とマウントを忘れないように注意する.

4. 2パターンのログイン方法
    1. power shellでログイン
    `docker exec -it postgres_volume psql -U postgres`を入力するとログイン可.
    2. Ubuntuでログイン
    `psql -h 127.0.0.1 -U postgres`を入力し実行して,パスワード入力しログイン.
5. docker run & stop
コンテナを停止させるときは, `docker stop [コンテナ名]`で停止する.  
コンテナ動かすときは, `docker start [コンテナ名]`で動作開始.

恐らく言葉の意味や使い方がかなり無茶苦茶なので,そこはご容赦ください...

# pythonでpostgreSQLに接続して動かす
1. psycopg2をインストールする.
`pip install psycopg2`でpsycopg2をインストール. エラーが出た場合, `pip install psycopg2-binary`を試してみる.
2. flaskのインストール
`pip install flask`でインストール.

# psycopg2でDATABASE CREATE
jupyterでどうぞ.  
`import psycopg2
from psycopg2.extensions import ISOLATION_LEVEL_AUTOCOMMIT

host = 'localhost'
port = 5432
dbuser = 'postgres'
dbpass = 'mypostgres'

con = psycopg2.connect(host=host, port=port, user=dbuser, password=dbpass)

cursor = con.cursor()
con.set_isolation_level(ISOLATION_LEVEL_AUTOCOMMIT)
cursor.execute("CREATE DATABASE test2")

cursor.close()
connection.close()`
