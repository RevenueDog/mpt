# RevenueDog · MPT — knowledge base

> **The money goes to the merchant. We just fetch the state.**
> RevenueCat drži stanje in-app kupnji, a novac isplaćuju Apple i Google.
> RevenueDog drži stanje bankovnih i onchain uplata, a novac (EURe) ide izravno trgovcu.

Ovaj repo je **lokalni single source of truth** za ideju da se **MPT (Mint Pay Transfer)**,
proizvod koji danas radi na [mpt.hr](https://mpt.hr) i u kodu
[pay.domovina.ai](https://github.com/domovinatv/pay.domovina.ai), globalno opiše i slaže kao
**RevenueDog**, odnosno **RevenueDOGE**.

Ovdje je početna točka za opisivanje proizvoda. Kod je drugdje, a odluke se bilježe ovdje.

**Status (11. 10. 2026.): razmišljanje i kreativna razrada.** MPT se ne preimenuje.
mpt.hr, prefiks reference `mpt:` i Telegram `mpt_hr` ostaju.

## Karta

| # | Dokument | Što drži |
|---|---|---|
| 01 | [Teza](docs/01-teza.md) | zašto Cat → Dog → DOGE uopće ima smisla, u jednoj stranici |
| 02 | [Proizvod danas](docs/02-proizvod-danas.md) | što MPT stvarno radi: tok novca, API, webhookovi, izmjerene brojke, status |
| 03 | [RevenueCat ↔ RevenueDog](docs/03-revenuecat-mapa.md) | pojam po pojam, što postoji, što fali |
| 04 | [Arhitektura brenda](docs/04-arhitektura-brenda.md) | RevenueDog vs RevenueDOGE vs MPT vs airKUNA, opcije i preporuka |
| 05 | [Pseći rječnik](docs/05-psec-rjecnik.md) | semantika psa kao sustav: Fetch, Tag, Leash, Sniff, Bark… |
| 06 | [Poruke i copy](docs/06-poruke.md) | taglinei, pitchevi (hr/en), naslovi, nacrt X launch threada, README hero |
| 07 | [Tržište](docs/07-trziste.md) | RevenueCat danas, konkurencija, EU vjetar u leđa |
| 08 | [Ime i rizici](docs/08-ime-i-rizici.md) | tko još koristi ime, domene, žig, DOGE, regulatorna linija |
| 09 | [Roadmap proizvoda](docs/09-roadmap.md) | moduli od današnjeg MPT-a do RevenueDoga |
| 10 | [Odluke i otvorena pitanja](docs/10-odluke.md) | dnevnik odluka i popis za Matiju |
| — | [Povijest](docs/povijest.md) | od svibnja 2026. do danas, s citatima osnivača |
| — | [Izvori](docs/izvori.md) | gdje je istina za svaku tvrdnju |
| — | [Pojmovnik](docs/pojmovnik.md) | intent, sid, tenant, EURe, Safe, Roles… |

## Pravila ovog repoa

1. **Činjenice o mehanizmu dolaze iz pay.domovina.ai, ne iz ovog repoa.** Ovdje je
   preslika na dan 11. 10. 2026. Kad se kod promijeni, ažurira se
   [02](docs/02-proizvod-danas.md), a ne obrnuto.
2. **Razlikuj tri vremena:** *radi u produkciji*, *napisano ali isključeno*, *plan*. Svaka
   marketinška rečenica mora preživjeti tablicu statusa u [02](docs/02-proizvod-danas.md#status).
3. **Repo pišemo kao da je javan.** Oba GitHub orga su Matijina, a repo bi se mogao pushati.
   Zato ovdje nema ovoga:
   - sigurnosnih rupa ni nalaza iz reviewa
   - interne analize Moneriumovih uvjeta korištenja
   - imena VC fondova ni pregovaračkih detalja
   - privatnih planova koji nisu o proizvodu
4. **„mpt" ima dva značenja u starim dokumentima.** U lipanjskoj strategiji je to creator
   pilot „mpt (glazba)". Ovdje MPT uvijek znači Mint Pay Transfer.
5. Hrvatski za razradu, engleski za copy koji ide van.
