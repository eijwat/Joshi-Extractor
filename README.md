# 助詞抽出器（Joshi Extractor）

日本語テキストから**助詞・助動詞・句読点**だけを残し、それ以外の文字を全角スペースに置き換えるツールです。

## 背景

助詞だけを抽出した文章をAI（Claude）に渡したところ、助詞の配列パターンだけで夏目漱石の『坊っちゃん』を特定するという驚くべき結果が得られました。この実験の詳細は [GitHub Pages](https://eijwat.github.io/Joshi-Extractor/) で公開しています。

## デモ

GitHub Pages でそのまま動作します。サーバーサイド処理は不要です。

[https://eijwat.github.io/Joshi-Extractor/](https://eijwat.github.io/Joshi-Extractor/)

## 使い方

1. テキストエリアに日本語を入力
2. 「抽出する」ボタンを押す（または Ctrl+Enter）
3. 助詞・句読点だけが残り、他の文字は文字数分の全角スペースに置換されます
4. 「コピー」ボタンで結果をクリップボードにコピー

## 出力の仕様

| 種別 | 扱い |
|------|------|
| 助詞・助動詞 | そのまま残す（複合助詞も含む） |
| 句読点・括弧・記号 | そのまま残す |
| 名詞・動詞・形容詞など | 文字数分の全角スペースに置換 |

## 技術

- [kuromoji.js](https://github.com/takuyaa/kuromoji.js) による形態素解析（ブラウザ完結）
- 辞書は [jsDelivr CDN](https://www.jsdelivr.com/) から動的に読み込み
- 依存フレームワークなし、単一HTMLファイル

## ライセンス

MIT
