---
description: >-
  Stutt kynning á Git og GitHub fyrir byrjendur, hvernig þau virka og hvernig hægt er að nýta þau
  í námi og starfi.
---

# Hvað er Git og GitHub?

Git og GitHub eru lykilverkfæri í útgáfustjórnun og samvinnu á hugbúnaðarverkefnum. Þau eru mikið
notuð í forritun, rannsóknum og jafnvel skjölun verkefna.

## Git

Git er dreift útgáfustjórnunarkerfi (version control system) sem gerir notendum kleift að:

- Halda utan um breytingar í kóða og skrám.
- Skrá og endurheimta fyrri útgáfur af skjölum.
- Vinna í hópum með sjálfstæðar útgáfur (branches) og sameina breytingar á öruggan hátt.

## GitHub

GitHub er vefþjónusta sem veitir geymslu og stjórnun á Git geymslum (repositories). Auk þess
býður GitHub upp á verkfæri fyrir samvinnu og skipulagningu verkefna, eins og:

- **Fjargeymslur (repositories)** til að deila kóða með öðrum.
- **Pull requests** fyrir samvinnu og kóðaúttektir.
- **Issues** og **Projects** til að halda utan um verkefna- og villustjórnun.
- **Actions** fyrir sjálfvirkar keyrslur (CI/CD).

### Er GitHub ókeypis?

- GitHub er **almennt ókeypis** fyrir alla notendur.
- **GitHub Education pakkinn** býður upp á **GitHub Pro**, sem inniheldur:
    - **GitHub Copilot** (AI-aðstoð í forritun) ókeypis fyrir nemendur.
    - Meiri geymslupláss fyrir einkageymslur (private repos).
    - Aukna greiningu á kóða (advanced code insights).

## Frí GitHub aðgangur fyrir nemendur og akademískt starfsfólk

GitHub býður **frítt** akademískt aðgengi í gegnum [GitHub Education](https://github.com/education).

- Nemendur geta fengið **GitHub Pro** áskrift með ókeypis **GitHub Copilot**.
- Til að fá aðgang þarf að skrá sig með **háskólanetfangi (`@hi.is`)** eða tengja það við GitHub
  reikninginn.
- Hægt er að setja **háskólanetfang sem secondary email** í stillingum GitHub reikningsins.
- Nemendur geta einnig fengið **ókeypis microcredential** í
  gegnum [GitHub Foundations Certificate](https://education.github.com/experiences/foundations_certificate).
- Kennarar geta sett upp **GitHub Classroom** fyrir verkefnastjórnun og
  námskeið: [GitHub Classroom](https://classroom.github.com/).

## Hvernig á að byrja?

1. **Setja upp Git**
    - Sæktu og settu upp Git frá [git-scm.com](https://git-scm.com/).
    - Stilltu notendaupplýsingar með skipunum:
      ```sh
      git config --global user.name "Nafn"
      git config --global user.email "netfang@example.com"
      ```

2. **Búa til GitHub reikning**
    - Farðu á [GitHub](https://github.com/) og stofnaðu reikning.
    - Tengdu háskólanetfangið þitt í [stillingum GitHub](https://github.com/settings/emails).
    - Skráðu þig í [GitHub Education](https://education.github.com/) til að fá ókeypis aðgang að
      GitHub Pro.

3. **Búa til fyrsta geymsluna (repository)**
    - Smelltu á **New repository** í GitHub.
    - Gefðu verkefninu nafn, lýsingu og veldu public eða private.
    - Fylgdu leiðbeiningunum til að bæta verkefninu við tölvuna þína með Git.

4. **Grunnskipanir í Git**
    - Klóna geymslu:
      ```sh
      git clone https://github.com/your-username/your-repo.git
      ```
    - Bæta skrá við Git:
      ```sh
      git add filename
      ```
    - Skrá breytingu:
      ```sh
      git commit -m "Lýsing á breytingu"
      ```
    - Sækja nýjustu breytingar úr GitHub:
      ```sh
      git pull origin main
      ```
    - Ýta breytingum á GitHub:
      ```sh
      git push origin main
      ```
    - Skoða breytingasögu verkefnis:
      ```sh
      git log --oneline --graph --all
      ```

Með þessum grunnatriðum geturðu hafið vinnu með Git og GitHub á öruggan og skilvirkan hátt! 🚀