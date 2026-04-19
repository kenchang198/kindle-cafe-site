# kindle-cafe-site

書籍『Claude Codeで100倍早く学ぶ HTML & CSS ― AIと一緒に、ゼロからカフェサイトを爆速で作る』の公式サンプルリポジトリ。

## このリポジトリの役割

本書で読者が作成する架空カフェサイトの **完成形プロトタイプ** と、第2章・第3章で用いる **基礎サンプル** を提供する。本書を読み進める際の参照用／学習後のフォーク用として活用できる。

> **書籍ページ**: Kindle 公開後にリンクを追記予定
>
> **書籍原稿リポジトリ（著者管理・非公開）**: [kenchang198/kindle_pub](https://github.com/kenchang198/kindle_pub) ／本書のプロジェクトディレクトリ：`html_learning_claude/`

## 章対応表

| 章 | 内容 | このリポ内の場所 | 動作確認の仕方 |
|---|---|---|---|
| 第1章 | Claude Code 環境構築 | （リポの利用は第2章以降） | — |
| 第2章 | HTMLの基礎 | [`basics/ch02-html/`](basics/ch02-html/) | フォルダ内の `index.html` をブラウザで開く |
| 第3章 | CSSの基礎 | [`basics/ch03-css/`](basics/ch03-css/) | 同上 |
| 第4章 | カフェサイト構築（演習） | リポジトリ直下 | `index.html` をブラウザで開く |
| 第5章 | レスポンシブ対応 | リポジトリ直下（レスポンシブ込み） | DevTools でスマホ表示を確認 |

章ごとのスナップショットはブランチ／タグ `chapter/02`・`chapter/03`・… として参照可能（該当章が完成次第、本表にリンクを追加する）。

## 使い方

### Git で取得する

```
git clone https://github.com/kenchang198/kindle-cafe-site.git
```

### ZIP で取得する

1. このページ右上の緑色の **Code** ボタンをクリック
2. **Download ZIP** を選択
3. 展開したフォルダ内の `index.html` をブラウザで開く

### ブラウザで開く

HTML ファイルをダブルクリックするか、VSCode の Live Server 拡張機能を使うとリアルタイムプレビューができる。

## ライセンス

[MIT License](LICENSE)

画像素材は商用利用可かつクレジット表示不要のもの（Unsplash／Pexels／pixabay 等）を採用している。
