---
tip: pojam
aliases: [attack]
izvor: NIST SP 800-30 Rev. 1, Guide for Conducting Risk Assessments (pojam attack, preuzet iz CNSSI 4009-2022), https://csrc.nist.gov/glossary/term/attack
---
# Napad (attack)

## Definicija
Napad je niz radnji koje [[Napadač|napadač]] izvodi ili navodi druge da izvedu, u pokušaju da ostvari jednu ili više [[Pretnja po komponenti|pretnji po komponenti]]. U tom nizu napadač po potrebi iskorišćava [[Ranjivost|ranjivosti]] komponenti sistema da bi stekao mogućnosti koje nema, kao što su pristup komponenti ili ovlašćenja tuđeg naloga, dok ne bude u stanju da naruši [[Bezbednosno svojstvo|bezbednosno svojstvo]] ciljnog resursa.

## Primer
Napad ransomware grupe na Kliniku Sana:

| # | Radnja | Uloga |
|---|---|---|
| 1 | Napadač iz javnih izvora saznaje adrese e-pošte lekara | priprema |
| 2 | Šalje lekaru poruku sa zlonamernim prilogom | priprema |
| 3 | Lekar otvara prilog bez provere pošiljaoca i zlonamerni softver se pokreće | iskorišćavanje ranjivosti; napadač stiče izvršavanje koda na lekarovom računaru |
| 4 | Napadač pogađa lozinku administratorskog naloga u Active Directory-ju, jer politika lozinki dozvoljava kratke lozinke | iskorišćavanje ranjivosti; napadač stiče administratorska ovlašćenja |
| 5 | Prijavljuje se kao administrator na server baze sistema elektronskih kartona | korišćenje stečenih ovlašćenja |
| 6 | Šifruje bazu | narušavanje dostupnosti kartona i rezultata analiza u bazi |

Napad ostvaruje dve pretnje po komponenti: narušavanje dostupnosti kartona i narušavanje dostupnosti rezultata analiza u bazi sistema elektronskih kartona. Da lekar nije otvorio prilog, napad bi se ipak desio, ali ne bi uspeo.

Lekar koji legitimno vidi karton pacijenta kog leči, pa ga proda novinaru, takođe izvodi napad. Njegov napad nema nijedan korak iskorišćavanja ranjivosti, jer lekar od početka ima sve mogućnosti potrebne da naruši poverljivost kartona.

## Napomene
Napad je pokušaj, pa postoji i kada ne uspe. [[Pretnja]] kaže koje svojstvo kog resursa napadač želi da naruši, a napad kako to pokušava. Jedan napad može ostvariti više pretnji po komponenti, a jedna pretnja po komponenti se može ostvariti različitim napadima.

Iskorišćavanje ranjivosti po pravilu ne narušava svojstvo direktno, već napadaču daje novu mogućnost. Broj takvih koraka zavisi od toga koliko su početne mogućnosti napadača udaljene od onih koje su mu potrebne.
