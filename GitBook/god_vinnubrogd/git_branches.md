---
description: >-
  Leiðbeiningar um hvernig á að nota branches í Git, mikilvægi þeirra í vinnuflæði og góðar venjur varðandi nafngiftir.
---

# Hvernig nota branches í Git?

Branches (greinar) í Git eru leið til að vinna sjálfstætt á breytingum án þess að hafa áhrif á
aðalútgáfu (t.d. `main`). Þetta gerir kleift að vinna í nýjum eiginleikum, lagfæringum og tilraunum
á skipulagðan hátt.

## Af hverju að nota branches?

- **Aðskilja vinnu** – Hægt er að vinna í nýjum eiginleikum án þess að hafa áhrif á aðalútgáfu
  verkefnisins.
- **Samvinna** – Teymi geta unnið á mismunandi branches og sameinað breytingar þegar þær eru
  tilbúnar.
- **Öryggi** – Ef eitthvað fer úrskeiðis í breytingum er auðvelt að skipta aftur yfir í
  aðalútgáfuna.

## Algengar Git skipanir fyrir branches

- **Skoða allar greinar í verkefninu:**
  ```sh
  git branch
  ```
- **Búa til nýja grein:**
  ```sh
  git branch branch-nafn
  ```
- **Skipta yfir í grein:**
  ```sh
  git checkout branch-nafn
  ```
- **Búa til og skipta yfir í nýja grein í einni skipun:**
  ```sh
  git checkout -b branch-nafn
  ```
- **Sameina grein við aðra grein (t.d. aðalgreinina `main`):**
  ```sh
  git checkout main
  git merge branch-nafn
  ```
- **Eyða branch eftir sameiningu:**
  ```sh
  git branch -d branch-nafn
  ```
  Ef grein hefur ekki verið sameinuð en þú vilt samt eyða henni, þarf að nota `-D` í stað `-d`.

## Góðar venjur um nafngiftir á branches

Það er mikilvægt að velja lýsandi nöfn á branches frekar en að nota eigið nafn eða almenna
skammstöfun.

✅ **Góð dæmi um branch nöfn:**

- `feature-user-authentication` (nýr eiginleiki: notendaskráning)
- `bugfix-login-error` (lagfæring: innskráningarvilla)
- `hotfix-payment-gateway` (bráðabirgðalagfæring fyrir greiðslukerfi)
- `sandbox-experiment` (tilrauna branch fyrir prófanir)

❌ **Dæmi um slæm branch nöfn:**

- `helga` (Lýsir ekki hvað greinin gerir)
- `test` (Of almennt, ekki gagnlegt fyrir aðra notendur)
- `new` (Hvaða nýjung er þetta?)

Ef branch er bara fyrir **tilraunir eða persónulega notkun**, er í lagi að nota **sandbox-** sem
forskeyti, t.d. `sandbox-helga`.

## Sameining greina (merging) og merge conflicts

Þegar grein er sameinu[] getur komið upp **merge conflict** ef breytingar stangast á við
breytingar sem þegar eru í aðalútgáfunni.

- **Hvernig á að leysa merge conflict?**
    - Opnaðu skrána sem hefur árekstur (`<<<<<<< HEAD` og `>>>>>>>` merki).
    - Veldu hvaða breytingar eiga að haldast.
    - Fjarlægðu árekstramerkin.
    - Vistaðu og bættu við breytingunni:
      ```sh
      git add uppfærð-skrá
      git commit -m "Leysti merge conflict"
      ```

## Samantekt

| Skipun                     | Lýsing                                              |
|----------------------------|-----------------------------------------------------|
| `git branch`               | Sýnir öll branches í verkefninu                     |
| `git branch <nafn>`        | Býr til nýtt branch                                 |
| `git checkout <branch>`    | Skipta yfir í annað branch                          |
| `git checkout -b <branch>` | Býr til og skipta yfir í nýtt branch                |
| `git merge <branch>`       | Sameinar annað branch við það sem er nú þegar valið |
| `git branch -d <branch>`   | Eyðir branch eftir sameiningu                       |

Með þessum skrefum geturðu unnið á skilvirkan hátt með branches í Git! 🚀
