# 06 · Poruke i copy

> Svaka rečenica mora proći statusnu tablicu u [02](02-proizvod-danas.md#status). Brojke
> su izmjerene u produkciji (ADR 0017/0018).

## Taglinei

**RevenueDog (ozbiljno):**

- **We fetch. We don't keep.**
- RevenueCat for bank payments. Money goes straight to you.
- Bank transfer in. Stablecoin out. Nobody in the middle.
- The payment rail that never holds your money.
- Card-like checkout on SEPA. Without the card fee.

**RevenueDOGE (zajednica):**

- Much settle. Very non-custodial. Wow.
- The Department of Getting Paid Efficiently.
- DOGE cut government waste. We cut payment waste.
- Direct-to-Owner Gross Earnings.
- Cat holds the state. Doge fetches the money.

## Pitch u jednoj rečenici

- **EN:** RevenueDog lets any European customer pay a merchant straight from their bank.
  The money settles as regulated euro stablecoin on the merchant's own account in about
  12 seconds, and we never touch it.
- **HR:** Kupac plaća iz bilo koje europske banke, a novac za oko 12 sekundi stiže kao
  regulirani euro stablecoin na trgovčev vlastiti račun. Mi ga nikad ne dodirujemo.

## Elevator pitch (30 sekundi, EN)

> RevenueCat proved that developers will pay 1% for someone to handle the messy state of
> payments, even though Apple and Google do the actual money moving. We do the same for
> bank payments in Europe.
>
> Your customer scans a QR and pays from their bank. The transfer carries a tag that says
> who the money belongs to. A regulated issuer, Monerium, mints euro stablecoin on *your*
> account, and our rail fetches it to your approved address. You get a signed webhook in
> seconds.
>
> We never hold the money. You can switch us off with one signature, and the whole
> backend is MIT. Free up to €2,500 a month, then 1%.

## Struktura naslovnice (RevenueCat uzorak)

1. **Hero:** „We fetch. We don't keep." Podnaslov: RevenueCat for bank payments → EURe.
   CTA: „Request integration".
2. **Tri broja koja su stvarno izmjerena:**
   - **5 s** do „received"
   - **12 s** do „paid"
   - **0 €** za kupca na Revolut putu

   Nikad ne pisati izmišljeni volumen.
3. **Kako radi**, u četiri pseća koraka: Tag → Fetch → Bark → Good boy (dijagram iz
   [02](02-proizvod-danas.md)).
4. **„Your kennel, your keys":** tenant model i isključivanje jednim potpisom.
5. **Kod:** `POST /api/intents` i `intent.paid` webhook.
6. **Cijene:** jedna rečenica, kao RevenueCat.
7. **Što jesmo, a što nismo:** non-custodial, nismo licencirana platna usluga, Monerium radi
   regulirani dio.
8. **Open source:** „Run your own kennel."

## Nacrt X launch threada (RevenueDOGE)

> Status: nacrt. Objavljuje se tek nakon odluke iz [04](04-arhitektura-brenda.md) i nakon
> prvog vanjskog tenanta. Bez Muska i bez doge.gov taggiranja; ako primijete, to je bonus,
> a ne plan.

1. RevenueCat holds the state of in-app purchases. It never holds the money. 🐱
   We built the same thing for bank payments in Europe. 🐶 **RevenueDOGE.**
2. Your customer pays from any EU bank. No wallet, no app, no crypto. Just a QR.
3. The transfer wears a tag: `mpt:0x<you>?sid=<order>`. A regulated issuer mints euro
   stablecoin on *your* account. We fetch it to *your* address. 12 seconds.
4. We never hold it. One signature from you and we're off the leash.
5. Revolut started stripping payment references in October. So we taught the dog to sniff:
   same amount, same minute → same owner. First one settled in 12 s.
6. Card fee on €50: €1.00. On RevenueDOGE: €0 up to €2,500/month. Such efficiency.
7. Whole backend is MIT. Run your own kennel → github.com/…

## FAQ s psećim šlagvortom

- **„Do you hold my money?"** No. We fetch, we don't keep. Funds land on your own Monerium
  account and Safe.
- **„What if the customer forgets the reference?"** We sniff out the owner by exact amount
  and time. If we're not sure, it waits in lost & found until a human decides.
- **„Can you run off with it?"** Our router is on a leash that allows one action:
  `EURe.transfer`, to addresses you approved, checked fail-closed. And you can revoke it
  with one signature.
- **„Is this crypto?"** For your customer, no. It's a bank transfer. For you, the money
  arrives as EURe, a regulated euro e-money token, which you can redeem back to your bank.

## Zabranjene rečenice

| Ne pisati | Zašto |
|---|---|
| „Subscriptions", „entitlements" kao postojeće | ne postoje |
| „0 € from any bank" | samo na Revolut putu |
| „Can't be paid twice" | ponovljena uplata s istom referencom se ponovno forwarda |
| „Restricted onchain to merchant addresses" | prije toga provjeriti ADR 0016 u pay.domovina.ai |
| „We pay out merchants" / „licensed" | nismo platna usluga; regulirani dio radi Monerium |
| „Trusted by X merchants", volumen | danas je ITalk jedini aktivni tenant |
| Bilo što o Musku, doge.gov ili politici | zid |
