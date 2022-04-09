# Dockerについて色々記録
Dockerについて学習したことをmemo.

## DockerfileとDocker compose
Dockerfileはimageを作成. Docker composeはコンテナから環境まで一括で作成可.

## volume
* bind
bindマウントは, Docker Engine外のマシン上のディレクトリ上にマウントする.

* volume
volumeマウントは, Docker Engine管理の範囲内にvolumeを作成し, ディスクとしてマウントする.

### memo
Dockerでサーバを立ててみて -> 起動後にしばらくの間, 思ったような挙動をしないことがある?  
特に, jupyter lab上からの接続で何か引っかかることがしばしば...  
-> jupyterの問題?
