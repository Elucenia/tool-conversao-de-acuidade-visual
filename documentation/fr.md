<!-- ELUCENIA technical documentation · conversao-de-acuidade-visual · fr · no clinical/professional/rights approval -->

# Conversion de l’acuité visuelle

[conditions, sources et autorisations](https://elucenia.org/fr/outils/conversao-de-acuidade-visual)

## Mode d’emploi

Utilisez l’outil sur le portail ou ouvrez index.html via un serveur HTTP local. Sélectionnez la langue, remplissez les champs et lancez le calcul.

## Données d’entrée et unités

### Notation saisie

`modo`

- `s20` — Snellen 20/x (pieds)
- `s6` — Snellen 6/x (mètres)
- `dec` — Décimal
- `log` — logMAR

### Valeur (Snellen : dénominateur uniquement)

`valor`

intervalle: -0,4–2000

## Édition de la méthode

Conversion Snellen/décimal/logMAR ; ETDRS 1982 0,02 par lettre ; conventions Holladay 2004

## Formule documentée

Décimal = numérateur ÷ dénominateur de Snellen (20/40 = 0,5). logMAR = −log10(décimal) = log10(MAR), où MAR est l’angle minimal de résolution en minutes d’arc. Chaque ligne ETDRS vaut 0,1 logMAR (5 lettres de 0,02).

## Limites et population

La conversion exige une fraction de Snellen positive et conserve la mesure d’origine ; elle ne réalise pas un nouvel examen. Comparez les résultats en documentant la distance, l’œil, la correction optique et le tableau utilisé. La progression de 0,1 logMAR par ligne et de 0,02 par lettre correspond à la structure ETDRS, pas à tous les tableaux. Holladay 2004 recommande de calculer les moyennes en logMAR, et non la moyenne arithmétique des fractions de Snellen. Le comptage des doigts et les mouvements de la main dépendent de la distance et ne doivent pas recevoir d’équivalents décimaux fixes par cette conversion.

## Références

- [Holladay JT. Visual acuity measurements. J Cataract Refract Surg, 2004.](https://doi.org/10.1016/j.jcrs.2004.01.014)

- [Ferris FL et al. New visual acuity charts for clinical research. Am J Ophthalmol, 1982.](https://doi.org/10.1016/0002-9394(82)90197-0)

- [Organização Mundial da Saúde. Blindness and vision impairment (fact sheet).](https://www.who.int/news-room/fact-sheets/detail/blindness-and-visual-impairment)

- [Holladay2004,JCRS30:287–290](https://www.hicsoap.com/__static/03b5dccbd2b603d4d234479004ca5de4/097-visual-acuity-measurements-jcrs-2004-_in-3426.pdf?dl=1)

## Reproduire les tests techniques

Exécutez node test.cjs dans le répertoire racine de ce dépôt pour reproduire les cas synthétiques enregistrés. Les données d’entrée, les résultats attendus et les tolérances d’origine sont conservés. Les tests techniques ne constituent pas une validation clinique.

```sh
node test.cjs
```

tool.json contient les sources, l’édition et le périmètre de la revue. examples.json conserve les données d’entrée et les résultats attendus des cas synthétiques ; results.json consigne les résultats obtenus.

[Fiche et références](../tool.json) · [Code JavaScript](../calculator.js) · [Cas de référence](../examples.json) · [results.json](../results.json)

## Revue et conditions d’utilisation

Aucune révision clinique indépendante n’a été effectuée.

Cette interface est une traduction réalisée par nos soins, et non une édition officielle ou certifiée. La revue clinique indépendante, la révision linguistique professionnelle et l’autorisation des droits sur les instruments n’ont pas été réalisées.

Résultat de la formule ou de la classification. L’interprétation, la conduite et l’applicabilité dépendent de l’évaluation professionnelle et de la source sélectionnée.

## Licence et attribution

Apache-2.0 s’applique uniquement au code d’ELUCENIA. Les droits sur les instruments, publications, traductions et données restent ceux de leurs titulaires respectifs. Conservez LICENSE et NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
