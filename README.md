## このリポジトリについて

このリポジトリは、さくらのVPSを利用するにあたって便利なスクリプトを私自身のためにインターネット上からアクセス可能にするために作成されたものです。  
検証等一切行っていない個人的なスクリプト集となります。  

## 使い方

各スクリプトの使い方を記載します。

### initialize_live_debian.sh

 `dd` 等によるディスクイメージのコピー作成の際やiso起動からディスクをマウントしてメンテナンスを行いたい場合に使用します。  
このスクリプトでIPアドレス等を対象VPSのもの・SSH公開鍵配布URLを個人のものに変更してrootで実行することで、  
「OS再インストール」機能で起動したDebianLiveCDの環境にSSHログインできる環境が整います。

前回使用した際は `debian-live-11.3.0-amd64-standard.iso` による環境でした。

1. DebianLiveCD(standerd)をさくらのVPSで起動します
2. スクリプト冒頭の `### Network configuration` の 部分を手動で打鍵します(ネットワークによるスクリプト取得が可能になる前なので)
3. wget/curl で `https://raw.githubusercontent.com/y-komatsugawa-598/sakura-vps-tools/master/initialize_live_debian.sh` (このスクリプト)をダウンロードします
4. ダウンロードしたスクリプトの `{ description }` の部分を自身の環境に合わせて書き換えrootのシェルで実行します
5. スクリプトで設定した公開鍵でログイン可能になっているはずなのでSSHログインしてメンテナンス作業を行います
6. `apt` でのパッケージインストールも可能です





