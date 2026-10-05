<!-- ELUCENIA technical documentation · conversao-de-acuidade-visual · ja · no clinical/professional/rights approval -->

# 視力の換算

[条件・出典・許諾](https://elucenia.org/ja/tools/conversao-de-acuidade-visual)

## 使い方

ポータルでツールを使用するか、ローカルHTTPサーバー経由でindex.htmlを開いてください。言語を選択し、項目を入力して計算してください。

## 入力項目と単位

### 入力値の表記方式

`modo`

- `s20` — Snellen 20/x（フィート）
- `s6` — Snellen 6/x（メートル）
- `dec` — 小数
- `log` — logMAR

### 数値（Snellenでは分母のみ）

`valor`

範囲: -0.4–2000

## 方法の版

Snellen/小数/logMAR換算；ETDRS 1982 1文字0.02；Holladay 2004規約

## 記載された計算式

小数視力 = Snellen分子÷分母 (20/40 = 0.5). logMAR = −log10(小数視力) = log10(MAR), MARは分角単位の最小分離角です。ETDRS表の1行は0.1 logMAR（5文字、各0.02）に相当します。

## 限界・対象集団

変換には正の Snellen 分数が必要で、元の測定値を保ちます。新しい検査を行うものではありません。検査距離、対象眼、光学的矯正、視力表を記録して結果を比較してください。1 行あたり 0.1 logMAR、1 文字あたり 0.02 という段階は ETDRS の構造に対応し、すべての視力表に当てはまるわけではありません。Holladay 2004 は Snellen 分数の算術平均ではなく、logMAR での平均を推奨します。指数弁と手動弁は距離に依存し、この変換で固定した小数値を割り当ててはいけません。

## 参考文献

- [Holladay JT. Visual acuity measurements. J Cataract Refract Surg, 2004.](https://doi.org/10.1016/j.jcrs.2004.01.014)

- [Ferris FL et al. New visual acuity charts for clinical research. Am J Ophthalmol, 1982.](https://doi.org/10.1016/0002-9394(82)90197-0)

- [Organização Mundial da Saúde. Blindness and vision impairment (fact sheet).](https://www.who.int/news-room/fact-sheets/detail/blindness-and-visual-impairment)

- [Holladay2004,JCRS30:287–290](https://www.hicsoap.com/__static/03b5dccbd2b603d4d234479004ca5de4/097-visual-acuity-measurements-jcrs-2004-_in-3426.pdf?dl=1)

## 技術テストの再現

このリポジトリのルートディレクトリでnode test.cjsを実行すると、記録された合成ケースを再実行できます。元の入力、期待結果、許容誤差は保持されています。技術テストは臨床的検証を意味しません。

```sh
node test.cjs
```

tool.jsonには出典、版、確認範囲が記録されています。examples.jsonには合成入力と期待結果が保持され、results.jsonには実際に得られた結果が記録されています。

[記録・参考文献](../tool.json) · [JavaScriptコード](../calculator.js) · [参照ケース](../examples.json) · [results.json](../results.json)

## 確認状況と使用条件

独立した臨床レビューは実施されていません。

このインターフェースは独自に作成した翻訳であり、公式版や認証済みの版ではありません。独立した臨床レビュー、専門家による言語レビュー、評価尺度等の権利許諾の確認は実施されていません。

式または分類の結果です。解釈、対応、適用可能性は専門家による評価と選択した出典に依存します。

## ライセンスと帰属表示

Apache-2.0はELUCENIAのコードにのみ適用されます。評価尺度等、出版物、翻訳、データの権利は、それぞれの権利者に帰属します。LICENSEとNOTICEを保持してください。

ELUCENIA · Felipe Guedes · Copyright © 2026
