# Izvori

## Istina o mehanizmu (`~/git/domovinatv/pay.domovina.ai`, javno, MIT)

| Što | Gdje |
|---|---|
| Intent API, granice, odgovori | `backend/src/intents/api.ts` |
| Faze statusa i `custodian` | `backend/src/intents/stage.ts` |
| Webhook događaji | `backend/src/intents/outbound.ts` |
| Potpis i retry outbox | `backend/src/intents/outbox.ts` |
| SSE | `backend/src/intents/stream.ts` |
| Parser reference | `backend/src/monerium/sid.ts` |
| Forward (Roles) | `backend/src/router/safe.ts` |
| Whitelist, fail-closed | `backend/src/tenants/whitelist.ts` |
| Tenant ključevi | `backend/src/tenants/auth.ts` |
| Flagovi | `backend/wrangler.toml` |
| Payout whitelist i tenant model | `docs/decisions/0016-tenant-payout-whitelist.md` |
| Multi-tenant rail | `docs/decisions/0017-multi-tenant-rail.md` |
| Stray resolver i rano „zaprimljeno" | `docs/decisions/0018-stray-payment-resolver.md` |
| Detektor odljeva i off-cloud potpisnik | `docs/decisions/0019-off-cloud-forward-signer.md` |
| Hrvatski IBAN listener | `docs/decisions/0020-hr-iban-listener-bez-minta.md` |
| Monerium ugovor | `docs/monerium-private.md` |
| Izmjerene brojke Moneriuma | `docs/research/2026-09-monerium-first-iban-screening.md` |
| Vizija intenata | `docs/product-vision/payment-intents-and-sse.md` |
| Regulatorni okvir | `docs/compliance/README.md` |

## Landing (`~/git/domovinatv/mpt-landing`, javno)

- `CLAUDE.md`: pozicioniranje, cijene, struktura sitea
- `src/lib/mpt-pricing.ts`: SSOT cjenika
- `src/lib/market-fees.ts`: naknade kartica i SEPA (izvor je analiza isplativosti)
- `docs/revenuedog.md`: prva razrada 10. 10. 2026. (opcije A/B/C, gap analiza)
- `docs/2026-10-10-revenuecat-benchmark.md`: što je od RevenueCata preuzeto, a što odbačeno

## Lipanjski plan (privatno, ne citirati izvan sažetka)

- `/Volumes/DOMOVINA2TB/git/RevenueDog/brief/HANDOFF.md` i `README.md` (commit `3918dcf`,
  bez remotea)
- `~/git/domovinatv/ecosystem-brain/_global/STRATEGIJA-WALLET-EKOSUSTAVA.md` §1, §3, §8–§10.
  Putanja briefa u njoj (`~/git/RevenueDog/brief/`) je zastarjela.

## Vanjski izvori (11. 10. 2026.)

- RevenueCat: revenuecat.com, /state-of-subscription-apps/,
  /blog/company/revenuecat-virtual-currency, /blog/company/introducing-revenuecat-billing
- žig: trademarks.justia.com/owners/revenuecat-inc-5136281
- Stripe stablecoin subscriptions: stripe.com/blog/introducing-stablecoin-payments-for-subscriptions
- Base recurring: docs.base.org/base-account/guides/accept-recurring-payments
- Coinbase Commerce: moonpay.com/newsroom/coinbase-commerce-shutdown-guide-for-merchants
  (izvor je konkurent)
- EURe: monerium.com/assets/whitepapers/monerium-eure-whitepaper.xhtml,
  defillama.com/rwa/asset/EURe
- Instant Payments Regulation:
  ecb.europa.eu/paym/retail/instant_payments/html/instant_payments_regulation.da.html
- Digitalni euro: sumsub.com/media/news/digital-euro-proposal-advances-to-final-eu-negotiations/
- Imena: `gh search repos revenuedog`, whois/RDAP (11. 10. 2026.)

**Nije provjereno:**

- vlasnici `revenuedog.com` i `revenue.dog`
- EUIPO žigovi
- vijesti o Moneriumu 2025.–2026.
- trakcija Spherea, Loopa i Requesta
