<!-- ELUCENIA technical documentation · conversao-de-acuidade-visual · pt-BR · no clinical/professional/rights approval -->

# Conversão de acuidade visual

[condições, fontes e permissões](https://elucenia.org/pt-br/ferramentas/conversao-de-acuidade-visual)

## Como usar

Use a ferramenta no portal ou abra index.html em um servidor HTTP local. Selecione o idioma, preencha os campos e calcule.

## Entradas e unidades

### Notação informada

`modo`

- `s20` — Snellen 20/x (pés)
- `s6` — Snellen 6/x (metros)
- `dec` — Decimal
- `log` — logMAR

### Valor (em Snellen, só o denominador)

`valor`

intervalo: -0,4–2000

## Edição do método

Conversão Snellen/decimal/log MAR; ETDRS 1982 0,02 porletra; Holladay 2004 convenções

## Fórmula documentada

Decimal = numerador ÷ denominador do Snellen (20/40 = 0,5). logMAR = −log10(decimal) = log10(MAR), em que MAR é o mínimo ângulo de resolução em minutos de arco. Cada linha da tabela ETDRS vale 0,1 logMAR (5 letras de 0,02).

## Limites e população

A conversão exige uma fração de Snellen positiva e preserva a medida original; não realiza um novo exame. Compare resultados com distância, olho, correção óptica e tabela documentados. A progressão de 0,1 logMAR por linha e 0,02 por letra corresponde à estrutura ETDRS, não a qualquer tabela. Holladay 2004 orienta calcular médias em logMAR, não pela média aritmética das frações de Snellen. Contar dedos e movimento de mãos dependem da distância e não devem receber equivalências decimais fixas por esta conversão.

## Referências

- [Holladay JT. Visual acuity measurements. J Cataract Refract Surg, 2004.](https://doi.org/10.1016/j.jcrs.2004.01.014)

- [Ferris FL et al. New visual acuity charts for clinical research. Am J Ophthalmol, 1982.](https://doi.org/10.1016/0002-9394(82)90197-0)

- [Organização Mundial da Saúde. Blindness and vision impairment (fact sheet).](https://www.who.int/news-room/fact-sheets/detail/blindness-and-visual-impairment)

- [Holladay2004,JCRS30:287–290](https://www.hicsoap.com/__static/03b5dccbd2b603d4d234479004ca5de4/097-visual-acuity-measurements-jcrs-2004-_in-3426.pdf?dl=1)

## Reproduzir os testes técnicos

Execute node test.cjs na pasta raiz deste repositório para repetir os casos sintéticos registrados. As entradas, expectativas e tolerâncias originais são preservadas. Testes técnicos não constituem validação clínica.

```sh
node test.cjs
```

tool.json contém fontes, edição e escopo de revisão. examples.json conserva as entradas e expectativas sintéticas; results.json registra os resultados obtidos.

[Ficha e referências](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referência](../examples.json) · [results.json](../results.json)

## Revisão e condições de uso

Revisão clínica independente não realizada.

Esta interface é uma tradução autoral, não uma edição oficial ou certificada. Revisão clínica independente, revisão linguística profissional e autorização de direitos de instrumentos não foram realizadas.

Resultado da fórmula ou classificação. Interpretação, conduta e aplicabilidade dependem da avaliação profissional e da fonte selecionada.

## Licença e atribuição

Apache-2.0 aplica-se somente ao código da ELUCENIA. Os instrumentos, publicações, traduções e dados mantêm os direitos dos respectivos titulares. Preserve LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
