---
tip: pojam
aliases: [vulnerability]
izvor: Krsul, I. V., Software Vulnerability Analysis, doktorska disertacija, Purdue University, 1998 (COAST TR 98-09), https://www.cerias.purdue.edu/assets/pdf/bibtex_archive/98-09.pdf
---
# Ranjivost (vulnerability)

## Definicija
Ranjivost je osobina [[Komponenta sistema|komponente sistema]] zbog koje komponenta omogućava radnju suprotnu nekom [[Bezbednosni zahtev|bezbednosnom zahtevu]], a kojom [[Napadač|napadač]] može da ostvari [[Pretnja|pretnju]]. Nastaje u dizajnu, implementaciji, konfiguraciji ili načinu upotrebe komponente.

## Primer
| Slučaj u Klinici Sana | Ranjivost? | Zašto |
|---|---|---|
| Sistem elektronskih kartona upisuje podatke iz kartona u aplikativni log koji čitaju i administratori bez prava da vide kartone | da | omogućava čitanje kartona suprotno zahtevu poverljivosti |
| Isti aplikativni log čitaju samo lekari koji ionako smeju da vide te kartone | ne | ne omogućava nijednu radnju suprotnu zahtevu |
| Politika lozinki za naloge zaposlenih u Active Directory-ju dozvoljava kratke lozinke koje se lako pogađaju | da | omogućava prijavu pod tuđim nalogom |
| Lekar otvara priloge iz e-pošte bez provere pošiljaoca | da | omogućava izvršavanje tuđeg koda na računaru klinike |
| Portal za pacijente je javno dostupan na internetu | ne | klinika to dozvoljava |
| Greška u delu koda portala do kog napadač ne može da dođe | ne | ne omogućava nijednu radnju |

## Napomene
Ranjivost nije linija koda ili podešavanje, nego mogućnost koju oni stvaraju u datom sistemu. Ista linija može biti ranjivost u jednom sistemu, a u drugom ne. Ranjivost ne mora biti na komponenti na kojoj se svojstvo narušava, jer napad može koristiti ranjivosti više komponenti na putu do resursa.
