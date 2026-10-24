# TakateLAB サイト

TakateLAB の個人サイト（屋号の紹介・アプリ紹介・プライバシーポリシー・お問い合わせ）。
HTML / CSS のみの静的サイトで、GitHub Pages で公開する想定。

## 構成

```
index.html                       トップ（屋号・事業内容・アプリ・お問い合わせ）
about/index.html                 運営者情報
apps/index.html                  アプリ一覧（アプリを増やしたらこことトップに追加）
apps/kotobatown/index.html       ことばタウン紹介
apps/kotobatown/privacy/         ことばタウン プライバシーポリシー（ストアに登録する URL）
privacy/index.html               共通プライバシーポリシー（基本方針）
contact/index.html               お問い合わせ
404.html                         見つからないページ（リンクはルート絶対パス）
assets/css/style.css             共通スタイル（色はトークン、ダークモード対応）
assets/img/                      画像（mark.svg がロゴマーク兼ファビコン）
.nojekyll                        GitHub Pages の Jekyll 処理を無効化
```

- ヘッダー・フッターは各ページに直接書いている。ページを追加・リンクを変えるときは全ページを更新する。
- 新しいアプリは `apps/<アプリ名>/index.html` と `apps/<アプリ名>/privacy/index.html` を作り、アプリ一覧・トップ・共通ポリシーの「アプリごとのプライバシーポリシー」に追加する。
- リンクは相対パス（404.html のみルート絶対パス）。

## 確認方法

```bash
python3 -m http.server 8000
# → http://localhost:8000/
```

## TODO

- [ ] 開業後、運営者情報に所在地（バーチャルオフィス）を追加する
- [ ] ストア公開後、`apps/kotobatown/index.html` のダウンロード欄をストアのリンクに差し替える
- [ ] 独自ドメインを取ったら GitHub Pages に設定する（`CNAME` ファイル）
- [ ] プライバシーポリシーの内容をアプリの実装と照らして最終確認する（制定日も公開日に合わせる）
