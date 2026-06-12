# Form audit and GDPR gate fix — 2026-06-12

## Javított hibák

1. A főoldali GDPR/AI elfogadó blokk átkerült a belépő/főoldali kártyába, ezért HU/EN/DE nyelven már a kérdőív megnyitása előtt látható.
2. A `consent_0` checkbox most a fő formhoz van kötve `form="assessmentForm"` attribútummal, ezért a beküldött adatok része lesz akkor is, ha a belépő blokk az elfogadás után elrejtésre kerül.
3. A beküldéshez külön rejtett mezők rögzítik az elfogadás időpontját, nyelvét, verzióját és az elfogadási szöveg pillanatképét.
4. A félrevezető „jelszóval védett” szöveg mindhárom nyelven át lett írva GDPR/adatvédelmi elfogadással védett belépésre, mert a jelenlegi verzió nem tartalmaz aktív jelszómezőt.
5. A fő JavaScript futási hibája javítva: pótolva lettek a hiányzó segédfüggvények és változók az automatikus mentéshez, validációhoz, állapotjelzéshez és exporthoz.
6. A teljes kérdés-válasz export immár figyelembe veszi a formon kívüli, de a formhoz kötött mezőket is, különösen a belépő GDPR checkboxot.
7. HU/EN/DE nyelven ellenőrizve lett a GDPR, AI, feldolgozói, számlázási és kereskedelmi elfogadási címkék megléte.

## Audit státusz

- HTML form: javítva és újracsomagolva.
- Google Apps Script action URL: megmaradt a fájlban: `https://script.google.com/macros/s/AKfycbz2L-DqpBR10Pbr1HwjqtuXlNqcfX1XE_ljg11Pg-Bx9J32fqYns0Jg1KhW8nnR-aInPA/exec`.
- Beküldés élő végpontját nem hívtam meg tesztadatokkal, mert az valódi e-mailt / feldolgozást indíthat.
- Jogi megjegyzés: ez technikai és tartalmi megfelelőségi audit, nem ügyvédi jogi vélemény.

## Még emberileg ellenőrizendő

- A tényleges alvállalkozói / adatfeldolgozói szerződés létezik-e Mag. Tamás Tóth e.U. és a közreműködő között.
- A használt AI-eszközök és Google Workspace / Apps Script adatfeldolgozói feltételei ténylegesen összhangban vannak-e a vállalt tájékoztatóval.
- Az EU-n kívüli adattovábbításokhoz tényleges SCC / adequacy / DPF vagy más garancia dokumentált-e.

## Technikai QA futtatás

- Statikus ellenőrzés: 1 darab fő `assessmentForm` form van.
- `frontGdprNotice` a belépő/főoldali `passwordGate` részen belül van.
- `consent_0` kötelező, a `form="assessmentForm"` attribútummal a fő formhoz van kötve.
- A rejtett jogi naplómezők létrejöttek: elfogadás ideje, nyelve, tájékoztató-verzió, elfogadási szöveg, form URL, beküldési idő, böngészőadat.
- JavaScript szintaktikai ellenőrzés: minden `<script>` blokk `node --check` szerint szintaktikailag érvényes.
- Headless böngészős ellenőrzés: HU/EN/DE nyelvváltás után a fő GDPR checkbox címkéje megfelelő nyelvre vált; elfogadás után a védett tartalom megnyílik; a FormData tartalmazza az `agreeFrontGdprAiNotice=accepted` értéket és a jogi naplómezőket.
- Beküldési esemény szimuláció: a kötelező mezők kitöltése és elfogadások bepipálása után a form validnak minősül, a submit logika futási hiba nélkül lefut, és a teljes kérdés-válasz export elkészül.


## 2026-06-12 szigorított audit kiegészítés

- A Perplexity által kifogásolt Art. 13 / címzett / megőrzési idő / háttérfeldolgozási elemek ellenőrizve lettek.
- Az adatvédelmi tájékoztatóban pontosítva lett, hogy nincs aktív külső Google Fonts betöltés, ezért külön fontszolgáltatói IP-továbbítás nincs.
- A régi „password gate” megfogalmazás a felhasználói és jogi szövegekben GDPR-elfogadásos kapura lett cserélve.
- A verziótörténet 6 hónapos megőrzési utalása 30 napra lett javítva, hogy egyezzen a formban és a rejtett beküldési mezőben szereplő adattal.
- Külső jogi megfelelőségi feltétel maradt: a tényleges AVV/DPA szerződések, szolgáltatói DPA-k és törlési naplók nem a HTML fájl részei, ezeket külön kell megőrizni.
