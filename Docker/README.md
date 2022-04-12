# Dockerについて色々記録
Dockerについて学習したことをmemo.

## DockerfileとDocker compose
Dockerfileはimageを作成. Docker composeはコンテナから環境まで一括で作成可.

## volume
* bind  
bindマウントは, Docker Engine外のマシン上のディレクトリ上にマウントする.  
`docker run [~~] -v [記憶域path]:[コンテナの記憶域path]`
  
* volume  
volumeマウントは, Docker Engine管理の範囲内にvolumeを作成し, ディスクとしてマウントする.  
`docker run [~~] -v [ボリューム名]:[コンテナの記憶域path]`

## docker run
option

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
