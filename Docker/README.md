# Dockerについて色々記録
Dockerについて学習したことをmemo.

## DockerfileとDocker compose
Dockerfileはimageを作成. Docker composeはコンテナから環境まで一括で作成可.

## docker volume
* bind  
bindマウントは, Docker Engine外のマシン上のディレクトリ上にマウントする.  
`docker run [~~] -v [記憶域path]:[コンテナの記憶域path]`
  
* volume  
volumeマウントは, Docker Engine管理の範囲内にvolumeを作成し, ディスクとしてマウントする.  
`docker run [~~] -v [ボリューム名]:[コンテナの記憶域path]`

## docker run
docker runはdocker createとdocker startを一体化したものだそう.

* option  

| option | 内容 |
| :---: | :---: |
| --iname [コンテナ名] | コンテナ名 |
| -p [hostポート]:[containerポート] | ポート指定 |
| -v [hostディレクトリ]:[containerディレクトリ] | volumeマウント |
| -d | バックグランド実行 |
| -i | コンテナ起動後操作 |
| -t | 特殊キー(tabによる入力補助など？) |

### memo
Dockerでサーバを立ててみて -> 起動後にしばらくの間, 思ったような挙動をしないことがある?  
特に, jupyter lab上からの接続で何か引っかかることがしばしば...  
-> jupyterの問題?

## docker commit
docker commitでコンテナをイメージとして保存. コンテナで色々とインストールや開発を行っているとついつい保存し忘れたりしてしまうので, 新しいイメージとしてある程度の間隔で保存しておくと良いかも.  
`docker [コンテナID] [レポジトリ(:=イメージ名)]`で保存できる.

## docker save
docker saveでイメージを保存して外部に移動したりできる.  
`docker save [レポジトリ(:=イメージ名)] > [保存したいファイル名].tar`
