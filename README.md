# visitor-crewcue

VisitorAdventure のクルー用カンペ（VRChat の手首メニューの「カンペ」タブ）が読み込む JSON と図面を置く公開リポジトリです。
GitHub Pages（`*.github.io`）は VRChat の信頼済みドメインなので、「信頼できない URL」がオフでも読み込めます。

**このリポジトリは公開です。誰でも読めます。** 台本（探偵・MC・スタッフの進行）をそのまま載せています。ゲストに知られると演出の驚きが減る内容を含みますが、「知られても大きな問題はない」と判断して公開しています（2026-10-03）。本当に伏せたい内容は、ここに置かないでください。

## ファイル
- `crewcue.json` — 役 → 場面 → 本文
- `images/<番号>.png` — 図面。JSON の `image`（0〜7）が番号に対応する。直リンク（リダイレクトなし）、最大 2048×2048、運用は 1024px 以内

## URL
- JSON: https://masakadolian.github.io/visitor-crewcue/crewcue.json
- 図面: https://masakadolian.github.io/visitor-crewcue/images/0.png

## ポスター画像（`posters/`）
ワールドの壁のポスターが読み込む画像。ファイル名が枠に対応する（`L00`〜`L08` = 左の壁の窓、`R00`〜`R08` = 右の壁の窓、`PanelL` `PanelR` = 窓の下のパネル）。
窓は縦長 1448×2048、パネルは横長 2048×956 を目安にする。長辺 2048 以内、JPEG 推奨。
**同じファイル名で上書きすれば URL は変わらない**（反映まで最大10分かかる）。いまは枠の名前を描いた仮の画像。

- 例: https://masakadolian.github.io/visitor-crewcue/posters/L00.jpg
- URL をワールドへ入れる手順は、VisitorAdventure の `docs/design/dropbox-poster-display.md`

## JSON の形

```json
{
  "updated": "2026/10/03（台本 v1.4 より）",
  "updated_en": "2026/10/03 (from script v1.4)",
  "roles": [
    { "name": "探偵", "name_en": "Detective", "scenes": [
      { "name": "依頼", "name_en": "The request",
        "image": 0,
        "text": "…", "text_en": "…" } ] }
  ]
}
```

- `*_en` は英語版。VRChat の言語設定が日本語（`ja`）以外のとき、`name_en` `text_en` `updated_en` があればそれを使い、無い項目は日本語に戻る
- `image` は省略できる。0〜7 の整数
- 上限: 役 6、1 役あたり場面 8、名前 24 文字、本文 3000 文字（超えた分は切り捨て）
- 本文で使えるタグは `<b>` `<i>` `<color=#rrggbb>` だけ。改行は `\n`。それ以外の `<` は全角になる

## 書き方
- **時間は「開演から何分後か」の目安で書く**（例: 開演の7分後ごろ / About 7 min after curtain）。`T+7` のような記号は使わない
- 探索の部分は、特定のワールドに依存しない書き方にする。探索ワールドは次回以降変わりうる

## 更新
- 中身の差し替えは、このリポジトリの `crewcue.json` を直して push するだけ。ワールドの再アップロードは要らない
- **GitHub Pages は応答を最大10分キャッシュします。** 直してすぐ読み込み直しても、古い内容が返ることがあります
- VRCUrl はワールドに固定で埋め込むので、ファイル名・パスを変えるとワールド側の再アップロードが要ります

## 元になっている台本
`Masakadolian/VisitorsQuest-Discord`（非公開）の `SCRIPT-探偵.md` `SCRIPT-MC.md` `SCRIPT-スタッフ.md`（v1.4）。
