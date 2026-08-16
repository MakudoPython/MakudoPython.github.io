# math/ ディレクトリの構造メモ

久しぶりに戻ってきたときに迷わないためのメモ。新しいページを追加するときは、まずこのファイルを見る。

## フォルダ分けのルール

- `math_1`, `math_2`, `math_a`, `math_b`, `math_c` ... → 高校の課程(数学Ⅰ、数学A など)に対応する内容
- `matrix`, `suken_xxx` のような名前 → 高校の課程に直接対応しない、検定対策やトピック単位のまとまり(例: 数検準1級の行列)

新しい分野を追加するときは、「これは課程ベースか、トピックベースか」をまず決めて、上のどちらの命名規則に沿うか判断する。

## 現在のページ一覧

### math_1 (数学Ⅰ)
- `sine-law.html` / `sine-law-problems.html` — 正弦定理
- `cosine-law.html` / `cosine-law-random.html` — 余弦定理

### matrix (数検準1級・行列)
- `matrix-cayley-hamilton.html` — ケーリー・ハミルトンの定理(定理・証明)
- `matrix-inverse.html` — 逆行列
- `matrix-power.html` — A^nの求め方(次数下げ／べき零行列／回転移動)
- `matrix-scalar-case.html` — a+d, ad−bcを求める問題(スカラー行列の場合分け)
- `matrix-cayley-hamilton-problems.html` — 練習問題+解答

## 新しいページを追加する手順

1. `_template.html` をコピーして、適切なフォルダに置く
2. `<h1>` とタイトル、本文、数式を書き換える
3. 一番下の「数学トップに戻る」リンクは基本そのままでOK(相対パスの階層だけ確認)
4. `math/index.html` の該当セクションに `<li>` でリンクを追加する
5. このREADMEの「現在のページ一覧」にも1行追加しておく(これを忘れると次回また迷う)

## いつかやりたい改善(メモ)

- 各ページに同じ `<style>` を貼り付けているので、`assets/style.css` のような共通CSSファイルに切り出す
- 数式がプレーンテキストなので、KaTeXなどを導入して見やすくする
- ページ数が増えてきたら、index.html の手動更新をやめて自動生成にする
- 練習問題ページは `<details><summary>解答を見る</summary>` で解答を折りたたむ
