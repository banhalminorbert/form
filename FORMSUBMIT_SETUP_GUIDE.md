# Űrlapküldés beállítási útmutató — Google Apps Script / Google Workspace

Ez a verzió nem FormSubmit.co-ra épül. Az `index.html` aktuális form action URL-je Google Apps Script végpontot használ, amely a beérkező adatokat e-mailben továbbítja a szolgáltatási folyamat szerint.

## Aktuális adatút

1. A végügyfél kitölti a formot a `form.metallagentur.at` oldalon.
2. A form POST kérést küld a Google Apps Script végpontra.
3. Az adatok Mag. Tamas Toth / Mag. Tamás Tóth e.U. szolgáltatási folyamatába érkeznek.
4. A 96 órás HTML stratégiai audit elkészítése Mag. Tamás Tóth e.U. szerződéses szakmai alvállalkozójának / GDPR Art. 28 szerinti adatfeldolgozójának közreműködésével történhet.
5. A feldolgozás ChatGPT, Claude, Grok, Gemini és Copilot AI-eszközök támogatásával, emberi szakmai kontroll mellett történhet.

## GDPR-minimum

- A form noindex / nofollow beállítással működik.
- A különleges kategóriájú személyes adatok megadását a form kifejezetten tiltja.
- A végügyfél előzetesen látja az AI-, adatfeldolgozási és nyilvános kutatási tájékoztatót.
- A form Mag. Tamás Tóth e.U. elsődleges szerződéses és adatkezelői szerepét, valamint a szerződéses szakmai alvállalkozó / adatfeldolgozó bevonásának lehetőségét tartalmazza.
- Harmadik országbeli feldolgozás esetén megfelelő GDPR-garancia szükséges: SCC, megfelelőségi határozat, EU–US DPF, anonimizálás vagy pseudonimizálás.

## Tesztelés

Beküldés előtt ellenőrizni kell:

- a Google Apps Script végpont él;
- az e-mail címzettek helyesek;
- a teljes kérdés + válasz export bekerül az e-mailbe;
- HU / EN / DE nyelven a jogi checkboxok és adatvédelmi blokkok azonos tartalmúak;
- tesztbeküldés után a gomb lezár, és nincs dupla beküldés.
