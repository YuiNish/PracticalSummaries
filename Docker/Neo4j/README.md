# DockerでNeo4jを動かしてみた記録
`docker pull neo4j`で公式からイメージを引っ張ってくる.  
念のため, `docker volume create [volume名]`でvolumeを作成.  
`docker run -v neo4j_volume:/var/lib/docker/volumes/neo4j_volume/ -p 7474:7474 -p 7687:7687 --name neo4j_db10 -d neo4j`でコンテナ作成.  
localhost:7474/browserをブラウザで入力して接続すると, ログイン画面が表示される.

### Neo4j python ドライバ
`pip install neo4j`でインストール可.
