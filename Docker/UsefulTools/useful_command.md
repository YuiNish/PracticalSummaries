# Dockerで遊ぶときに使えるコマンドなど
1. コンテナのIPアドレスを得る方法  
`docker inspect --format '{{.NetworkSettings.IPAddress}}' *コンテナ名/コンテナID*`を実行する.
> ### 参考
> 1. [it-swarm.dev](https://www.it-swarm.dev/ja/docker/%E3%83%9B%E3%82%B9%E3%83%88%E3%81%8B%E3%82%89docker%E3%82%B3%E3%83%B3%E3%83%86%E3%83%8A%E3%81%AEip%E3%82%A2%E3%83%89%E3%83%AC%E3%82%B9%E3%82%92%E5%8F%96%E5%BE%97%E3%81%99%E3%82%8B%E6%96%B9%E6%B3%95/1073314901/)
