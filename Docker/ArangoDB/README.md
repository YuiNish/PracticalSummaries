# ArangoDBをDockerで
ArangoDBをDcokerで導入してみた記録.  
`docker pull arangodb`でイメージを引っ張ってくる.  
`docker run -e ARANGO_ROOT_PASSWORD=arango -v arangodb_volume:/var/lib/docker/volumes/arangodb_volume/ -p 8529:8529 --name arango_db2 -d arangodb`でコンテナ運用開始.  
volumeについては, 自由に`docker volume create [volume名]`で作成しておきましょう.  
ブラウザ(localhost:8529)でログインが可能. ***ユーザ名:root, パス:指定したもの***
