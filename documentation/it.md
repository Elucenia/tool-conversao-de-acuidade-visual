<!-- ELUCENIA technical documentation · conversao-de-acuidade-visual · it · no clinical/professional/rights approval -->

# Conversione dell’acuità visiva

[condizioni, fonti e autorizzazioni](https://elucenia.org/it/strumenti/conversao-de-acuidade-visual)

## Come usare

Usi lo strumento nel portale oppure apra index.html tramite un server HTTP locale. Selezioni la lingua, compili i campi ed esegua il calcolo.

## Dati di ingresso e unità

### Notazione inserita

`modo`

- `s20` — Snellen 20/x (piedi)
- `s6` — Snellen 6/x (metri)
- `dec` — Decimale
- `log` — logMAR

### Valore (Snellen: solo il denominatore)

`valor`

intervallo: -0,4–2000

## Edizione del metodo

Conversione Snellen/decimale/logMAR; ETDRS 1982 0,02 per lettera; convenzioni Holladay 2004

## Formula documentata

Decimale = numeratore ÷ denominatore di Snellen (20/40 = 0,5). logMAR = −log10(decimale) = log10(MAR), dove MAR è l’angolo minimo di risoluzione in minuti d’arco. Ogni riga ETDRS vale 0,1 logMAR (5 lettere da 0,02).

## Limiti e popolazione

La conversione richiede una frazione di Snellen positiva e conserva la misura originale; non esegue un nuovo esame. Confrontare risultati con distanza, occhio, correzione ottica e ottotipo documentati. La progressione di 0,1 logMAR per riga e 0,02 per lettera corrisponde alla struttura ETDRS, non a qualsiasi ottotipo. Holladay 2004 raccomanda medie in logMAR, non la media aritmetica delle frazioni di Snellen. Contare le dita e il movimento della mano dipendono dalla distanza e non devono ricevere equivalenti decimali fissi tramite questa conversione.

## Riferimenti

- [Holladay JT. Visual acuity measurements. J Cataract Refract Surg, 2004.](https://doi.org/10.1016/j.jcrs.2004.01.014)

- [Ferris FL et al. New visual acuity charts for clinical research. Am J Ophthalmol, 1982.](https://doi.org/10.1016/0002-9394(82)90197-0)

- [Organização Mundial da Saúde. Blindness and vision impairment (fact sheet).](https://www.who.int/news-room/fact-sheets/detail/blindness-and-visual-impairment)

- [Holladay2004,JCRS30:287–290](https://www.hicsoap.com/__static/03b5dccbd2b603d4d234479004ca5de4/097-visual-acuity-measurements-jcrs-2004-_in-3426.pdf?dl=1)

## Riprodurre i test tecnici

Esegua node test.cjs nella cartella principale di questo repository per ripetere i casi sintetici registrati. Gli input, i risultati attesi e le tolleranze originali sono conservati. I test tecnici non costituiscono validazione clinica.

```sh
node test.cjs
```

tool.json contiene le fonti, l’edizione e l’ambito della revisione. examples.json conserva gli input e i risultati attesi dei casi sintetici; results.json registra i risultati ottenuti.

[Scheda e riferimenti](../tool.json) · [Codice JavaScript](../calculator.js) · [Casi di riferimento](../examples.json) · [results.json](../results.json)

## Revisione e condizioni d’uso

Non è stata effettuata una revisione clinica indipendente.

Questa interfaccia è una traduzione realizzata dagli autori, non un’edizione ufficiale o certificata. Non sono state eseguite la revisione clinica indipendente, la revisione linguistica professionale né la verifica delle autorizzazioni relative ai diritti sugli strumenti.

Risultato della formula o classificazione. Interpretazione, condotta e applicabilità dipendono dalla valutazione professionale e dalla fonte selezionata.

## Licenza e attribuzione

Apache-2.0 si applica solo al codice di ELUCENIA. I diritti su strumenti, pubblicazioni, traduzioni e dati restano ai rispettivi titolari. Conservi LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Risultati documentati

Le informazioni seguenti conservano gli output del metodo per esempi sintetici. Non costituiscono una validazione clinica indipendente.

### 1

Nessuna disabilità visiva (6/12 o migliore), se riferita all’occhio migliore

| Dettagli del risultato | |
| --- | --- |
| Decimale | 0,50 |
| Snellen (piedi) | 20/40 |
| Snellen (metri) | 6/12,0 |


### 2

Disabilità visiva moderata (peggiore di 6/18 fino a 6/60), se riferita all’occhio migliore

| Dettagli del risultato | |
| --- | --- |
| Decimale | 0,10 |
| Snellen (piedi) | 20/200 |
| Snellen (metri) | 6/60,0 |


### 3

Nessuna disabilità visiva (6/12 o migliore), se riferita all’occhio migliore

| Dettagli del risultato | |
| --- | --- |
| Decimale | 1,00 |
| Snellen (piedi) | 20/20 |
| Snellen (metri) | 6/6,0 |


### 4

Cecità (peggiore di 3/60), se riferita all’occhio migliore

| Dettagli del risultato | |
| --- | --- |
| Decimale | 0,04 |
| Snellen (piedi) | 20/500 |
| Snellen (metri) | 6/150,0 |

