---
description: >-
  Hér eru helstu Git skipanir sem þarf að þekkja til að geta unnið með Git
  geymslur, ásamt samantekt á lengra komnum skipunum.
---

# Skipanir í Git

Git er öflugt útgáfustjórnunarkerfi sem gerir þér kleift að vinna með kóða og skjöl á skilvirkan
hátt.
Hér eru helstu skipanir sem þú þarft að kunna.

## Búa til eða klóna geymslu

- **Búa til nýja Git geymslu í möppu:**
  ```sh
  git init
  ```
  Þetta býr til tóma Git geymslu í núverandi möppu. Almennt mælt með að búa til nýtt repo á
  GitHub vefviðmótinu og klóna það niður á tölvuna, þá er hægt að stilla fleiri valkosti, eins og
  hvort geymslan á að vera opin eða lokuð, innihalda `.gitignore` eða `LICENSE` skrár og fleira.

- **Klóna núverandi geymslu af GitHub:**
  ```sh
  git clone https://github.com/your-username/your-repo.git
  ```
  Sækir geymsluna og afritar hana á tölvuna þína.
  Einnig er hægt að endurnefna geymsluna með að bæta við nafni á endanum:
  ```bash
  git clone https://github.com/your-username/your-repo.git new-repo-name
  ```

## Unnið með breytingar

- **Sýna stöðu verkefnis:**
  ```sh
  git status
  ```
  Sýnir hvaða skrár eru í vinnslu, hvaða breytingar eru óskráðar og hvaða skrár eru í undirbúningi
  fyrir commit.

- **Bæta skrám við Git (undirbúa fyrir skráningu):**
  ```sh
  git add filename
  ```
  Eða bæta við öllum skrám:
  ```sh
  git add .
  ```

- **Skrá breytingar í Git:**
  ```sh
  git commit -m "Lýsing á breytingu"
  ```
  Þetta vistar breytingarnar í *staðbundinni* Git geymslu (þ.e.a.s. á tölvunni þinni, en ekki
  á GitHub.com).

## Sameina breytingar og leysa árekstra

Þegar breytingar eru sameinaðar getur verið að árekstrar (merge conflicts) komi upp ef aðrir hafa
breytt sömu skránum eða ef breytingar rekast á.

- **Hvað gerist við merge conflict?**
    - Git getur ekki ákveðið sjálfkrafa hvaða breytingar á að halda og biður þig að leysa
      áreksturinn.
    - Skjöl sem hafa árekstra verða merkt í Git sem óleyst (`unmerged`).

- **Hvernig á að leysa merge conflict?**
    - Opnaðu skrárnar sem Git hefur merkt sem í árekstri.
    - Leitaðu að `<<<<<<< HEAD` og `>>>>>>>` merkjum í skránum.
    - Veldu hvaða breytingar eiga að fara í lokaútgáfuna og fjarlægðu árekstramerkin.
    - Þegar breytingarnar hafa verið leystar:
      ```sh
      git add uppfærðar-skrár
      git commit -m "Leysti merge conflict"
      ```

## Vinna með submodules

Submodules eru notuð þegar þú vilt bæta við öðru Git repo innan verkefnisins þíns.
Þetta er gagnlegt þegar þú vilt halda utan um annað repo sem hluta af verkefninu án þess að samlaga
það beint við geymsluna.

- **Bæta við Git submodule:**
  ```sh
  git submodule add https://github.com/example/example-submodule.git path/to/submodule
  ```
  Þetta bætir `example-submodule` við í `path/to/submodule` og tengir það sem sér Git geymslu.

- **Sækja submodules eftir klónun:**
  ```sh
  git submodule update --init --recursive
  ```
  Þetta tryggir að öll submodules séu sótt og sett upp rétt.

- **Uppfæra submodules í nýjustu útgáfu:**
  ```sh
  git submodule update --remote --merge
  ```
  Þetta sækir nýjustu breytingar í hverri submodule og sameinar í aðalrepo-ið þitt.

## Samantektartafla

| Skipun                          | Lýsing                                        |
|---------------------------------|-----------------------------------------------|
| `git init`                      | Býr til nýja Git geymslu                      |
| `git clone <url>`               | Klónar Git geymslu                            |
| `git status`                    | Sýnir stöðu verkefnis                         |
| `git add <file>`                | Bætir skrá við undirbúning                    |
| `git commit -m "msg"`           | Skráir breytingar                             |
| `git pull origin main`          | Sækir nýjustu breytingar                      |
| `git push origin main`          | Ýtir breytingum á GitHub                      |
| `git merge <branch>`            | Sameinar breytingar úr öðrum branch           |
| `git submodule add <url>`       | Bætir við submodule                           |
| `git submodule update --init`   | Sækir submodules eftir klónun                 |
| `git submodule update --remote` | Uppfærir submodules í nýjustu útgáfu          |
| `git checkout <branch>`         | Skipta yfir í annan branch                    |
| `git checkout -b <branch>`      | Búa til og skipta yfir í nýjan branch         |
| `git branch -d <branch>`        | Eyða branch                                   |
| `git commit --amend -m "msg"`   | Breytir síðasta commit færslu                 |
| `git push --force`              | Ýtir breytingum og skrifar yfir fyrri gögn ⚠️ |

Með þessum skipunum geturðu unnið á skilvirkan hátt með Git og GitHub! 🚀
