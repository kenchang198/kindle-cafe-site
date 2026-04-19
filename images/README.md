# images

カフェサイトで使用する画像アセットの一覧。現在は [placehold.co](https://placehold.co/) のプレースホルダーを使用しており、このフォルダに下記ファイル名で実画像を配置し、HTML/CSS の URL を書き換えることで差し替えが完了する。

## 必要なアセット一覧

| # | ファイル名 | 用途 | 推奨サイズ | 形式 | 代替テキスト(alt) |
|---:|---|---|---|---|---|
| 1 | `hero.jpg` | ヒーロー背景（トップ） | 1600 × 900 以上 | JPG | （背景画像のため alt 不要） |
| 2 | `about.jpg` | お店紹介セクション（トップ） | 800 × 600 以上 | JPG | 店内の様子 |
| 3 | `featured-coffee.jpg` | おすすめ1 ハンドドリップ ブレンド | 600 × 450 | JPG | ハンドドリップブレンド |
| 4 | `featured-quiche.jpg` | おすすめ2 自家製キッシュ&サラダ | 600 × 450 | JPG | 自家製キッシュとサラダ |
| 5 | `featured-cheesecake.jpg` | おすすめ3 ベイクドチーズケーキ | 600 × 450 | JPG | ベイクドチーズケーキ |

※ アスペクト比はヒーロー・おすすめが 16:9 / 4:3、About が 4:3 相当。リサイズ時は中心寄りでトリミングすると破綻しにくい。

## 差し替え手順

### 1. 画像素材の入手

フリー素材サイト（Unsplash／Pexels／pixabay など）から **商用利用可かつクレジット表示不要** のものを選ぶ。雰囲気は「木の温もり・間接照明・落ち着いたトーン」を目安に、カフェのカラーパレット（チョコレートブラウン／キャラメル／クリーム）と調和するものを採用する。

### 2. リサイズ・書き出し

上表の推奨サイズに合わせて、トリミング＆書き出し。JPG 品質は 80〜85% 程度、1ファイル 200KB 以下を目安にするとページ表示が軽い。

### 3. このフォルダに配置

```
images/
├── README.md         ← 本ファイル
├── hero.jpg
├── about.jpg
├── featured-coffee.jpg
├── featured-quiche.jpg
└── featured-cheesecake.jpg
```

### 4. HTML/CSS の URL を書き換える

#### `css/style.css`（`.hero` セレクタ）

```css
/* 変更前 */
background: url("https://placehold.co/1600x900/6B4F3B/FAF5EF?text=Hero+Photo") center / cover no-repeat;

/* 変更後 */
background: url("../images/hero.jpg") center / cover no-repeat;
```

#### `index.html`

| 変更前 `src` | 変更後 `src` |
|---|---|
| `https://placehold.co/800x600/E8C07D/2E2720?text=About+Photo` | `images/about.jpg` |
| `https://placehold.co/600x450/6B4F3B/FAF5EF?text=Hand+Drip` | `images/featured-coffee.jpg` |
| `https://placehold.co/600x450/E8C07D/2E2720?text=Quiche` | `images/featured-quiche.jpg` |
| `https://placehold.co/600x450/2E2720/FAF5EF?text=Cheesecake` | `images/featured-cheesecake.jpg` |

## 将来的なオプション（現時点では未使用）

必要に応じて、メニューページに品ごとのサムネイルを追加する場合：

| ファイル名候補 | 用途 | 推奨サイズ |
|---|---|---|
| `menu-coffee-*.jpg` | コーヒー各品の写真 | 400 × 300 |
| `menu-meal-*.jpg` | 軽食各品の写真 | 400 × 300 |
| `menu-sweets-*.jpg` | スイーツ各品の写真 | 400 × 300 |

追加する場合は `menu.html` のレイアウト（`.menu-item` と `.menu-list`）も併せて調整する。

## 素材の出典メモ（任意）

クレジット不要の素材のみを採用するため本 README にも出典は記載しない。ただし運用上、差し替え時に「どのサイトから」「どの画像を」使ったかを手元メモとして残しておくと、後日の差し替え・同系統の画像選定がスムーズになる。
