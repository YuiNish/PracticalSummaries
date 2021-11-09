# DockerでmongoDBを使ってみた記録
`docker pull mongo`で公式のimageを引っ張ってくる.  
毎回のごとく, volumeを作る. `docker volume create [volume名]`でvolume作成.  
`docker run -v [volume名]:[マウント場所] -p 27017:27017 --name mongo_db -d mongo`でmongoDBを動作させる.  
