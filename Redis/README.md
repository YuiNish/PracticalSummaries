# Redis
Redisについて色々記録を残しておく.

## WindowsにRedisを導入
microsoft公式のGitHubからインストール可  
インストーラ→Redis-x64-3.X.XXX.msi  
(microsoftarchive/redis)[https://github.com/microsoftarchive/redis/releases]

## Redisモジュールのインストール
anacondaプロンプトに`pip install redis`と入力して実行することでインストール可.  
Pythonのファイル内でimportすることでエラーが出ないことを確認できる.

## RedisをPythonで触ってみる際には
自分のPC内で動かす際にはホストは ***"localhost"*** とし、portは標準で ***6379*** となっている.
