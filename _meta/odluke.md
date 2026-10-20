---
tip: odluke
---
# Odluke

## Pretpostavljeni pojmovi
Pojmovi koje publika zna bez definisanja. Ne otvaraju se ponovo osim na zahtev studenta.

- Razvoj softvera
- Aplikacija
- Baza podataka
- Računarska mreža
- Klijent, server
- API
- Sistem (u opštem smislu; obuhvat poslovanja nosi pojam resursa)
- Organizacija
- Ovlašćenje (autorizacija)

## Odluke o obuhvatu
- Pretnja se definiše usko: obuhvata samo namerne radnje malicioznog napadača. Nenamerni događaji (greške, kvarovi, nepogode) nisu pretnje u ovoj bazi.
- Pretnja i napadač su odvojeni pojmovi. Pretnja je događaj, napadač je onaj ko ga izaziva.
- Napadač je definisan preko motivacije: narušavanje bezbednosnih svojstava je sredstvo, a ne cilj. Ko narušava svojstvo kao sporednu posledicu (npr. iz pogodnosti), nije napadač; VERIS motiv convenience je namerno izostavljen.
- Pretnja ima dva nivoa: pretnja (napadač, resurs, svojstvo) i pretnja po komponenti (pretnja ograničena na jednu komponentu sistema). Veza je 1:N. Napad se vezuje za pretnju po komponenti (M:N) i iskorišćava ranjivost komponente.
- Resurs je širok: obuhvata podatke, sisteme, poslovne procese, ljude i reputaciju.
- Bezbednosna kontrola je definisana preko sloja 1 i komponente sistema, bez sloja 2 i bez rizika. Određuje se po dejstvu na svojstva, ne po uzroku narušavanja, pa obuhvata i mere protiv kvarova. Otklanjanje ranjivosti (npr. zakrpa) takođe je kontrola. Osiguranje nije kontrola.
- Privatnost nije posebno bezbednosno svojstvo. Posledice po lične podatke izražavaju se kroz poverljivost i uticaj; osetljivost podataka određuje veličinu uticaja, a ne posebno svojstvo.

## Terminologija
- Asset se prevodi kao Resurs, ne kao imovina. "Imovina" ostaje alias radi pretrage.
- Lokacija resursa se zove komponenta sistema (ne podržavajući resurs, ne stanje podataka). Konkretni nivo pretnje se zove pretnja po komponenti.
- Security requirement se prevodi kao bezbednosni zahtev. Zahtev kaže šta mora da važi za resurs, ne kojim mehanizmom. Termin "bezbednosna politika" se ne koristi za pojedinačna pravila, jer u praksi označava organizacioni dokument; ako zatreba, politika je skup zahteva.
- Security control se prevodi kao bezbednosna kontrola; "mera zaštite" (termin Zakona o informacionoj bezbednosti) je alias. "Mitigacija" nije sinonim za kontrolu, nego je rezervisana za opciju postupanja sa rizikom u sloju 3.
- Threat actor / adversary / attacker se prevodi kao Napadač. "Akter pretnje" se ne koristi kao termin, ostaje alias.

## Redosled rada
1. Šta štitimo: resurs, bezbednosno svojstvo, bezbednosni zahtev
2. Šta može poći naopako: napadač, pretnja, komponenta sistema, pretnja po komponenti, ranjivost, napad
3. Šta preduzimamo: bezbednosna kontrola (definisana unapred), uticaj, verovatnoća, rizik, postupanje sa rizikom (mitigacija, prenos, izbegavanje, prihvatanje)
4. Kako opisujemo sistem: granica poverenja, površina napada, vektor napada, elementi modela sistema (komponenta sistema je izvučena u sloj 2, u obliku nezavisnom od metode)

## Promene konvencija
- Bezbednosna kontrola je definisana pre ostatka sloja 3, na zahtev studenta, jer ne zavisi od uticaja, verovatnoće ni rizika.
- Uticaj je premešten iz sloja 2 u sloj 3, jer služi prioritizaciji, a ne identifikaciji. Verovatnoća je izdvojena kao poseban pojam sloja 3.
- Bezbednosni zahtev je dodat u sloj 1, posle bezbednosnog svojstva. Ranjivost je definisana preko bezbednosnog zahteva (komponenta omogućava radnju suprotnu zahtevu), a ne preko pojma "slabost".
- "Nedozvoljene radnje" u definiciji bezbednosnog svojstva namerno ostaju neformalne i ne linkuju bezbednosni zahtev, da bi se izbegao ciklus svojstvo -> zahtev -> svojstvo.
- Redosled rada je promenjen: komponenta sistema je izvučena iz sloja 4 u sloj 2, jer je potrebna za definisanje pretnje po komponenti, ranjivosti i napada.
- Autentičnost je izostavljena iz nabrajanja u definiciji bezbednosnog svojstva (može se uvesti kasnije, npr. uz STRIDE).
- Privatnost je privremeno bila uvedena kao bezbednosno svojstvo, pa je izbačena (vidi odluke o obuhvatu).

## Otvorena pitanja
- Zloupotreba svrhe od strane ovlašćenog insajdera (npr. recepcija koristi telefone pacijenata za privatni posao) nije pokrivena nijednim svojstvom. Ako postane važna, proširiti definiciju poverljivosti ("nisu dostupne, otkrivene niti korišćene"), a ne vraćati privatnost.
- Podatak o ličnosti verovatno treba definisati uz pojam uticaja.
- Motivacija napadača je za sada deo definicije napadača. Izdvojiti u posebnu belešku ako zatreba (profil napadača, verovatnoća), pazeći na ciklus Napadač -> Motivacija -> Napadač.
- Vektor napada je odložen za sloj 4. Termin ima više značenja (ulazni kanal, CVSS Attack Vector, deo putanje do ranjivosti) i pretpostavlja granicu poverenja i površinu napada. Radna ideja: put kojim napadač prelazi granicu poverenja do prve komponente.
- "Mogućnost" napadača (pristup, izvršavanje koda, ovlašćenja) i njegova početna pozicija koriste se u definiciji napada bez posebne beleške. Kandidati za definisanje uz putanje napada ili sloj 4.
- Korak i tehnika napada (npr. MITRE ATT&CK taktike) i iskorišćavanje ranjivosti kao posebna beleška odloženi su do izbora metode.
- Bezbednosni incident (uspešan napad) verovatno treba uz pojam uticaja; Zakon o informacionoj bezbednosti koristi pojam incidenta.
- Sloj 4 (opis sistema) je odložen dok se ne izabere metoda, jer zavisi od nje (npr. DFD).
