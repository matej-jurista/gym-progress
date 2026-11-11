# Gym Progress PWA v5

Mobilný tréningový denník pre trojdňový plán **Upper A / Lower / Upper B**, zameraný na funkčnú silu pre padel, bicykel a turistiku.

## Spustenie

Appka je bez buildu a bez závislostí. Nahraj všetky súbory do koreňa GitHub Pages (alebo iného HTTPS hostingu). Otvor URL v Safari/Chrome a zvoľ **Pridať na plochu**. Po prvom načítaní bude fungovať offline.

Na lokálne vyskúšanie spusti v tomto priečinku jednoduchý webový server, napr. `python3 -m http.server 8080`, a otvor `http://localhost:8080`.

## Čo obsahuje

- váha a opakovania pre každú sériu; váhy podporujú ľubovoľné desatinné čísla vrátane 0,25 / 0,5 / 0,75 kg,
- pridanie aj odobratie extra série bez možnosti omylom znížiť počet pod predpísaný plán,
- odporúčané prestávky podľa typu cviku a osobitné odporúčanie pre supersérie,
- tri režimy merania cviku: váha + opakovania, vlastná váha + opakovania alebo čas v sekundách,
- voliteľné RIR pri každej sérii,
- spätná editácia uloženého tréningu vrátane pridania a odstránenia sérií bez vytvárania duplikátu,
- posledné hodnoty a odporúčania podľa štvortýždňovej periodizácie,
- návrhy podobných cvikov aj ľubovoľná vlastná náhrada,
- oddelená história každého náhradného cviku pri zachovaní starej histórie,
- história, dátumy a graf podľa režimu merania: odhad 1RM, maximum opakovaní alebo najdlhší čas,
- JSON export/import,
- lokálne uloženie a offline PWA režim.

## Dáta a aktualizácia

Dáta sa ukladajú v `localStorage` aktuálneho prehliadača a neposielajú sa na server. Pred vymazaním údajov prehliadača alebo zmenou URL sprav JSON export. Pri aktualizácii súborov ponechaj rovnakú URL; service worker používa cache `gym-progress-v5.2.0`.

Staršie v5 aj v4 JSON zálohy sa pri importe doplnia o nové polia bez zmeny pôvodných tréningových hodnôt. Pri cvikoch bez kilogramov sa dá zvoliť vlastná váha alebo čas; staré záznamy zostávajú zachované.

Pri prvom spustení na rovnakej URL sa existujúca história z Gym Progress v4 automaticky prenesie do v5. Pôvodný záznam `gym-progress-v4` zostane nedotknutý ako záloha.

Poznámka: tréningový plán je praktická šablóna, nie zdravotné odporúčanie. Techniku a záťaž prispôsob bolesti, regenerácii a odporúčaniam trénera alebo fyzioterapeuta.
