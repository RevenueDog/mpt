# 07 · Tržište (istraženo 11. 10. 2026.)

## RevenueCat danas

- **Što radi:** subscription backend za iOS, Android i web. SDK-ovi su MIT (provjereno:
  `purchases-ios`, `-android`, `-flutter`, `-js`, `-kmp`, `react-native-purchases`), a
  backend je zatvoren.
- **Cijena:** besplatno do $2.500 MTR, zatim 1 % (na bruto prihod, prije Apple/Google
  reza).
- **Financiranje:** Series C od $50M u svibnju 2025. (Bain Capital Ventures), uz valuaciju
  oko $500M. Ukupno su podigli $102–120M, ovisno o izvoru.
- **Skala:** State of Subscription Apps 2026 obuhvaća 115.000+ aplikacija i više od $16B
  prihoda.
- **Web:** Web Billing (Stripe), Web Paywalls i Purchase Links. Od travnja 2026. nude i
  merchant-of-record preko Stripe Managed Payments.
- **Kripto:** **ne.** U objavi o virtualnim valutama kažu da se ne pivotiraju u kripto, a
  zahtjev iz zajednice iz 2022. nikad nije realiziran.
- **Žig:** RevenueCat, Inc. drži „REVENUECAT" u SAD-u (razredi 9 i 42).

Izvori: revenuecat.com, revenuecat.com/blog/company/revenuecat-virtual-currency,
trademarks.justia.com/owners/revenuecat-inc-5136281.

## Konkurencija

| Igrač | Što | Recurring | Skrbništvo nad novcem | Fokus |
|---|---|---|---|---|
| Stripe stablecoin subscriptions (listopad 2025.) | USDC preko smart-wallet mandata | da | Stripe konvertira i isplaćuje USD (posrednik) | SAD |
| Stripe / Bridge / Tempo | infrastruktura za izdavanje stablecoina i L1 | — | custodial | SAD |
| Coinbase Base Pay / Spend Permissions | `subscribe/charge/revoke`, USDC na Baseu | da | non-custodial | wallet-first |
| Coinbase Commerce | self-custody zatvoren izvan SAD-a i Singapura 31. 3. 2026. | — | — | **EU mjesto ostalo prazno** |
| Loop Crypto | ERC-20 allowance autopay | da | non-custodial | wallet-first |
| Sphere | recurring na Solani | da | approval-based | wallet-first |
| Superfluid | streamovi po sekundi | stream | non-custodial | protokol |
| Request Network | onchain računi i recurring | da | non-custodial | wallet-first |
| MoonPay Commerce (ex-Helio) | checkout i pretplate | da | mješovito | Solana |
| Confirmo Subscribe (srpanj 2026.) | USDC/USDG pretplate | da | procesor | EU (CZ) |
| **Monerium** | izdavatelj EURe, IBAN ↔ wallet | ne | regulirani EMI | **naš rail, nije konkurent** |

**Praznina:** svi su wallet-first, a većinom i USDC/SAD. Nitko ne radi *bank-first + EUR +
novac izravno na trgovčev regulirani račun + multi-tenant + MIT*. Nijedna financirana
tvrtka ne koristi frazu „RevenueCat for crypto".

## EU vjetar u leđa

- **MiCA:** Monerium je islandski EMI s passportom u EEA. Bijeli papir za EURe notificiran
  je 1. 7. 2025. EURe je na Ethereumu, Gnosisu, Arbitrumu, Polygonu i drugim lancima.
  Tržišna kapitalizacija je oko $32M, otprilike dvije trećine na Gnosisu. To je malo u
  odnosu na EURC, pa je ovisnost o jednom izdavatelju rizik.
- **Instant Payments Regulation:**
  - od 9. 10. 2025. banke u eurozoni moraju nuditi slanje SEPA Instant po cijeni običnog
    naloga
  - Verification of Payee je obavezan, pa kupac vidi ime trgovca prije slanja
  - države EU-a izvan eurozone uvode to do 9. 7. 2027.
- **Digitalni euro:** Parlament je 9. 7. 2026. otvorio trilog (416–169). Ako zakon prođe,
  piloti su od 2027., a izdavanje možda 2029. To je politički vjetar za europska A2A
  plaćanja, a dugoročno i konkurent.

## Što iz ovoga slijedi

1. **Bank-first je wedge koji nitko ne drži.** Pretplate su gužva (Stripe, Coinbase, Loop,
   Sphere). Jednokratni bank → merchant checkout u eurima nije.
2. **Recurring nije nužno prvi.** Lipanjski brief kaže da je recurring core IP. Tržište
   kaže da je recurring komoditiziran (Spend Permissions su besplatni), a bank-first EUR nije.
3. **Ovisnost o Moneriumu je i snaga i rizik.** Snaga je regulacija bez vlastite licence;
   rizik je jedan EMI i mali EURe.
