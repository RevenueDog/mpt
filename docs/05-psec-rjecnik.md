# 05 · Pseći rječnik

Mačka te ignorira, a pas ti donese. Ovaj rječnik pokazuje da metafora psa nije ukras, nego
točan opis mehanizma. Svaki pojam ima tehnički par u kodu, pa se priča ne može odlijepiti od
istine.

| Pseći pojam | Što je u stvarnosti | Kod / ADR | Rečenica za copy |
|---|---|---|---|
| **Tag** (pločica na ogrlici) | referenca `mpt:0x<trgovac>?sid=<intent>` u SEPA nalogu | `backend/src/monerium/sid.ts` | *Every payment wears a tag that says who it belongs to.* |
| **Fetch** | forward EURe s prihvatnog Safea na trgovčevu odobrenu adresu | `router/safe.ts` | *We fetch. We don't keep.* |
| **Owner** | trgovac (tenant) s vlastitim reguliranim računom | ADR 0016/0017 | *The money goes to the owner. Always.* |
| **Kennel** | tenantov prihvatni Safe (multisig) | ADR 0017 | *Your kennel, your keys.* |
| **Leash** | Zodiac Roles: router smije pozvati samo `EURe.transfer` | ADR 0017 | *A dog on a short leash: one trick, nothing else.* |
| **Guard** | fail-closed whitelist i binding | `tenants/whitelist.ts` | *Strangers don't get the stick.* |
| **Bark** | potpisani webhook | `intents/outbound.ts` | *It barks when money arrives. Twice: received, then paid.* |
| **Ears up** | SSE „zaprimljeno" 0 s od placedAt | ADR 0018 | *Ears up in 5 seconds. Settled in 12.* |
| **Sniff** | stray resolver: uplata bez reference se poveže po iznosu i vremenu | ADR 0018 | *Lost the tag? We sniff out the owner.* |
| **Lost & found** | parkirana uplata koju operater preusmjeri | ADR 0018 | *If we're not sure, we wait. We never guess with money.* |
| **Good boy** | intent `paid` | `intents/stage.ts` | — (stanje u UI-ju, ikona) |
| **Heel** | tenant jednom transakcijom isključi modul | ADR 0017 | *One signature and the dog sits. Your call, not ours.* |
| **Watchdog** | detektor odljeva sa Safea | ADR 0019 | *A watchdog that counts every bone that leaves the yard.* |
| **Pack** | kvorum telefona kao potpisnici (plan) | ADR 0019 | ⚠ plan, ne koristiti u copyju |
| **Leash (proizvod)** | pretplate i recurring allowance (plan) | — | ⚠ plan |
| **Kennel (proizvod)** | self-host, MIT | `LICENSE` | *Run your own kennel. MIT.* |

## Ton

- **RevenueDog:** pas službenik, retriever koji donosi. Ozbiljan, vjeran, pouzdan. Ton je
  „Labrador u uniformi".
- **RevenueDOGE:** shiba s podignutom obrvom. Unutarnji monolog na internetskom doge
  jeziku, bez gramatike, samo kao uskličnik u zajednici, nikad u dokumentaciji:

  > such settle · very non-custodial · wow 12 seconds · much 0 € fees

## Gdje pas staje

- **Nikad uz regulatorne tvrdnje.** U rečenici o Moneriumu, licenci, KYB-u ili žigu nema
  psa.
- **Nikad u kartici statusa ni ugovoru.**
- **Nikad „pas čuva vaš novac".** Pas ne čuva novac nego ga donosi. Novac čuva trgovčev
  vlastiti račun, a to razlikovanje je cijela poanta non-custodiala.
