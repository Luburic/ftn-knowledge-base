---
tip: kontekst
uloga: primarni
---
# Klinika Sana

Klinika Sana je privatna zdravstvena ustanova sa više ordinacija. Pacijentima nudi preglede, laboratorijske analize i online zakazivanje, a zdravstvenu dokumentaciju vodi elektronski. Pogodna je za ilustraciju modelovanja pretnji jer obrađuje osetljive podatke, ima i poslovni i softverski sloj i zavisi od više spoljnih subjekata.

## Elementi

### Sistemi
- **Portal za pacijente**: veb aplikacija za online zakazivanje pregleda i uvid u nalaze.
- **Sistem elektronskih kartona**: interni sistem u kom lekari i medicinske sestre vode zdravstvenu dokumentaciju pacijenata. Svaku izmenu kartona beleži u dnevnik izmena (audit log) sa nalogom korisnika i vremenom izmene. Baza sistema se svakodnevno kopira u sistem za rezervne kopije.
- **Laboratorijski sistem**: prima uputnice i vraća rezultate analiza u elektronski karton preko integracije sa sistemom elektronskih kartona.
- **Integracija sa RFZO**: razmena podataka o osiguranju i uslugama sa Republičkim fondom za zdravstveno osiguranje.
- **Integracija sa platnim procesorom**: naplata usluga karticom preko portala i na recepciji.
- **Kancelarijska IT infrastruktura**: e-pošta, Active Directory za naloge zaposlenih i VPN za udaljeni pristup lekara i spoljnog dobavljača održavanja.

### Podaci
- Zdravstveni kartoni (dijagnoze, terapije, nalazi)
- Lični podaci pacijenata
- Podaci o plaćanju
- Kredencijali zaposlenih

### Ljudi i uloge
- Pacijent
- Lekar
- Medicinska sestra
- Recepcija
- Administrator
- Spoljni dobavljač održavanja

### Spoljni subjekti
- Osiguravajuća društva
- Laboratorije partneri
- Regulator (nadzor primene Zakona o zaštiti podataka o ličnosti)
