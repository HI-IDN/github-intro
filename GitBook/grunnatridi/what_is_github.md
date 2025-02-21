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

- GitHub er **almennt ókeypis** fyrir alla notendur. Helsta virkni GitHub er opið fyrir alla, en
  fyrir stærri verkefni og fyrirtæki er **GitHub Pro** með greiðsluáskrift.
- **GitHub Education pakkinn** býður upp á **GitHub Pro**, sem inniheldur:
    - **GitHub Copilot** (AI-aðstoð í forritun).
    - Meiri geymslupláss fyrir einkageymslur (private repos).
    - Aukna greiningu á kóða (advanced code insights).
- Almennt er ókeypis virkni fyrir **public repos** en lokað fyrir **private repos**, nema með
  greiðsluáskrift.

### GitHub Education pakkinn

Nemendur og akademískt starfsfólk geta fengið **GitHub Pro** áskrift með ókeypis **GitHub
Copilot**.

Til að fá aðgang þarf að skrá sig með **háskólanetfangi (`@hi.is`)** eða tengja það við GitHub
reikninginn.
Hægt er að setja **háskólanetfang sem secondary email** í stillingum GitHub reikningsins.

Það þarf að taka mynd af gildu háskólakorti og senda inn til staðfestingar ásamt að vera tengt
háskólaneti (t.d. eduroam eða nota VPN til að tengjast HÍ-neti).

> **Nemendur** geta einnig fengið frítt **microcredential** í gegnum
> [GitHub Foundations Certificate](https://education.github.com/experiences/foundations_certificate).

> **Kennarar** geta sett upp **GitHub Classroom** fyrir verkefnastjórnun og
> námskeið: [GitHub Classroom](https://classroom.github.com/).

## Hvernig á að byrja?

### Setja upp Git

Git er hægt að nota bæði í **skipanalínu (CLI)** og í **myndrænu viðmóti (GUI)**:

- **Skipanalína (CLI)**: Sæktu og settu upp Git frá [git-scm.com](https://git-scm.com/) og notaðu
  skipanir í `bash`, `cmd` eða `PowerShell`.
- **GitHub Desktop**: Einföld leið fyrir byrjendur með myndrænt viðmót, hægt að sækja
  frá [desktop.github.com](https://desktop.github.com/).
- **Git innbyggt í IDE**: Í flestum forritunarumhverfum er native stuðningur við Git, til
  dæmis er Git innbyggt sem *extension* í Visual Studio Code, PyCharm, IntelliJ IDEA og RStudio .
  Helsti kosturinn er að þessi IDE bjóða upp á samþætt stjórnborð fyrir Git, þannig þú getur
  notað GUI eða CLI eftir hvað þér hentar best hverju sinni.

Stilltu notendaupplýsingar með skeljar skipunum:

  ```sh
  git config --global user.name "Nafn"
  git config --global user.email "notendanafn@hi.is"
  ```

### Búa til GitHub reikning

Farðu á [GitHub](https://github.com/) og stofnaðu reikning.
Tengdu háskólanetfangið þitt í [stillingum GitHub](https://github.com/settings/emails) (þarf
ekki að vera primary netfang).
Skráðu þig í [GitHub Education](https://education.github.com/) til að fá ókeypis aðgang að
GitHub Pro.

### Búa til fyrstu geymsluna (repository)

- Smelltu á **New repository** í [GitHub](https://github.com/new).
- Gefðu verkefninu nafn, lýsingu og veldu public eða private.
    - **Public** er opinber geymsla sem allir geta séð.
    - **Private** er lokað geymsla sem aðeins þú og aðrir sem þú býður inn geta séð.

> Hægt er að búa til geymslur beint í tölvunni með `git init`, en það er einfaldara að byrja á
> GitHub og klóna geymsluna niður á tölvuna.

