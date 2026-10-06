<!-- ELUCENIA technical documentation · conversao-de-acuidade-visual · es · no clinical/professional/rights approval -->

# Conversión de agudeza visual

[condiciones, fuentes y permisos](https://elucenia.org/es/herramientas/conversao-de-acuidade-visual)

## Cómo usar

Utilice la herramienta en el portal o abra index.html mediante un servidor HTTP local. Seleccione el idioma, complete los campos y calcule.

## Entradas y unidades

### Notación introducida

`modo`

- `s20` — Snellen 20/x (pies)
- `s6` — Snellen 6/x (metros)
- `dec` — Decimal
- `log` — logMAR

### Valor (Snellen: solo el denominador)

`valor`

intervalo: -0,4–2000

## Edición del método

Conversión Snellen/decimal/logMAR; ETDRS 1982 0,02 por letra; convenciones Holladay 2004

## Fórmula documentada

Decimal = numerador ÷ denominador de Snellen (20/40 = 0,5). logMAR = −log10(decimal) = log10(MAR), donde MAR es el mínimo ángulo de resolución en minutos de arco. Cada línea ETDRS vale 0,1 logMAR (5 letras de 0,02).

## Límites y población

La conversión exige una fracción de Snellen positiva y conserva la medición original; no realiza un examen nuevo. Compare resultados con distancia, ojo, corrección óptica y tabla documentados. La progresión de 0,1 logMAR por línea y 0,02 por letra corresponde a la estructura ETDRS, no a cualquier tabla. Holladay 2004 recomienda calcular medias en logMAR, no la media aritmética de las fracciones de Snellen. Contar dedos y el movimiento de manos dependen de la distancia y no deben recibir equivalencias decimales fijas mediante esta conversión.

## Referencias

- [Holladay JT. Visual acuity measurements. J Cataract Refract Surg, 2004.](https://doi.org/10.1016/j.jcrs.2004.01.014)

- [Ferris FL et al. New visual acuity charts for clinical research. Am J Ophthalmol, 1982.](https://doi.org/10.1016/0002-9394(82)90197-0)

- [Organização Mundial da Saúde. Blindness and vision impairment (fact sheet).](https://www.who.int/news-room/fact-sheets/detail/blindness-and-visual-impairment)

- [Holladay2004,JCRS30:287–290](https://www.hicsoap.com/__static/03b5dccbd2b603d4d234479004ca5de4/097-visual-acuity-measurements-jcrs-2004-_in-3426.pdf?dl=1)

## Reproducir las pruebas técnicas

Ejecute node test.cjs en el directorio raíz de este repositorio para repetir los casos sintéticos registrados. Se conservan las entradas, los resultados esperados y las tolerancias originales. Las pruebas técnicas no constituyen validación clínica.

```sh
node test.cjs
```

tool.json contiene las fuentes, la edición y el alcance de la revisión. examples.json conserva las entradas y los resultados esperados de los casos sintéticos; results.json registra los resultados obtenidos.

[Ficha y referencias](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referencia](../examples.json) · [results.json](../results.json)

## Revisión y condiciones de uso

No se ha realizado una revisión clínica independiente.

Esta interfaz es una traducción de elaboración propia, no una edición oficial o certificada. No se han realizado la revisión clínica independiente, la revisión lingüística profesional ni la autorización de derechos de los instrumentos.

Resultado de la fórmula o clasificación. La interpretación, la conducta y la aplicabilidad dependen de la evaluación profesional y de la fuente seleccionada.

## Licencia y atribución

Apache-2.0 se aplica únicamente al código de ELUCENIA. Los derechos de los instrumentos, publicaciones, traducciones y datos permanecen en manos de sus respectivos titulares. Conserve LICENSE y NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Resultados documentados

La información siguiente conserva las salidas del método para ejemplos sintéticos. No constituye una validación clínica independiente.

### 1

Sin deficiencia visual (6/12 o mejor), si corresponde al mejor ojo

| Detalles del resultado | |
| --- | --- |
| Decimal | 0,50 |
| Snellen (pies) | 20/40 |
| Snellen (metros) | 6/12,0 |


### 2

Deficiencia visual moderada (peor que 6/18 hasta 6/60), si corresponde al mejor ojo

| Detalles del resultado | |
| --- | --- |
| Decimal | 0,10 |
| Snellen (pies) | 20/200 |
| Snellen (metros) | 6/60,0 |


### 3

Sin deficiencia visual (6/12 o mejor), si corresponde al mejor ojo

| Detalles del resultado | |
| --- | --- |
| Decimal | 1,00 |
| Snellen (pies) | 20/20 |
| Snellen (metros) | 6/6,0 |


### 4

Ceguera (peor que 3/60), si corresponde al mejor ojo

| Detalles del resultado | |
| --- | --- |
| Decimal | 0,04 |
| Snellen (pies) | 20/500 |
| Snellen (metros) | 6/150,0 |

