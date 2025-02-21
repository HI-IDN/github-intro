---
description: >-
  Mikilvægi þess að tryggja öryggi við geymslu lykilorða og annarra viðkvæmra upplýsinga í GitHub
  repo, og hvernig á að forðast öryggisbrot.
---

# Öryggismál og lykilorð í GitHub

Að vista lykilorð, notendanöfn eða aðrar viðkvæmar upplýsingar í GitHub repo sem er opinber (public)
er mjög alvarlegt öryggisbrot. Hér eru nokkrar ástæður fyrir því að það má aldrei gera þetta:

## Opnar fyrir öryggisbrot

Ef lykilorð eða API lyklar eru vistuð í GitHub repo, getur hver sem er nálgast þær upplýsingar og
misnotað þær. Þetta getur valdið því að óprúttnir aðilar fá aðgang að kerfum, gagnagrunnum, eða API
þjónustum í þínu nafni.

## Kostnaður

Ef API lyklar eða greiðsluþjónustur eru birtar óvart í repo, getur einhver annar notað þá lykla til
að framkvæma aðgerðir sem þú þarft svo að borga fyrir. Þetta getur valdið stórfelldum fjárhagslegum
skaða þar sem þú þarft að borga fyrir notkun sem einhver annar framkvæmdi.

## Öryggisbrestur og erfitt að laga

Þegar lykilorð eða lyklar eru vistaðir í GitHub sögunni, þá er ekki nóg að eyða bara skránni. Git
history (útgáfusagan) heldur utan um allar breytingar, þar með talið fyrri útgáfur skrárinnar þar
sem lykilorðin gætu enn verið til staðar. Að fjarlægja viðkvæmar upplýsingar úr sögu reposins er
flókið og oft er einfaldara að eyða öllu repo-inu og byrja frá grunni.

## Staða þín sem forritari

Að setja viðkvæmar upplýsingar í opinbera repo getur skaðað orðspor þitt sem forritari og dregið úr
trúverðugleika þínum hjá vinnuveitendum eða samstarfsaðilum. Það er talið alvarleg mistök að vista
slíkar upplýsingar í opinberum kóða.

## Hvernig á að koma í veg fyrir þetta?

- **Notið `.gitignore`**: Gætið þess að búa til skrár sem innihalda lykilorð og notendanöfn
  fyrirfram í `.gitignore` svo þær skrár séu ekki skráðar í version control.
- **Notið umhverfisbreytur**: Lykilorð og API lyklar ættu aldrei að vera harðkóðaðir í kóðann. Notið
  í staðinn umhverfisbreytur (environment variables) eða sérstakar uppsetningarskrár sem eru ekki
  hluti af Git.
- **Tryggið aðgangsstýringar**: Ef þið notið private repo, passið að tryggja að einungis réttir
  aðilar hafi aðgang að því.

Ef þið hafið þegar sett viðkvæmar upplýsingar í repo, hafið strax samband við kerfisstjóra eða
admin reposins til að fá leiðbeiningar um hvernig á að laga það.
