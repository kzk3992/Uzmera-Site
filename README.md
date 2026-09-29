# Uzmera website

Uzmera のピクセルアート中心の紹介サイトです。HTML/CSS と静的画像のみで構成され、ビルド手順は不要です。

## ローカルで確認

`index.html` をブラウザで開きます。`python3 -m http.server 8000` を実行して `http://localhost:8000` を開いても確認できます。

## サブドメインで公開

1. このフォルダの内容をホスティング先へデプロイします。
2. DNS で `uzmera.mikaspark.com` をホスティング先へ向けます。
3. ホスティング先にカスタムドメイン `uzmera.mikaspark.com` を設定し、HTTPS を有効にします。

`CNAME` は GitHub Pages など CNAME ファイルでドメインを設定するホスト向けです。Cloudflare Pages ではダッシュボードの Custom domains に同じサブドメインを登録してください。

## アセット

`assets/` 内の DotGothic16 フォントとキャラクター画像は Uzmera iOS アプリのアセットを使用しています。フォントのライセンスは `assets/DotGothic16-OFL.txt` を参照してください。
