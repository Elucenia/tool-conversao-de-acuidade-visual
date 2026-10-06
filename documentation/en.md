<!-- ELUCENIA technical documentation · conversao-de-acuidade-visual · en · no clinical/professional/rights approval -->

# Visual acuity conversion

[conditions, sources and permissions](https://elucenia.org/en/tools/conversao-de-acuidade-visual)

## How to use

Use the tool in the portal or open index.html through a local HTTP server. Select the language, complete the fields and calculate.

## Inputs and units

### Entered notation

`modo`

- `s20` — Snellen 20/x (feet)
- `s6` — Snellen 6/x (meters)
- `dec` — Decimal
- `log` — logMAR

### Value (Snellen: denominator only)

`valor`

range: -0.4–2000

## Method edition

Snellen/decimal/logMAR conversion; ETDRS 1982 0.02 per letter; Holladay 2004 conventions

## Documented formula

Decimal = Snellen numerator ÷ denominator (20/40 = 0.5). logMAR = −log10(decimal) = log10(MAR), where MAR is the minimum angle of resolution in arcminutes. Each ETDRS chart line is 0.1 logMAR (5 letters of 0.02).

## Limits and population

Conversion requires a positive Snellen fraction and preserves the original measurement; it does not perform a new examination. Compare results with testing distance, eye, optical correction and chart documented. The progression of 0.1 logMAR per line and 0.02 per letter corresponds to the ETDRS structure, not every chart. Holladay 2004 recommends averaging in logMAR, not taking the arithmetic mean of Snellen fractions. Counting fingers and hand movements depend on distance and must not be assigned fixed decimal equivalents through this conversion.

## References

- [Holladay JT. Visual acuity measurements. J Cataract Refract Surg, 2004.](https://doi.org/10.1016/j.jcrs.2004.01.014)

- [Ferris FL et al. New visual acuity charts for clinical research. Am J Ophthalmol, 1982.](https://doi.org/10.1016/0002-9394(82)90197-0)

- [Organização Mundial da Saúde. Blindness and vision impairment (fact sheet).](https://www.who.int/news-room/fact-sheets/detail/blindness-and-visual-impairment)

- [Holladay2004,JCRS30:287–290](https://www.hicsoap.com/__static/03b5dccbd2b603d4d234479004ca5de4/097-visual-acuity-measurements-jcrs-2004-_in-3426.pdf?dl=1)

## Reproduce the technical tests

Run node test.cjs in the root directory of this repository to repeat the recorded synthetic cases. Original inputs, expectations and tolerances are preserved. Technical tests do not constitute clinical validation.

```sh
node test.cjs
```

tool.json contains sources, edition and review scope. examples.json retains synthetic inputs and expectations; results.json records the obtained results.

[Record and references](../tool.json) · [JavaScript code](../calculator.js) · [Reference cases](../examples.json) · [results.json](../results.json)

## Review and conditions of use

Independent clinical review has not been performed.

This interface is an authorial translation, not an official or certified edition. Independent clinical review, professional language review and instrument rights clearance have not been performed.

Formula or classification result. Interpretation, care and applicability depend on professional assessment and the selected source.

## License and attribution

Apache-2.0 applies only to ELUCENIA code. Rights to instruments, publications, translations and data remain with their respective holders. Preserve LICENSE and NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Documented results

The information below preserves the method outputs for synthetic examples. It does not constitute independent clinical validation.

### 1

No visual impairment (6/12 or better), if for the better eye

| Result details | |
| --- | --- |
| Decimal | 0.50 |
| Snellen (feet) | 20/40 |
| Snellen (meters) | 6/12.0 |


### 2

Moderate visual impairment (worse than 6/18 up to 6/60), if for the better eye

| Result details | |
| --- | --- |
| Decimal | 0.10 |
| Snellen (feet) | 20/200 |
| Snellen (meters) | 6/60.0 |


### 3

No visual impairment (6/12 or better), if for the better eye

| Result details | |
| --- | --- |
| Decimal | 1.00 |
| Snellen (feet) | 20/20 |
| Snellen (meters) | 6/6.0 |


### 4

Blindness (worse than 3/60), if for the better eye

| Result details | |
| --- | --- |
| Decimal | 0.04 |
| Snellen (feet) | 20/500 |
| Snellen (meters) | 6/150.0 |

