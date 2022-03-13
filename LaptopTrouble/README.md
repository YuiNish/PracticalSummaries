# HPのノートPCで充電できないトラブルの解決法
方法:15秒間電源ボタンを長押し.  
上記の動作をするだけで改善された.  
動作確認機種:HP Spectre x360 Convertible 15-ch0xx  
※実行する際は自己責任でお願いします.
> [HP公式](https://support.hp.com/jp-ja/document/c04094174)

# HPのノートPCでの仮想化の有効化
なぜかWSLがインストールしても動かなかったので調べたところ、BIOSの設定に原因があることが分かったので、メモとして残す.  
> [公式参考](https://support.hp.com/jp-ja/document/c03836690)
1. BIOSの起動->起動時F10を押す.  
1. System ConfigurationのVirtualization TechnologyをEnableにする.  
1. あとはBIOS終了->再起動
