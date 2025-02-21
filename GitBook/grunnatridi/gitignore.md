---
description: >-
  Leiðbeiningar um notkun `.gitignore` í Git, hvernig á að koma í veg fyrir að viðkvæmar skrár
  lendi í geymslu og hvernig á að stilla sérsniðna `.gitignore` skrá.
---

# `.gitignore` – Hvað og hvers vegna?

`.gitignore` er skrá sem segir Git að hunsa ákveðnar skrár eða möppur þegar verið er að skrá
breytingar í Git. Þetta kemur í veg fyrir að óþarfa eða viðkvæm gögn lendi í Git geymslunni.

## Bæta við `.gitignore` í nýtt verkefni

Þegar þú býrð til nýtt repo á **GitHub.com** er hægt að velja að bæta við `.gitignore` skrá
út frá ákveðnu forritunarmáli (t.d. Python, Node.js, C++ eða TeX). Hins vegar er aðeins hægt að
velja
**eitt** tungumál í þessu viðmóti, þannig að ef þú vinnur með mörg tungumál eða fleiri stillingar
gæti verið þörf á að breyta skránni handvirkt.

## Af hverju að nota `.gitignore`?

- **Koma í veg fyrir að viðkvæmar skrár séu geymdar í Git**
- **Hindra óþarfa skrár (t.d. afleiddar skrár og log skrár) í að lenda í Git geymslu**
- **Viðhalda hreinleika verkefnisins með því að hunsa skrár sem skipta ekki máli fyrir þróunina**

## Skrár sem ættu alltaf að vera í `.gitignore`

### Viðkvæmar upplýsingar

> Þetta eru skrár sem innihalda lykilorð, API lykla, og annað sem á ekki að birtast opinberlega.

- **`.env` skrár** (t.d. `config.env`, `.env.local`)
- **SSH lyklar og cert skrár** (t.d. `id_rsa`, `id_rsa.pub`)
- **JSON eða YAML skrár með lykilorðum**

### Afleiddar skrár og útgefnar skrár

> Þetta eru skrár sem eru búnar til sjálfkrafa og ættu ekki að vera í Git geymslu.

- **Tímabundnar skrár og log skrár**
  ```
  *.log
  *.tmp
  *.swp
  ```
- **Afleiddar bin skrár**
  ```
  *.exe
  *.dll
  *.out
  *.o
  ```
- **Cache og háhraðaminni**
  ```
  .cache/
  node_modules/
  __pycache__/
  ```

### Sérstillt `.gitignore` eftir forritunarmáli

#### Python verkefni

```
__pycache__/
*.pyc
*.pyo
venv/
```

#### Node.js verkefni

``` 
node_modules/
package-lock.json
npm-debug.log
```

#### C/C++ verkefni

``` 
*.o
*.so
*.out
*.exe
```

#### TeX verkefni

```
*.aux
*.log
*.synctex.gz
*.toc
*.lof
*.lot
*.fls
*.fdb_latexmk
```

## Hvernig á að bæta skrám við `.gitignore`?

1. Búðu til skrána handvirkt (ef hún er ekki þegar til):
   ```sh
   touch .gitignore
   ```
2. Opnaðu `.gitignore` og bættu við skrám sem á að hunsa.
3. Staðfestu að skráin virki með:
   ```sh
   git status
   ```
   Skrár sem eru í `.gitignore` ættu ekki að birtast í úttaki `git status`.

## Hvað ef ég gleymdi að bæta við `.gitignore` í upphafi?

Ef þú hefur þegar bætt við skrám sem ættu að vera í `.gitignore`, breytir það **ekki** sjálfkrafa
því sem þegar er í geymslunni. Þú þarft að fjarlægja skrárnar handvirkt með:

```sh
 git rm --cached file_to_remove
```

Og svo skrá breytinguna:

```sh
 git commit -m "Bætti file_to_remove við .gitignore"
```

### **Að fjarlægja viðkvæmar skrár alveg úr Git sögunni**

Ef skrá sem inniheldur viðkvæmar upplýsingar (t.d. lykilorð eða API lykla) hefur **þegar** verið
sett í Git, þá er ekki nóg að eyða henni með `git rm`. Hún er ennþá aðgengileg í Git sögunni. Til að
fjarlægja hana alveg:

```sh
 git filter-branch --force --index-filter 'git rm --cached --ignore-unmatch <skrá>' --prune-empty --tag-name-filter cat -- --all
```

> ⚠️ **Að framkvæma þessa aðgerð breytir Git sögunni og getur valdið vandræðum ef aðrir eru að
> vinna í geymslunni.** Það er mælt með að
> nota [BFG Repo-Cleaner](https://rtyley.github.io/bfg-repo-cleaner/)
> fyrir einfaldari hreinsun á viðkvæmum skrám.
>
> Þetta er aðeins fyrir þá Git-notendur sem vita hvað þeir eru að gera og hafa skilið
> afleiðingar þess. Passa þarf að allir sem vinna í geymslunni vita að þessi aðgerð er í gangi,
> annars getur það valdið verulegum vandræðum.

## Þegar þú vilt bæta við skrá sem er í `.gitignore`

Ef þú þarft að bæta skrá sem er í `.gitignore` samt sem áður, þá færðu villu nema þú notar
`--force`:

```sh
 git add -f file_to_include
```

Þetta er gagnlegt ef þú ert að vinna með undantekningar, en ætti að nota með varúð.

## Samantekt

| Skipun                                         | Lýsing                                      |
|------------------------------------------------|---------------------------------------------|
| `touch .gitignore`                             | Býr til `.gitignore` skrá                   |
| `echo "*.log" >> .gitignore`                   | Bætir við reglur í `.gitignore`             |
| `git rm --cached <skrá>`                       | Fjarlægir skrá úr Git en ekki úr verkefninu |
| `git add -f <skrá>`                            | Bætir skrá við Git þrátt fyrir `.gitignore` |
| `git status`                                   | Sýnir ekki hunsaðar skrár                   |
| `git filter-branch --force --index-filter ...` | Fjarlægir skrá **alveg** úr Git sögunni ⚠️  |

Með því að nota `.gitignore` skynsamlega tryggir þú að Git geymslan þín haldist snyrtileg og örugg
🚀
