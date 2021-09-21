# DockerでSQL
PostgeSQLをDockerで実装してみた記録.  
Windows 10 pro, power shell, Ubuntu

1. PostgreSQLのimageを引っ張ってくる.
`docker pull postgres`をpower shellで入力する.

2. PostgreSQLの永続化
`docker create volume [適当な名前：ここでは例としてpostgres_data]`でvolume作成(power shell).

3. run
`docker run -p 5432:5432/tcp --name [コンテナ名：ここでは例としてpostgres_volume2] -e POSTGRES_PASSWORD=mypostgres -d -v postgres_data:/var/lib/postgresql/ postgres`をpower shellで入力.  
ポート指定とマウントを忘れないように注意する.  

4. 2パターンのログイン方法  
  1. power shellでログイン
    `docker exec -it postgres_volume psql -U postgres`を入力するとログイン可.
  2. Ubuntuでログイン
    `psql -h 127.0.0.1 -U postgres`を入力し実行して,パスワード入力しログイン.

恐らく言葉の意味や使い方がかなり無茶苦茶なので,そこはご容赦ください...
