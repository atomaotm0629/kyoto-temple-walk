# 京都お寺めぐり（NFC キーホルダー用の案内マップ）

キーホルダーの NFC タグをかざすと開くページ。`index.html`（画面）と `data.js`（お寺・年表・言葉のデータ）の 2 ファイル。

## できること

- 京都の 21 のお寺を地図とリストで案内（地域・世界遺産で絞り込み、現在地から近い順）
- お寺ごとに：創建年・宗派・説明・見どころ・**ゆかりの人物**・**国宝**・アクセス・行き方（Google マップ）
- **📜 歴史**：750 年から 2000 年まで年が進み、お寺が建った順に地図に現れるアニメーション。時代の帯（奈良〜明治以降）と出来事（平安京遷都・応仁の乱など）。スライダーで好きな年へ
- **参拝のはんこ**（スマホの中だけに保存）
- **4 か国語**：日本語・English・中文（简体）・한국어。スマホの言語に自動で合わせ、右上で切り替えられる。`?lang=en` を付けて開くとその言語
- `#kinkakuji` のように末尾に付けて開くと、そのお寺のページがすぐ開く（お寺ごとのタグ用）
- キーホルダーの使い方と、タグを自分の SNS に書き換える手順をページ内に載せている

お寺の id：kiyomizudera, kuramadera, toji, sanzenin, eikando, daigoji, ninnaji, byodoin, sanjusangendo, chionin, kenninji, tofukuji, nanzenji, daitokuji, tenryuji, kinkakuji, ryoanji, ginkakuji, nishihonganji, higashihonganji, kodaiji

## 確認・編集

- ローカル確認：`.claude\launch.json` の `kyoto-temple-map`（ポート 8550）
- お寺を足す・直す：`data.js` の `TEMPLES` に追加（`y` は年表に現れる年）。ない言語の文章は英語 → 日本語で代わりに出る

## 公開について

公開先: **https://atomaotm0629.github.io/kyoto-temple-walk/** （リポジトリ atomaotm0629/kyoto-temple-walk、main を push すると1〜2分で反映）。
NFC タグにはこの URL を書く（お寺ごとなら末尾に `#kinkakuji` など）。
販売する場合の注意：

- 地図は OpenStreetMap のタイルを使っている。アクセスが多くなったら、OSM の利用ルールに合わせて有料・自前のタイル（MapTiler など）に切り替える
- 拝観時間・料金は載せていない（変わるため）。創建年は伝承を含む
- お寺の名前・説明は一般的な事実だけ。お寺の写真やロゴは使っていない（使うなら各お寺の許可が必要）
