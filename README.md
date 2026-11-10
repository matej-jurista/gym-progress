# Gym Progress PWA v5

Mobilný tréningový denník pre trojdňový plán **Upper A / Lower / Upper B**, zameraný na funkčnú silu pre padel, bicykel a turistiku.

## Spustenie

Appka je bez buildu a bez závislostí. Nahraj všetky súbory do koreňa GitHub Pages (alebo iného HTTPS hostingu). Otvor URL v Safari/Chrome a zvoľ **Pridať na plochu**. Po prvom načítaní bude fungovať offline.

Na lokálne vyskúšanie spusti v tomto priečinku jednoduchý webový server, napr. `python3 -m http.server 8080`, a otvor `http://localhost:8080`.

## Čo obsahuje

- váha a opakovania pre každú sériu; váhy podporujú ľubovoľné desatinné čísla vrátane 0,25 / 0,5 / 0,75 kg,
- posledné hodnoty a odporúčania podľa štvortýždňovej periodizácie,
- návrhy podobných cvikov aj ľubovoľná vlastná náhrada,
- oddelená história každého náhradného cviku pri zachovaní starej histórie,
- história, dátumy a graf odhadovaného 1RM,
- JSON export/import,
- lokálne uloženie a offline PWA režim.

## Dáta a aktualizácia

Dáta sa ukladajú v `localStorage` aktuálneho prehliadača a neposielajú sa na server. Pred vymazaním údajov prehliadača alebo zmenou URL sprav JSON export. Pri aktualizácii súborov ponechaj rovnakú URL; service worker používa cache `gym-progress-v5.0.0`.

Pri prvom spustení na rovnakej URL sa existujúca história z Gym Progress v4 automaticky prenesie do v5. Pôvodný záznam `gym-progress-v4` zostane nedotknutý ako záloha.

Poznámka: tréningový plán je praktická šablóna, nie zdravotné odporúčanie. Techniku a záťaž prispôsob bolesti, regenerácii a odporúčaniam trénera alebo fyzioterapeuta.
