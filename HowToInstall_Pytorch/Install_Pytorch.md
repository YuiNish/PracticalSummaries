# Pytorchのインストール(Win10)
1. まずはじめに、[Pyorch](https://pytorch.org/)にアクセスする.  
すると、ここで以下のような画面が現れる.  
![pytorchダウンロード方法選択画面]()  
このとき、CUDAはNVIDIAのGPUの有無(バージョン確認)を訪ねているので、  
PCに搭載されている場合はバージョンの確認を行い、対応するバージョンを選択し、  
NVIDIAのGPU(対応するもの)がない場合にはNoneを選択する.
2.上記の選択が終了したら、下部に記してあるコマンドをコピーし、  
Anaconda Promptにペーストして実行する.  
すると、ダウンロードとインストールが完了する.
>[PyTorch のインストール（Windows 上）https://www.kkaneko.jp/tools/win/pytorch.html](https://www.kkaneko.jp/tools/win/pytorch.html)

#JupyterLabでPytorchがimoprtできずエラーになるときの対処法
Pytorchインストール完了後、実際にコードを動かそうとしてみたところ、  
`No module named 'torch'`  
と表示された.
解決策としては、ANACONDA NAVIGATERからJupyterLabを開くことで、  
このエラーは表示されずに動作した.
>[ModuleNotFoundError: No module named 'torch' #4827 https://github.com/pytorch/pytorch/issues/4827](https://github.com/pytorch/pytorch/issues/4827)
