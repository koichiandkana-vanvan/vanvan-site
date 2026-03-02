# ばんばんサイト — 開発ガイド

## プロジェクト概要
黒トイプードル「ばんばん」の個人サイト。
家族・友人への共有と、SNSでの広い公開の両方を想定。

## ばんばんプロフィール
| 項目 | 内容 |
|---|---|
| 名前 | ばんばん |
| 犬種 | トイプードル |
| 毛色 | 黒（Noir） |
| 性別 | オス |
| 誕生日 | 2025年2月28日 |
| 特技 | おすわり |

## デザイン思想
- **テーマ**：高級感・エレガント・"Timeless Elegance"
- **配色**：黒背景（`#0a0a0a`）+ ゴールド（`#d4af37`）
- **フォント**：Cormorant Garamond（見出し）、Montserrat（本文）
- **演出**：カスタムカーソル（PCのみ）、スクロール進捗バー、フェードインアニメーション、BGM

## ファイル構成
```
vanvan-site/
├── index.html        # メインファイル（HTML/CSS/JS すべて単一ファイル）
├── images/
│   ├── 01〜06.jpg    # プロフィール写真（ギャラリー用）
│   ├── favicon.png   # 06.jpg の顔部分をクロップ（180×180px）
│   └── munku.MOV     # 背景動画
└── audio/
    └── bgm.mp3       # BGM（Fluffy Shadow Ban Ban）
```

## 技術仕様
- **構成**：HTML / CSS / Vanilla JS（単一ファイル、フレームワーク不使用）
- **背景動画**：`position: fixed` で全セクション共通。フェードイン 3s
- **ギャラリー**：メイン画像 + 横スクロールサムネイル。画像切り替えにフェード
- **BGM**：`touchend` / `click` で初回再生（iOS自動再生制限対応）、右下ボタンでON/OFF
- **スマホ対応**：ハンバーガーメニュー、カーソル非表示（`pointer: coarse`）

## GitHub / 公開情報
- **リポジトリ**：`koichiandkana-vanvan/vanvan-site`
- **公開URL**：https://koichiandkana-vanvan.github.io/vanvan-site/
- **ブランチ**：`master`（main ブランチ）

## 今後の予定
- [ ] Instagram 連携（写真・リールの埋め込みまたはリンク）
- [ ] ばんばん愛用 Goods 紹介ページ（アフィリエイトリンク掲載）
- [ ] Movies セクションへの動画追加

## 開発ルール
- HTML/CSS/JS はすべて `index.html` に一本化する（ファイル分割しない）
- 作業後は必ず `git push origin master` で GitHub Pages に反映する
- デザインの雰囲気（黒×ゴールド、高級感）は維持する
