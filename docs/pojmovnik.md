# Pojmovnik

| Pojam | Značenje |
|---|---|
| **MPT** | Mint Pay Transfer: orkestrator SEPA → EURe uplata; ujedno prefiks reference `mpt:` |
| **Intent** | jedna očekivana uplata: iznos, cilj, TTL; stanja `pending → paid → expired` |
| **sid** | ID intenta (6–32 znaka) koji putuje u SEPA referenci; SEPA mijenja `=` u `.`, a parser to tolerira |
| **Referenca / tag** | `mpt:0x<adresa trgovca>?sid=<sid>`; `cmp:0x<safe>?id=<id>` za trajni QR kampanje |
| **Tenant** | pravna osoba s vlastitim Monerium KYB-om, IBAN-om, Safeom i listom isplata |
| **Monerium** | EMI (islandska licenca, passport u EEA) koji izdaje EURe i daje IBAN |
| **EURe** | euro e-money token (MiCA EMT) koji izdaje Monerium; ovdje na Gnosis Chainu |
| **Safe** | multisig pametni ugovor; tenantov prihvatni „kennel" |
| **Zodiac Roles** | modul na Safeu koji routeru dopušta točno jednu akciju (`EURe.transfer`) |
| **Router** | ključ koji izvršava forward i plaća gas (za hostane tenante gas puni MPT) |
| **Forward** | prijenos EURe s prihvatnog Safea na trgovčevu odobrenu adresu |
| **Whitelist** | odobrene adrese za isplatu po tenantu; provjera je fail-closed |
| **Binding** | adresa u referenci mora biti jednaka adresi intenta stvorenog preko API-ja |
| **Stray resolver** | povezivanje uplate bez reference s intentom po točnom iznosu i vremenu |
| **Parkirano** | uplata koja nije prošla provjeru; čeka operatera, ništa se ne šalje |
| **SSE** | Server-Sent Events; status uživo za checkout |
| **Standard Webhooks** | shema potpisa webhooka (`webhook-id`, `webhook-timestamp`, `webhook-signature`) |
| **EPC QR / HUB3** | europski SEPA QR i hrvatski PDF417 barkod za uplatnicu |
| **Non-custodial software provider** | ITalkova pozicija: softver, bez držanja novca; regulirani dio radi Monerium |
| **MTR** | Monthly Tracked Revenue (RevenueCat); kod nas mjesečni promet uplata sa statusom `paid` |
| **airKUNA** | rail i regulatorni brend ekosustava (sloj 1) |
| **RevenueDog / RevenueDOGE** | globalni dev brend / meme i community brend; vidi [04](04-arhitektura-brenda.md) |
