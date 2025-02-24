---
description: >-
  Leiðbeiningar um hvernig á að framkvæma gagnlega og uppbyggilega kóðarýni.
---

# Hvernig framkvæma góða kóðarýni?

Kóðarýni (code review) er mikilvægur hluti af þróunarferli sem tryggir að kóðinn sé skiljanlegur, öruggur og vel skrifaður. Rýnir ber ábyrgð á því að hjálpa til við að bæta gæði kóðans áður en hann er sameinaður aðalgreininni.

## Af hverju er kóðarýni mikilvæg?
- **Tryggir gæði kóðans** – Hjálpar til við að finna villur og betrum bæta lausnir.
- **Deiling þekkingar** – Nýir liðsmenn læra af betri kóðunaraðferðum.
- **Tryggir samræmi** – Gæti að verkefnið fylgi stöðluðum forritunarvenjum.

## Hlutverk rýnanda
- **Fara yfir breytingarnar í smáatriðum**
- **Ekki samþykkja PR í blindni** – Vertu viss um að skilja kóðann
- **Óska eftir útskýringum ef nauðsynlegt er**
- **Keyra kóðann sjálfur og prófa virkni**
- **Vera uppbyggilegur í athugasemdum**
- **Nota inline comments fyrir skýra tilvísun í kóða**
- **Nota `suggestion` virknina til að leggja fram breytingar án þess að skrifa yfir kóða beint**
- **Ef kóðinn virkar ekki eins og til er ætlast, sýna skjáskot af villunni eða óvæntri hegðun**

## Hvað á að skoða í kóðarýni?

### 1️⃣ Skiljanleiki og læsileiki
- Er kóðinn auðlesanlegur og vel skipulagður?
- Nota nafngiftir skýrt og lýsandi heiti?
- Hefur verið forðast óþarfa flækjur og hringtengingar?

### 2️⃣ Villuleit og stöðugleiki
- Getur þessi kóði leitt til óvæntra villna?
- Hafa verið prófanir fyrir breytingarnar?
- Er kóðinn þolinn fyrir röngum inntökum?

### 3️⃣ Fylgni við verkefnastöðlun
- Fylgir kóðinn kóðastíl verkefnisins?
- Passar breytingin við arkitektúr verkefnisins?

### 4️⃣ Afköst og skilvirkni
- Er kóðinn of flókinn fyrir einfaldan tilgang?
- Hefði verið betra að nota aðra nálgun sem er hraðvirkari?

## Hvernig á að gefa góða endurgjöf?

### Dæmi um góð og slæm endurgjöf

✅ **Góð endurgjöf**
```markdown
Mjög flott útfærsla! Hins vegar, gætirðu notað `map()` hér í stað `for` lykkju til að einfalda kóðann?
```
```markdown
Þetta virkar vel, en mér finnst skýrleikinn betri ef við skiptum þessu í minni aðgerðir. Gætirðu búið til fall fyrir þessa útreikninga?
```
```markdown
Sjá skjáskot hér að neðan – úttakið er ekki eins og til er ætlast. Gætirðu athugað hvað veldur þessu?
![Skjáskot](https://example.com/error_screenshot.png)
```

❌ **Slæm endurgjöf**
```markdown
Mjög flott, virkar.
```
```markdown
Þetta er ekki gott. Lagaðu þetta.
```
```markdown
Ég skil ekki kóðann.
```

### Nota inline comments og `suggestion`
Í GitHub PR er hægt að gera athugasemdir við einstakar línur með inline comments. Einnig er hægt að nota `suggestion` til að sýna tillögur á breytingum:
``````markdown
```suggestion
for item in list_of_items:
    process(item)
```
``````
Ef um **Markdown** skjal er að ræða, er hægt að nota `suggestion` til að lagfæra kóðablokkir:
``````markdown
````suggestion
```python
# Endurbætt útgáfa
for item in list_of_items:
    process(item)
```
````
``````

Þetta gerir það auðveldara fyrir forritara að taka tillit til breytinga án þess að rýnir breyti beint í kóðann.

## Samþykki, synjun og beiðni um breytingar

Í kóðarýni er hægt að:
- **Samþykkja PR** – Þegar kóðinn uppfyllir allar kröfur.
- **Óska eftir breytingum** – Þegar þarf að laga hluti áður en hægt er að samþykkja.
- **Setja athugasemdir án þess að hindra PR** – Til að gefa uppbyggilega endurgjöf án þess að krefjast breytinga.

## Reglur fyrir PR samþykktir
Í **opinberum GitHub geymslum** er hægt að stilla reglur:
- **Að lágmarki tveir rýnendur þurfa að samþykkja PR**.
- **PR má ekki sameina ef óleyst samtöl eru til staðar**.
- **Aðeins notendur með tiltekin réttindi geta samþykkt breytingar í aðalgrein**.

Góð kóðarýni er ekki bara um að leita að villum, heldur einnig um að hjálpa teyminu að skrifa betri kóða! 🚀
