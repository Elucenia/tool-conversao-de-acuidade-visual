<!-- ELUCENIA technical documentation · conversao-de-acuidade-visual · zh · no clinical/professional/rights approval -->

# 视力换算

[条件、来源与许可](https://elucenia.org/zh/tools/conversao-de-acuidade-visual)

## 使用方法

在门户中使用工具，或通过本地 HTTP 服务器打开 index.html。选择语言，填写各字段，然后计算。

## 输入与单位

### 输入的表示法

`modo`

- `s20` — Snellen 20/x（英尺）
- `s6` — Snellen 6/x（米）
- `dec` — 小数
- `log` — logMAR

### 数值（Snellen 格式只填分母）

`valor`

范围: -0.4–2000

## 方法版本

Snellen/小数/logMAR转换；ETDRS 1982每字母0.02；Holladay 2004约定

## 已记录的公式

小数视力 = Snellen分子÷分母 (20/40 = 0.5). logMAR = −log10(小数视力) = log10(MAR), MAR为以角分计的最小分辨角。ETDRS视力表每行对应0.1 logMAR（5个字母，每字母0.02）。

## 限制与适用人群

转换要求 Snellen 分数为正，并保留原始测量结果；它不进行新的检查。比较结果时应记录检查距离、眼别、光学矫正和视力表。每行 0.1 logMAR、每字母 0.02 的递进对应 ETDRS 结构，而非任意视力表。Holladay 2004 建议在 logMAR 中计算均值，不应取 Snellen 分数的算术平均值。数指和手动视力依赖检查距离，不应通过此转换赋予固定的小数等价值。

## 参考文献

- [Holladay JT. Visual acuity measurements. J Cataract Refract Surg, 2004.](https://doi.org/10.1016/j.jcrs.2004.01.014)

- [Ferris FL et al. New visual acuity charts for clinical research. Am J Ophthalmol, 1982.](https://doi.org/10.1016/0002-9394(82)90197-0)

- [Organização Mundial da Saúde. Blindness and vision impairment (fact sheet).](https://www.who.int/news-room/fact-sheets/detail/blindness-and-visual-impairment)

- [Holladay2004,JCRS30:287–290](https://www.hicsoap.com/__static/03b5dccbd2b603d4d234479004ca5de4/097-visual-acuity-measurements-jcrs-2004-_in-3426.pdf?dl=1)

## 复现技术测试

在此仓库的根目录中运行 node test.cjs，以重复已记录的合成案例。原始输入、预期结果和容差保持不变。技术测试不构成临床验证。

```sh
node test.cjs
```

tool.json 包含来源、版本和审查范围。examples.json 保留合成输入与预期结果；results.json 记录实际得到的结果。

[记录与参考文献](../tool.json) · [JavaScript代码](../calculator.js) · [参考案例](../examples.json) · [results.json](../results.json)

## 审查与使用条件

尚未开展独立临床审查。

此界面为自主编写的翻译，并非官方或认证版本。尚未完成独立临床审查、专业语言审查或工具权利授权。

公式或分类结果。解释、处理及适用性须结合专业评估和所选来源。

## 许可与署名

Apache-2.0 仅适用于 ELUCENIA 代码。工具、出版物、翻译和数据的权利仍归各自权利人所有。请保留 LICENSE 和 NOTICE。

ELUCENIA · Felipe Guedes · Copyright © 2026
