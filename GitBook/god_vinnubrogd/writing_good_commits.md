---
description: >-
  Leiðbeiningar um hvernig á að skrifa skýr og gagnleg Git commit skilaboð.
---

# Hvernig á að skrifa góð Git commit skilaboð

Góð commit skilaboð eru mikilvæg til að auðvelda samstarf og viðhalda skýrri sögu breytinga í Git. Skýr og vel útfærð commit skilaboð hjálpa öðrum (og þér sjálfum í framtíðinni) að skilja breytingarnar sem voru gerðar.

## Grundvallarreglur fyrir commit skilaboð

- **Notaðu skýrt og lýsandi orðalag.**
- **Fylgdu ákveðinni formgerð.**
- **Skrifaðu í nútíð.** („Bætir við virkni...“ frekar en „Bætti við virkni...“)
- **Ekki vera of almennur.** („Lagaði villur“ er ekki gagnlegt, en „Lagaði innskráningarvillu í notendaviðmóti“ er betra.)

## Formgerð commit skilaboða

Dæmi um gott commit skilaboð:
```sh
Bætir við notendaskráningu með tveggja þátta auðkenningu

- Notar Google Authenticator fyrir tveggja þátta auðkenningu
- Bætir við SQL töflu fyrir notendaupplýsingar
- Lagar smávægilegar villur í HTML formi
```

Þetta commit fylgir eftirfarandi reglum:

1. **Fyrsta línan er stutt og skýr (helst undir 50 stöfum).**
2. **Fyrsta línan byrjar á sagnorði í nútíð.**
3. **Ítarleg lýsing (ef þörf krefur) kemur í næstu línum.**

## Hvernig á að skrifa lengri commit lýsingu í Bash?

Ef þú þarft að skrifa ítarleg commit skilaboð er best að nota eftirfarandi skipun:
```sh
git commit
```
Þetta opnar sjálfgefinn textaritil (t.d. `vim` eða `nano`) þar sem þú getur skrifað lengri lýsingu.

- Fyrsta línan ætti að vera **stutt og skýr lýsing á breytingunni**.
- Eftir eina auða línu má bæta við ítarlegri lýsingu.
- Skráin er vistuð og lokað með `:wq` í `vim` eða `CTRL + X`, `Y`, og `Enter` í `nano`.

Ef þú vilt skrifa commit skilaboð án þess að opna ritil geturðu notað:
```sh
git commit -m "Stutt lýsing" -m "Lengri lýsing á breytingunni."
```
Fyrsta `-m` inniheldur fyrirsögn, seinna `-m` inniheldur ítarlegri lýsingu.

## Cross-referencing við Issues í GitHub

Git commit skilaboð geta vísað beint í issues með sérstökum fráteknum orðum:

- **„Fixes #3“** – Lagar issue númer 3 og lokar því.
- **„Closes #2“** – Lokar issue númer 2.
- **„Resolves #5“** – Leysir issue númer 5.

Dæmi um commit með issue-referencing:
```sh
git commit -m "Lagar villu í innskráningu" -m "Fixes #42"
```
Þetta gerir það að verkum að þegar commit-ið er ýtt á GitHub, verður issue #42 sjálfkrafa lokað, 
og hægt er að sjá cross-reference á milli commit og issue í GitHub.

## Skammstöfunarkerfi fyrir commit skilaboð

Sum verkefni nota skammstafanir til að flokka commit skilaboð betur:

- `feat:` Ný virkni
- `fix:` Lagfæring á villu
- `docs:` Uppfærsla á skjölum
- `refactor:` Endurskipulagning á kóða
- `test:` Viðbætur eða breytingar á prófunum
- `chore:` Almennar breytingar sem hafa ekki áhrif á virkni

Dæmi um commit með skammstöfun:
```sh
feat: Bætir við stuðningi við myrkraham í viðmóti
```

## Hagnýtar Git skipanir fyrir commit

- **Búa til commit:**
  ```sh
  git commit -m "Lýsing á breytingu"
  ```

- **Bæta við ítarlegri skýringu með multi-line commit:**
  ```sh
  git commit
  ```
  Þetta opnar textaritil þar sem hægt er að skrifa lýsandi commit skilaboð.

- **Breyta síðasta commit (ef það hefur ekki verið push-að ennþá):**
  ```sh
  git commit --amend -m "Uppfærð lýsing á commit"
  ```

Með þessum aðferðum verður auðveldara að viðhalda snyrtilegri og skiljanlegri commit sögu! 🚀
