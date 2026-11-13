# DESIGN_REPORT — Uzmera 紹介サイト（branch: fable/site-design）

## 変えたこと（index.html / styles.css のみ。ビルドツールなし）
- ヒーロー：見出し「録って、重ねて、比べる。」が PC でも「比べ／る。」と割れていたのを、2行に収まる組みに修正。直下に機能チップ（録音・メトロノーム・チューナー・楽譜読み取り）を置き、ファーストビューで「何のアプリか」が分かるように。「iPhone & iPad／音楽を練習するすべての人へ」は CTA の下に独立させた。
- CTA：「App Store 公開準備中」をリンクではない状態バッジ（点滅するドット付き）として「Uzmeraを知る」ボタンの隣に配置。末尾セクションにもアプリアイコン付きの公開準備カードを追加。
- スタンプと SCROLL TO EXPLORE がボタンに重なっていたのを解消（スタンプは舞台の角へ）。
- 舞台：毬・花びら・雲に CSS アニメーション。機能カードはホバーで波形や音符が動く。
- セクション間：クリーム色の区画の下端をドットの噛み合わせにし、末尾セクション上端にヒーローと同じ点線を置いて流れをつなげた。左の空白が大きかった「01 — THE IDEA」の列幅を詰めた。
- 文字：8px の極小ラベルを 9〜10px に、本文を 13→14〜16px に。和文フォントスタックと禁則を整備。
- スクロール出現：インライン script（IntersectionObserver、ライブラリなし）。JS なしでも全表示。prefers-reduced-motion では全モーション停止。
- フッター：公式サイトと同じ「Made independently in Japan.」＋蛍光グリーンの菱形の印を追加し、同じスタジオのサイトだと分かるように。Mika Spark Studio へのリンクは維持。
- styles.css は1行に圧縮されていたものを読める形に整形。

## 不変条件チェック
- href 一覧の変更前後 diff（#about / #features / #main / #top / https://mikaspark.com/）：
```
差分なし（5行すべて一致）
```
- 追加・削除したファイル：DESIGN_REPORT.md の追加のみ。assets/ 未変更。新規画像なし。Webフォント追加なし（既存の DotGothic16 のみ）。privacy / terms / support は未作成。push なし。作業開始時に未コミット変更なし。

## 追加した文言（全件。事実は依頼文の記載に基づく）
1. 機能チップ：「録音」「メトロノーム」「チューナー」「楽譜読み取り」
2. バッジ：「App Store 公開準備中」
3. 公開準備カード：「App Store 公開準備中」「Uzmera iPhone & iPad」「App Storeで近日公開予定です。」
4. フッター：「Made independently in Japan.」
既存文言の書き換えはなし。

## 表示確認
1280 / 375 / 320 で撮影、横スクロールなし。保存先 ~/fable-design-shots/uzmera-*.png。ヘッドレス Chromium のみで確認（Safari / 実機は未確認）。

## 残した課題・次に効くこと
- DotGothic16-Regular.ttf が約 2MB。使用文字だけの woff2 サブセットにすると大幅に軽くなる（font-display: swap なので表示は止まらないが、読み込み後に字形が切り替わる）。
- uzmera-app-icon.png も大きい。表示サイズに合わせた縮小版が有効。
- 不足素材：アプリ実画面のスクリーンショット。機能カードが実画面になると説得力が最も上がる。
- App Store 公開後はバッジと公開準備カードをストアリンクに差し替える。
