---
tip: pojam
aliases: [component-level threat]
izvor: Nema standardne definicije. Najbliža je praksa primene STRIDE metode po elementu sistema (Shostack, Threat Modeling: Designing for Security, 2014).
---
# Pretnja po komponenti (component-level threat)

## Definicija
Pretnja po komponenti je [[Pretnja|pretnja]] ograničena na jednu [[Komponenta sistema|komponentu sistema]] u kojoj se ugroženi resurs nalazi.

## Primer
Pretnja da napadač naruši integritet rezultata analiza Klinike Sana razlaže se na tri pretnje po komponenti: izmenu rezultata u laboratorijskom sistemu, izmenu u integraciji laboratorijskog sistema sa sistemom elektronskih kartona i izmenu u bazi sistema elektronskih kartona. Napadač koji preuzme administratorski nalog u Active Directory-ju da bi izmenio rezultat u bazi ostvaruje treću pretnju po komponenti. Active Directory je pri tome deo putanje [[Napad|napada]], a ne komponenta ove pretnje.

## Napomene
Komponenta pretnje po komponenti je mesto gde se svojstvo resursa narušava, a ne mesto gde napadač pristupa sistemu. Napad do te komponente može proći kroz više drugih komponenti.
