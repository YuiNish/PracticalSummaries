# Ubuntuで外部ストレージの接続と取り外しをしたい

1. 外部ストレージを端末に接続する
2. コマンドラインで`sudo fdisk -l`と入力し, 接続されているデバイスを確認する (外部ストレージを接続する前に確認しておくと分かりやすいかも).
3. */dev/sdb1*のように, 接続したストレージデバイスの接続pathを確認する.
4. `sudo mount /dev/sdb1 /mnt`でマウントを行う.  
すると, 外部ストレージが認識されて, コピーなどができるようになる.
5. 外部ストレージにコピーするなり, コピーしてくるなり, 色々行いたい操作をする.
6. 外部ストレージを取り外すときは, `sudo umount /mnt/`でアンマウントすることで, 外部ストレージを安全に取り外すことができる.

マウントするディレクトリは/mntでなくとも, 事前にマウントポイントに使うディレクトリを作成しておけば, その作成したディレクトリをマウントポイントにすることも可能.
