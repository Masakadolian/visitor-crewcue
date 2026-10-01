# visitor-crewcue

VisitorAdventure のクルー用カンペ（VRChat の手首メニュー）が読み込む JSON と図面を置く公開リポジトリです。
GitHub Pages（`*.github.io`）は VRChat の信頼済みドメインなので、「信頼できない URL」がオフでも読み込めます。

**このリポジトリは公開です。誰でも読めます。秘密の台本は置かないでください。**

## ファイル
- `crewcue.json` — 役 → 場面 → 本文。形は `{ updated, roles:[{ name, scenes:[{ name, text, image? }] }] }`
- `images/<番号>.png` — 図面。JSON の `image` が番号に対応する。直リンク（リダイレクトなし）、最大 2048×2048、運用は 1024px 以内

## URL
- JSON: https://masakadolian.github.io/visitor-crewcue/crewcue.json
- 図面: https://masakadolian.github.io/visitor-crewcue/images/0.png

## 注意
- 現在の中身はダミーの動作確認用です。
- VRCUrl はワールドに固定で埋め込むので、ファイル名・パスを変えるとワールド側の再アップロードが要ります。内容の差し替えだけなら再アップロードは不要です。
