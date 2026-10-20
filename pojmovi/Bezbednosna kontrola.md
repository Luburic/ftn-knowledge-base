---
tip: pojam
aliases: [security control, mera zaštite, kontrola]
izvor: NIST SP 800-53 Rev. 5, Security and Privacy Controls for Information Systems and Organizations (pojam security control); podela po dejstvu i prirodi prema ISO/IEC 27002:2022, https://csrc.nist.gov/glossary/term/security_control
---
# Bezbednosna kontrola (security control)

## Definicija
Bezbednosna kontrola je mera ugrađena u [[Komponenta sistema|komponentu sistema]] ili uvedena kao nova komponenta, kojom organizacija sprečava, otkriva ili ispravlja narušavanje [[Bezbednosno svojstvo|bezbednosnih svojstava]] [[Resurs|resursa]]. Može biti tehnička, organizaciona, kadrovska ili fizička.

## Primer
| Kontrola u Klinici Sana | Komponenta | Dejstvo | Priroda |
|---|---|---|---|
| Višefaktorska autentifikacija za VPN nalog spoljnog dobavljača održavanja | VPN | preventivna | tehnička |
| Obuka lekara za prepoznavanje zlonamernih poruka | lekar | preventivna | kadrovska |
| Pravilo da zaposleni ne dele lozinke | svi zaposleni | preventivna | organizaciona |
| Dnevnik izmena u sistemu elektronskih kartona | sistem elektronskih kartona | detektivna | tehnička |
| Svakodnevne rezervne kopije baze sistema elektronskih kartona | nova komponenta: sistem za rezervne kopije | korektivna | tehnička |

Osiguranje od sajber rizika nije bezbednosna kontrola. Ono ne štiti nijedno svojstvo, nego klinici nadoknađuje finansijsku štetu.

## Napomene
Kontrola deluje na [[Ranjivost|ranjivosti]] i [[Napad|napade]], ali ne i na [[Pretnja|pretnju]]. Preventivna kontrola otklanja ranjivost ili prekida napad, detektivna otkriva napad, a korektivna vraća narušeno svojstvo. Pretnja ostaje, jer napadač i njegova namera ne zavise od kontrola.

Kontrola se razlikuje od [[Bezbednosni zahtev|bezbednosnog zahteva]] po predmetu. Zahtev je pravilo o resursu („karton smeju da vide samo pacijent i lekari koji ga leče“), a kontrola je mera na komponenti („zaposleni ne smeju da dele lozinke“).
