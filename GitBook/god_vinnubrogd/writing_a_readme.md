---
description: >-
  Leiðbeiningar um hvað ætti að vera í README.md skrá í GitHub repo.
---

# Hvað á að vera í `README.md`?

`README.md` er fyrsta skráin sem flestir sjá þegar þeir heimsækja GitHub repo. Hún ætti að veita skýra og gagnlega yfirsýn yfir verkefnið og leiðbeina notendum um hvernig á að nota það.

## Sérstaða `README.md`

- **GitHub birtir sjálfkrafa `README` skrána á forsíðu geymslu.**
- **Hægt er að nota annaðhvort `README` eða `README.md`**, en `.md` endingin gerir skjalið auðlesanlegra með Markdown uppsetningu.
- **Gott Markdown snið** eykur læsileika með fyrirsögnum, listum og kóðakössum.

## Grundvallaratriði í `README.md`

Hér eru lykilatriðin sem ættu að vera í `README.md`:

### 1️⃣ Heiti og lýsing
- **Nafn verkefnisins** – Stuttur titill efst í skjalinu.
- **Lýsing** – Hvað gerir verkefnið og hver er tilgangur þess?

Dæmi:
```markdown
# Gagnavinnslutól
Þetta er einfalt Python forrit sem hreinsar og umbreytir CSV gögn fyrir frekari úrvinnslu.
```

### 2️⃣ Uppsetning og notkun
Hvernig setja skal upp verkefnið og keyra það. Þetta ætti að innihalda:
- **Kerfiskröfur** (t.d. Python 3.10, PostgreSQL, Node.js)
- **Uppsetningarleiðbeiningar** (t.d. með `pip install` eða `npm install`)
- **Hvernig keyra á verkefnið**

Dæmi:
`````markdown
## Uppsetning

1. Klónaðu geymsluna:
   ```sh
   git clone https://github.com/your-username/your-repo.git
   ```
2. Farðu inn í verkefnamöppuna:
   ```sh
   cd your-repo
   ```
3. Settu upp nauðsynlegar pakkar:
   ```sh
   pip install -r requirements.txt
   ```
`````

### 3️⃣ Dæmi um notkun
Hvernig á að nota verkefnið með dæmum.

`````markdown
## Notkun

Til að umbreyta CSV gögnum:
```sh
python process_data.py input.csv output.csv
```
`````

### 4️⃣ Framlag frá öðrum
Ef verkefnið er opið fyrir framlag, skráðu:
- Hvernig notendur geta lagt sitt af mörkum.
- Hvaða vinnuflæði á að fylgja (t.d. `git fork -> branch -> pull request`).

`````markdown
## Framlag

Framlög eru velkomin! Vinsamlega fylgdu þessum skrefum:

1. Gerðu fork af geymslunni.
2. Búðu til nýjan branch: `git checkout -b feature-nafn`.
3. Gerðu breytingarnar og skráðu þær: `git commit -m "Lýsing á breytingu"`.
4. Ýttu breytingunum í þitt eigið repo: `git push origin feature-nafn`.
5. Sendu pull request.
`````

### 5️⃣ Leyfi og höfundar
Hvaða leyfi gildir fyrir verkefnið (t.d. MIT, GPL)?

`````markdown
## Leyfi

Þetta verkefni er gefið út undir MIT leyfi – sjá [`LICENSE`](LICENSE) fyrir frekari upplýsingar.
`````

## Viðbótaratriði

Fyrir stærri verkefni má bæta við eftirfarandi:
- **Merki og tákn** (t.d. CI/CD stöðu, niðurhalsfjölda)
- **Gögn um tengiliðaupplýsingar**
- **Tengingar í frekari skjöl, t.d. Wiki eða API docs**

---

### Samantekt

| Hluti | Lýsing |
|--------|--------|
| Heiti & lýsing | Hvað verkefnið gerir |
| Uppsetning | Hvernig setja skal upp og keyra verkefnið |
| Notkun | Dæmi um hvernig verkefnið er notað |
| Framlag | Leiðbeiningar fyrir þá sem vilja leggja sitt af mörkum |
| Leyfi | Hvaða leyfi verkefnið hefur |

Skýr og vel skipulögð `README.md` skrá hjálpar öllum að skilja verkefnið betur! 🚀