# Povijest

| Datum | Događaj |
|---|---|
| 30. 4. 2026. | prvi commit u pay.domovina.ai |
| 11. 5. 2026. | zauzet org `github.com/RevenueDog` |
| 22. 6. 2026. | zauzet org `github.com/RevenueDOGE` |
| 26.–27. 6. 2026. | prva razrada (Claude Code session u `novcanik-template`), brief „RevenueCat za web3" za VC raise, četveroslojna strategija ekosustava (airKUNA · RevenueDog · novčanik · builder) |
| 1. 8. 2026. | MPT u produkciji: 43 narudžbe, 41 forward, sav promet s `mpt:` referencom |
| 15. 8. 2026. | LinkedIn launch MPT-a |
| 5. 10. 2026. | multi-tenant rail (ADR 0017) mergan i deployan, isključen flagom |
| 7.–8. 10. 2026. | Revolut iOS počinje brisati referencu, pa nastaje stray resolver (ADR 0018); prva automatski povezana uplata za oko 12 s. Deployan detektor odljeva (ADR 0019). |
| 10. 10. 2026. | mpt.hr repozicioniran kao „RevenueCat za SEPA → EURe"; Matija: MPT globalno = RevenueDog; odluka da se MPT ne preimenuje |
| 11. 10. 2026. | ovaj repo |

## Riječima osnivača

Iz sessiona (pravopis originalan):

> „…recimo RevenueCat je trenutno najjaci svjetski igrac koji super hendla
> in-app-purcases sto je jako slicno self-custody walletu … pa sam ja zato napravio dvije
> GitHub organizacije … mislim da je jasno Cat Dog i Bitcoin DOGE :D … da to ima globalnu
> pricu :D"
> — 26. 6. 2026.

> „…zelim … da je RevenueDog iskljucivo web3 revenue, hrpa developera je familiar sa
> RevenueCat i ne ulazim u taj web2 biznis nego isti experience ali sa web3 railom, tako da
> ista mobile/web aplikacija moze imati i RevenueCat i RevenueDog SDK-ove ugradjene :D"
> — 26. 6. 2026.

> „…ako smo mi onchain rješenjen sto je IAM RevenueCat ima smisla prozvod globalnon
> nazvati RevenueDog :D"
> — 10. 10. 2026.

> „…na globalnon razini mpt bude RevenueDog i jos prije RevenueDOGE to ima definitivnon
> smisla jer igra rijeci je fenomelnaala…"
> — 11. 10. 2026.

## Što se iz lipnja nije ostvarilo

- recurring spike (Q3), SDK skeleton (Q4)
- sedam dokumenata iz briefa §9 (narrative, market, competitors, spike-recurring, pricing,
  raise, x-launch)
- push briefa na GitHub

Umjesto toga izgrađen je backend koji brief nije predvidio: bank-first, multi-tenant,
non-custodial.
