---
tip: pojam
aliases: [security requirement, zahtev]
izvor: NIST SP 800-192, Verification and Test Methods for Access Control Policies/Models (pojam security policy: "the statement of required protection for the information objects"), https://csrc.nist.gov/glossary/term/security_policy
---
# Bezbednosni zahtev (security requirement)

## Definicija
Bezbednosni zahtev je pravilo koje za određeni [[Resurs|resurs]] utvrđuje ko sme, a ko mora moći da izvrši koje radnje nad njim. Svaki bezbednosni zahtev konkretizuje neko [[Bezbednosno svojstvo|bezbednosno svojstvo]] tog resursa.

## Primer
Bezbednosni zahtevi za zdravstveni karton pacijenta u Klinici Sana:

| Svojstvo | Bezbednosni zahtev |
|---|---|
| Poverljivost | Karton smeju da vide samo pacijent i lekari koji ga leče. |
| Integritet | Dijagnozu i terapiju sme da menja samo lekar koji leči pacijenta. |
| Dostupnost | Lekar mora moći da otvori karton pacijenta tokom pregleda. |
| Neporecivost | Svaka izmena terapije mora se moći pripisati lekaru koji ju je izvršio. |

Zahtev važi gde god se karton nalazi. Linija koda koja upisuje podatke iz kartona u aplikativni log koji čitaju i administratori omogućava radnju suprotnu zahtevu poverljivosti, iako autor koda taj zahtev nije imao u vidu.

## Napomene
Bezbednosni zahtev kaže šta mora da važi za resurs, a ne kojim mehanizmom se to postiže. „Sistem koristi višefaktorsku autentifikaciju“ nije bezbednosni zahtev, nego [[Bezbednosna kontrola|bezbednosna kontrola]].

Većina bezbednosnih zahteva u organizaciji nije zapisana, ali ipak važi. Deo modelovanja pretnji je da se takvi zahtevi učine eksplicitnim.
