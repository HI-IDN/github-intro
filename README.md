# Git og GitHub fyrir byrjendur

Þetta repo er ætlað til kennslu í grunnatriðum Git og GitHub.

## GitBook glósur

Glósur um GitHub skrifað í _markdown_ eru geymdar í möppunni `GitBook` og má skoða á eftirfarandi
slóð: 

[GitHub glósur á GitBook](https://tungufoss.gitbook.io/github/)

## Notkun á Git submodules

Þetta repo sýnir einnig hvernig hægt er að nota `git submodule` fyrir önnur repo.
Dæmi:

- [tungufoss/hi-LaTeX-slides](https://github.com/tungufoss/hi-LaTeX-slides)

## Uppsetning

Til að klóna þetta repo þá er það gert með:

```sh 
git clone git@github.com:HI-IDN/github-intro.git 
```

> **Athugið**, það er betra að velja SSH en HTTPS til að klóna repo-ið ef þú ætlar að *push'a*
> breytingum aftur á GitHub. Annars dugar HTTPS vel (þ.e.
`https://github.com/HI-IDN/github-intro.git`)

Þar sem það eru *submodules* í þessu repo þá þarf að keyra eftirfarandi skipun til að sækja þau:

```sh
git submodule update --init --recursive
```

Ef þú vilt klóna repo-ið og submodules á sama tíma, þá dugar ein skipun:

```sh
git clone --recurse-submodules git@github.com:HI-IDN/github-intro.git
```

## Overleaf Sync

Til að tengja þetta repo við Overleaf og vinna með LaTeX-glærurnar beint:

1. Farðu í [Overleaf](https://www.overleaf.com/)
2. Veldu "New Project" > "Import from GitHub".
3. Tengdu Overleaf við GitHub og veldu þetta repo.
4. Gerðu breytingar í Overleaf og pushaðu þeim aftur í GitHub með "Recompile & Push".
