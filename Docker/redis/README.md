# DockerでRedis
redisをdockerで実装してみた記録.  
Windows 10 pro, power shell, ubuntu(wsl)
1. redisのimageを引っ張ってくる(official). `docker pull redis`でredisのimageを入手.
2. volumeを作る. `docker volume create [適当な名前:ここではredis_data]`でvolume作成.
3. 新しいコンテナを作成, 実行. `docker run -v redis_data:/var/lib/docker/volumes/redis_data/ -p 6379:6379/tcp --name [コンテナ名:ここではredis_db] -d redis`でコンテナの作成と起動.
4. redisには, `redis-cli`でログインする.
