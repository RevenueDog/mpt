# 03 · RevenueCat ↔ RevenueDog, pojam po pojam

Legenda: ✓ postoji u MPT-u · ◐ djelomično · ✗ ne postoji

| RevenueCat pojam | RevenueDog ekvivalent | Stanje |
|---|---|---|
| **Project / App** (developer spaja svoj App Store / Play račun) | **Tenant**: trgovac spaja svoj Monerium račun, Safe i listu isplata | ◐ kod postoji, isključen flagom |
| **Store** (App Store, Play, Stripe) | **Rail**: SEPA → Monerium EURe danas; wallet transfer sutra | ◐ jedan rail |
| **Purchase / Transaction** | **Intent** (`pending → paid → expired`) | ✓ |
| **Receipt validation** | provjera Monerium naloga (placed → processed) i onchain potvrda forwarda | ✓ |
| **Restore purchases** | **stray resolver**: uplata bez reference, povezana po iznosu i vremenu | ✓ |
| **Webhooks** | `payment.received`, `intent.paid`, `payment.underpaid`, `payment.late`, `payment.rejected`, `forward.blocked`, `contribution.sepa` | ✓ |
| **CustomerInfo listener** (SDK obavijesti) | SSE `/api/intents/:sid/stream` | ✓ |
| **Hosted paywall / Web Purchase Link** | hostani checkout `/checkout/:sid` (QR i status uživo) | ◐ checkout bez paywall logike |
| **Products** | `amount_eur` + `label` po intentu | ◐ nema kataloga |
| **Entitlements** (`entitlements["pro"].isActive`) | ✗; stanje intenta postoji, model prava pristupa ne | ✗ |
| **Offerings / Packages** (remote config) | ✗ | ✗ |
| **Paywalls** (remote UI) | ✗ | ✗ |
| **Subscriptions** (auto-renew, grace, billing retry) | ✗; vidi Leash u [09](09-roadmap.md) | ✗ |
| **Refunds** | ✗; SEPA recall nije automatiziran | ✗ |
| **SDK-ovi** (iOS, Android, RN, Flutter, JS) | ✗; REST + EPC QR. Prvi kandidat je fork `purchases-js` (MIT) | ✗ |
| **Dashboard / Charts** (MRR, churn) | ✗; postoji samo operaterski admin | ✗ |
| **Integracije** (Amplitude, Segment…) | Shopify app napravljen, nedeployan | ◐ |
| **Fraud / abuse** | binding, whitelist, fail-closed, detektor odljeva | ✓ (i više od RC-a, jer se ovdje radi o novcu) |
| **Pricing**: free do $2,5K MTR, zatim 1 % | free do 2.500 € mjesečno, zatim 1 % (`mpt-landing/src/lib/mpt-pricing.ts`) | ✓ objavljeno, naplata još ne postoji |
| **Open source** (SDK-ovi MIT, backend zatvoren) | **cijeli backend MIT**, može se samostalno hostati | ✓ i otvorenije od RC-a |

## Što MPT ima, a RevenueCat nema

- **Cijeli backend je otvoren.** Tko ne želi hostani servis, pokrene vlastiti.
- **Tenant može isključiti orkestrator jednom transakcijom.** Kod RC-a se to radi
  migracijom, ovdje jednim potpisom.
- **Status pokazuje tko u svakom trenutku drži novac** (`custodian` u svakom koraku).
- **Uplata bez wallet-a.** Kupac ne instalira ništa i ne zna da postoji blockchain.

## Najveća rupa

RevenueCat developeri **čitaju ime kao pretplate i entitlemente**. MPT danas radi
jednokratna plaćanja. Svaki globalni launch prije recurring primitiva je obećanje bez
proizvoda.

Postoje dva načina da se to zatvori:

1. **Iskreno:** pozicionirati prvi modul kao *checkout*, ne kao *subscriptions* („RevenueDog
   Fetch"), a pretplate najaviti kao sljedeći modul.
2. **Proizvodno:** napraviti recurring spike (Safe modul s allowanceom ili spend permission
   na EURe). Vidi [09](09-roadmap.md).
