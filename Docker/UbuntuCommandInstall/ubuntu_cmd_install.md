# Dockerで遊んでいたら…
 Docker内でubuntuを対話モードで色々なコマンドを試してみようとしたところ、
 **nslookup**や**curl**が入ってない(未インストール)というエラーが発生したため、
 とりあえずコマンドをインストールする方法をメモとして残しておく.
1. nslookup
コマンドラインで`apt-get install dnsutils`を実行する.  

1. curl
コマンドラインで`apt-get install curl`を実行する.  


> # 参考
> [410gone.click](https://410gone.click/blog/ubuntu-dig-nslookup-nsupdate%E3%82%B3%E3%83%9E%E3%83%B3%E3%83%89%E3%82%92%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB%E3%81%99%E3%82%8B/)
> [あんらぶぎーくどっとこむ](https://410gone.click/blog/ubuntu-dig-nslookup-nsupdate%E3%82%B3%E3%83%9E%E3%83%B3%E3%83%89%E3%82%92%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB%E3%81%99%E3%82%8B/)
