---
description: >-
  Leiðbeiningar um hvernig á að búa til skýr og gagnleg pull requests í GitHub.
---

# Hvernig á að skrifa góð Pull Requests (PRs)?

Pull requests (PRs) eru mikilvægur hluti af samvinnu í GitHub verkefnum. Gott PR ætti að vera skýrt og veita rýnum (reviewers) nauðsynlegan bakgrunn til að meta breytingarnar.

## Af hverju skiptir máli að skrifa góð PRs?
- **Sparar tíma rýna** – Lýsandi PR hjálpar öðrum að átta sig á breytingunum fljótt.
- **Betri endurgjöf** – Skýr PR gerir rýnum kleift að veita gagnlegri athugasemdir.
- **Skilvirkari samþætting** – Með góðum PR er auðveldara að sameina breytingarnar án ruglings.

## Hvað á PR að innihalda?

1. **Góða fyrirsögn** – Hún ætti að vera lýsandi og segja hvað PR-ið gerir.
   ```
   Bætir við tveggja þátta auðkenningu fyrir innskráningu
   ```

2. **Samantekt (Description)** – Útskýrir hvað var gert og hvers vegna.
   ```markdown
   ## Lýsing
   Þessi breyting bætir við tveggja þátta auðkenningu (2FA) með Google Authenticator.
   Notendur þurfa að slá inn kóða úr síma sínum þegar þeir skrá sig inn.
   ```

3. **Tengingar við issues** – Ef PR-ið leysir ákveðið issue, notaðu `Fixes #X`.
   ```markdown
   Fixes #42
   ```

4. **Hvernig prófa má breytingarnar** – Leiðbeiningar fyrir rýna um hvernig þeir geta prófað kóðann.
   ```markdown
   ## Prófanir
   1. Skráðu þig inn með notanda.
   2. Athugaðu hvort þú sért beðinn um 2FA kóða.
   3. Sláðu inn réttan kóða og staðfestu að innskráning virki.
   ```

5. **Skjáskot (ef við á)** – Ef breytingarnar hafa áhrif á UI, bættu við mynd.
   ```markdown
   ![Screenshot of new login screen](https://example.com/screenshot.png)
   ```

6. **Hvað þarf að athuga?** – Eru einhverjir aukahlutir sem þarf að skoða?
   ```markdown
   ## Athugasemdir
   - Þarfnast uppfærslu á skjölum
   - Ekki búið að skrifa prófanir fyrir 2FA ennþá
   ```

7. **Óskað eftir rýnendum** – Merktu viðeigandi aðila til að fara yfir kóðann.

## Gott PR vs. Slæmt PR

✅ **Gott PR**
```markdown
## Lýsing
Bætir við virkni til að vista notendastillingar í gagnagrunni.

Fixes #12

## Prófanir
1. Opnaðu stillingasíðuna.
2. Breyttu notendanafni og vistaðu.
3. Athugaðu að breytingarnar eru skráðar í gagnagrunninn.
```

❌ **Slæmt PR**
```markdown
Breytti einhverju í stillingum.
```

Skýr og skipulögð PR hjálpa öllum að vinna betur saman! 🚀
