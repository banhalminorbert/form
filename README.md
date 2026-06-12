# Digitális Entitás Audit Framework

**Professional Digital Identity & Reputation Strategy Assessment Tool**

A [Mag. Tamás Tóth e.U.](https://www.metallagentur.at) által fejlesztett, GDPR-kompatibilis, professzonális audit-rendszer vállalkozók, közéleti személyiségek és szervezetek digitális jelenlétének értékeléséhez.

---

## 📋 Dokumentáció és Fájlok

### Fő Fájlok

```
├── index.html                          # FŐOLDAL — Interaktív audit kérdőív (GDPR-kompatibilis)
├── README.md                          # Ez a dokumentum
├── GDPR_COMPLIANCE.md                 # GDPR és osztrák adatvédelmi nyilatkozat
├── LICENSE.md                         # Jogok és felelősség korlátozás
├── IMPRESSUM.md                       # Impresszum (Mag. Tamás Tóth e.U.)
├── TERMS_OF_SERVICE.md                # Felhasználási feltételek
└── docs/
    ├── Digital_Entity_Audit_Template.md
    ├── ÚTMUTATÓ.txt
    └── Technikai_Specifikáció.md
```

---

## 🎯 Projekt Leírása

### Cél

A **Digitális Entitás Audit Framework** egy kérdőív-alapú, AI-barát stratégiai értékelési rendszer, amely:

1. **Strukturált adatgyűjtés** — 60+ kérdésből álló, 9 szekciós kérdőív
2. **Elemzési sablon** — Kitölthető audit-dokumentum az auditorok számára
3. **Nemzetközi pozicionálás** — SEO, GEO (AI-keresés), Knowledge Graph optimalizálás
4. **GDPR-kompatibilitás** — EU és osztrák jogszabályoknak való teljes megfelelés

### Alkalmazási Esetek

✓ **Egyéni vállalkozók** (tanácsadó, szakértő, influencer)  
✓ **Közéleti személyiségek** (politikus, művész, üzletember)  
✓ **Nonprofit szervezetek** (alapítvány, NGO, kulturális intézmény)  
✓ **Kreatív ügynökségek** (saját kliensfelméréshez)

---

## 🚀 Gyors Indítás (Quick Start)

### 1. Lokális Futtatás

```bash
# Clone a repository-t
git clone https://github.com/metallagentur/digital-entity-audit.git

# Nyisd meg az index.html-t böngészőben
open index.html
# vagy
firefox index.html
```

### 2. GitHub Pages Deployment

```bash
# Ha GitHub-on van a repo
git push origin main

# GitHub Pages beállítása:
# Repo Settings > Pages > Source: main branch, /root folder
# Ezután elérhető: https://username.github.io/digital-entity-audit/
```

### 3. Saját Szerveren Deployment

```bash
# Másold az index.html és a docs/ mappát a szerveredre
scp index.html user@server:/var/www/html/
scp -r docs/ user@server:/var/www/html/

# Apache vagy Nginx konfigurálás: ld. alább
```

---

## ⚖️ JOGI SZEKCIÓK ÉS COMPLIANCE

### GDPR (2016/679/EU) Compliance

Az `index.html` az alábbi GDPR-követelményeket teljesíti:

✓ **Artikulus 13 & 14**: Adatkezelési tájékoztatás (explicit nyilatkozat)  
✓ **Artikulus 7**: Szabad, konkrét, értelmes hozzájárulás (opt-in checkboxok)  
✓ **Artikulus 17**: Jog a törléshez (30 nap után automatikus adattörlés)  
✓ **Artikulus 20**: Adathordozhatóság (teljes JSON export az e-mailben)  
✓ **Artikulus 21**: Jog a hozzájárulás megvonásához (e-mail-ben nyújtva)

**Adatkezelő**: Mag. Tamás Tóth e.U., [City], [Country]  
**Ügyfél céljára végzett feldolgozás**: Digitális entitás audit és stratégiai tanácsadás  
**Tárolási időtartam**: 30 nap, majd végleges törlés (vagy megmarad, ha szerződés kötik)

### Osztrák Adatvédelmi Törvény (DSG)

Az alábbi osztrák szabályozás megsértésének elkerülésével:

✓ **Datenschutzgesetz 2000** (DSG): Személyes adatok védelme  
✓ **Telekommunikációs Törvény (TKG)**: E-mail és telefon adatok kezelése  
✓ **E-kereskedelem Törvény**: Impresszum és jogszabályi nyilatkozatok

### Jogi Nyilatkozatok az index.html-ben

1. **Impresszum (Pflichtangaben nach TMG/E-Commerce-Richtlinie)**
   - Szervezet neve: Mag. Tamás Tóth e.U.
   - Cím: [City], [Country]
   - Felelős: Tamas Toth
   - E-mail: [your-email@example.com]
   - Törvényi forma: GmbH

2. **Adatvédelmi Nyilatkozat**
   - Teljes GDPR-kompatibilis adatvédelmi szöveg az űrlapban
   - Link az `GDPR_COMPLIANCE.md` fájlhoz

3. **Felhasználási Feltételek**
   - Szellemi tulajdon védelme
   - Felelősség korlátozás
   - Szerződéses feltételek
   - Ld.: `TERMS_OF_SERVICE.md`

4. **Bizalmasság és Szerződési Kötelezettségek**
   - Az audit-dokumentum bizalmas
   - Harmadik féllel nem osztható meg
   - Kizárólag szerződéskötésre jogosuló felek által használható

---

## 🔒 Adatkezelés és Biztonság

### Adatok Forrása és Továbbítása

| Adat | Forrás | Továbbítás | Tárolás | Törlés |
|------|--------|-----------|---------|--------|
| E-mail, Név | Kérdőív | HTTPS (TLS 1.2+) | Formspree + Metallagentur | 30 nap |
| Szenzitív adat (jogi konfliktusok) | Kérdőív | HTTPS | Titkosított szerver | 30 nap |
| Audit-dokumentum | AI-feldolgozás | E-mail (HTTPS) | Ügyfél eszköz | Megmarad |

### Biztonsági Mérések

✓ **HTTPS/TLS 1.2+**: Teljes forgalom titkosítása  
✓ **Formspree**: Harmadik féltől függő, GDPR-kompatibilis e-mail gateway  
✓ **Jelszó-hash** (bcrypt vagy SHA-256): Ha szükséges  
✓ **Audit naplózás**: Kérésre rendelkezésre bocsátandó

---

## 📄 Kötelező Jogi Fájlok (Szükséges a Repo-ban)

### 1. GDPR_COMPLIANCE.md

Teljes GDPR nyilatkozat, beleértve:
- Adatkezelő, feldolgozó, ügyfél definíció
- Jogalapok (GDPR Art. 6)
- Alanyok jogai (hozzáférés, törlés, adathordozhatóság)
- Nemzetközi adattovábbítás (Standard Contractual Clauses)
- Panasztétel (nemzeti adatvédelmi hatóságnál)

### 2. LICENSE.md

Az audit-kód és -sablonok licenciája:

```
Ajánlott: CC BY-NC-ND 4.0 (Creative Commons)
- Módosítás: NEM engedélyezett
- Kereskedelmi: NEM engedélyezett
- Megosztás: Engedélyezett (attribúcióval)
```

### 3. IMPRESSUM.md

Közvetlenül szükséges osztrák és EU kötelezettségek:

```
Mag. Tamás Tóth e.U.
[City], [Country]
FN: [Firmenregister szám]
ÖSt.ID: [ÖSt.ID szám]
Geschäftsführer: Tamas Toth
```

### 4. TERMS_OF_SERVICE.md

- Szerződéses kötelezettségek
- Felelősség korlátozás
- Nyilatkozat a nem-garantált jellegről
- Szellemi tulajdon védelme

### 5. CODE_OF_CONDUCT.md

Opcionális, de ajánlott:
- Közösség viselkedési szabályai
- Szexuális zaklatás, diszkrimináció nulla tolerancia
- Bírálatokra vonatkozó irányelvek

---

## 🛠️ Technikai Specifikáció

### Felhasznált Technológiák

| Technológia | Verzió | Célja | License |
|-------------|--------|-------|---------|
| HTML5 | 5 | Struktúra | Public Domain |
| CSS3 | 3 | Stílus (Flexbox, Grid) | Public Domain |
| JavaScript (Vanilla) | ES6+ | Forma logika, validáció | Public Domain |
| Rendszerfontok | Aktuális | New York / Georgia és San Francisco / system sans fallback | Nincs külső betöltés |
| Formspree | API | E-mail gateway | GDPR-kompatibilis SaaS |

### Browser Kompatibilitás

✓ Chrome/Chromium 90+  
✓ Firefox 88+  
✓ Safari 14+  
✓ Edge 90+  
✓ Mobile: iOS Safari 14+, Chrome Android  

### Szintaxis és Konvenciók

- **Indentáció**: 2 szóköz
- **Karakterkódolás**: UTF-8 BOM nélkül
- **Sortörések**: LF (\n), nem CRLF (\r\n)
- **Max. sorhos**: 100 karakter (ajánlott)

### Build és Deployment

```bash
# Nincs build folyamat szükséges (plain HTML/CSS/JS)

# Validálás (opcionális)
npm install -g html-validate
html-validate index.html

# Lighthouse teszt (opcionális)
npm install -g lighthouse
lighthouse index.html --output-path=./report.html
```

---

## 📧 E-mail Integráció

### Formspree Setup

Az `index.html` az alábbi form-actiont használja:

```html
<form id="assessmentForm" action="https://formspree.io/f/mgvwyvoa" method="POST">
```

**Saját Formspree-s végpont beállításához:**

1. Látogass el a https://formspree.io oldalra
2. Hozz létre egy új formot saját e-maileddel
3. Másold a végpontot (pl. `f/mgvwyvoa`)
4. Cseréld le az `index.html`-ben a form actionben

### E-mail Tartalom

Az ügyfél által kitöltött adatok formátolt e-mailben érkeznek az alábbi szekciókkal:

```
DIGITÁLIS ENTITÁS AUDIT - KITÖLTÖTT ÉRTÉKELŐLAP
================================================

SZEMÉLYES ADATOK
SZAKMAI PROFIL
EREDMÉNYEK / DÍJAK
TÁRSADALMI HATÁS
DIGITÁLIS JELENLÉT
JÖVŐKÉP
PARTNEREK / SZÖVETSÉGEK
TECHNIKAI KÉRDÉSEK
KONTAKT PREFERENCIÁK
EGYÉB MEGJEGYZÉSEK
JOGI NYILATKOZATOK

================================================
GDPR-KOMPATIBILIS | Mag. Tamás Tóth e.U.
```

---

## 🔐 Biztonsági Javaslatok

### SSL/TLS Tanúsítvány

Ha saját szerveren hostolod:

```bash
# Let's Encrypt (ingyenes, auto-renew)
sudo certbot certonly --standalone -d yourdomain.com
```

### CORS Beállítás (ha szükséges)

```apache
# .htaccess (Apache)
Header set Access-Control-Allow-Origin "https://yourdomain.com"
Header set Access-Control-Allow-Methods "GET, POST, OPTIONS"
Header set X-Content-Type-Options "nosniff"
Header set X-Frame-Options "SAMEORIGIN"
Header set Content-Security-Policy "default-src 'self'; script-src 'self' 'unsafe-inline'; style-src 'self' 'unsafe-inline'; font-src 'self' data:"
```

### nginx Konfigurálás

```nginx
server {
    listen 443 ssl http2;
    server_name yourdomain.com;

    ssl_certificate /etc/letsencrypt/live/yourdomain.com/fullchain.pem;
    ssl_certificate_key /etc/letsencrypt/live/yourdomain.com/privkey.pem;

    root /var/www/html;
    index index.html;

    add_header X-Content-Type-Options "nosniff";
    add_header X-Frame-Options "SAMEORIGIN";
    add_header Content-Security-Policy "default-src 'self'; script-src 'self' 'unsafe-inline'; style-src 'self' 'unsafe-inline'; font-src 'self' data:";

    location / {
        try_files $uri $uri/ =404;
    }
}
```

---

## 📋 Checklist: Deployment Előtt

- [ ] `index.html` validáció (W3C Validator)
- [ ] GDPR texto ellenőrzése (jogász által)
- [ ] Formspree végpont beállítása
- [ ] SSL/TLS tanúsítvány (produktion)
- [ ] Impresszum kitöltése (Metallagentur adatok)
- [ ] E-mail-cím megadása ([your-email@example.com])
- [ ] Backup stratégia (mined 30 nap adattörlés)
- [ ] Privacy Policy link működése
- [ ] Mobile responsiveness teszt
- [ ] Lighthouse audit futtatás (90+ pontszám célzott)

---

## 🤝 Hozzájárulás

Az audit-keretrendszer az alábbi feltételek alatt módosítható:

1. **Az CC BY-NC-ND 4.0 licencre való hivatkozás** szükséges
2. **Jogi szekciók nem módosíthatóak** (a Metallagentur felelőssége)
3. **Formátumon belüli módosítások** engedélyezetek (pl. szín, betűtípus)
4. **Új szekciók hozzáadása** engedélyeztek (új kérdésekkel)

---

## 📞 Támogatás és Kontakt

**Mag. Tamás Tóth e.U.**
- Web: https://www.metallagentur.at
- E-mail: [your-email@example.com]
- Ország: Österreich (Austria)
- Forma: GmbH (Gesellschaft mit beschränkter Haftung)

---

## 📄 Verzió és Frissítések

| Verzió | Dátum | Változások |
|--------|-------|-----------|
| 1.0 | 2026-05-08 | Kezdeti kibocsátás: HTML form, GDPR compliance, teljes jogi szekciók |
| 1.1 (tervezett) | 2026-06 | Spanyol és német nyelvű sablonok |
| 2.0 (tervezett) | 2026-09 | Automatizált audit-generátor (AI-integrációval) |

---

## 📜 Fájl Struktúra a Repo-ban

```
digital-entity-audit/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   └── PULL_REQUEST_TEMPLATE.md
├── docs/
│   ├── Digital_Entity_Audit_Template.md
│   ├── ÚTMUTATÓ.txt
│   └── Technikai_Specifikáció.md
├── .gitignore
├── .editorconfig
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── GDPR_COMPLIANCE.md
├── IMPRESSUM.md
├── LICENSE.md
├── README.md (ez a fájl)
├── TERMS_OF_SERVICE.md
├── index.html (FŐOLDAL)
└── package.json (opcionális, meta-információk)
```

---

## ⚠️ Jogi Felelősség Korlátozás

**Az index.html és az audit-keretrendszer "ahogyan van" (AS IS) biztosított, semmilyen garanciával nem.**

- **Az audit nem garantálja** az internetes pozicionálás fejlődését
- **A Metallagentur nem vállal felelősséget** harmadik féltől származó adatokért
- **Az algoritmus-frissítések** nem előre jelezhetőek vagy garantálhatóak

A teljes felelősség korlátozásért ld. a `TERMS_OF_SERVICE.md` fájlt.

---

## 🌐 Nemzetközi Kiterjesztés

Az alábbi nyelvek támogatottsága tervezett:

- [x] **Magyar** (hu)
- [ ] **Angol** (en) — v1.1+
- [ ] **Német** (de) — v1.1+
- [ ] **Spanyol** (es) — v1.1+

A fordítási berkehezést a `docs/` mappában végezzük.

---

## 📚 További Források

- **GDPR Magyarázat**: https://gdpr-info.eu/
- **Austria DSG**: https://www.dsb.gv.at/
- **Formspree Docs**: https://formspree.io/
- **W3C HTML Validator**: https://validator.w3.org/
- **Lighthouse**: https://developers.google.com/web/tools/lighthouse

---

**© 2026 Mag. Tamás Tóth e.U.. All rights reserved.**

*Gitub repository: [digital-entity-audit](https://github.com/metallagentur/digital-entity-audit)*

---

**Last Updated**: 2026-05-08  
**Maintainer**: Mag. Tamás Tóth e.U.  
**Status**: Production Ready ✓


## 2026-06-11 GDPR / AI útvonal frissítés

A form magyar alapnyelvű, angol és német fordítással. A szolgáltatási útvonal szerint az adatok elsődlegesen Mag. Tamas Toth / Mag. Tamás Tóth e.U.-hoz érkeznek, és az ügyfél Mag. Tamás Tóth e.U.-val szerződik. A 96 órás HTML stratégiai audit elkészítése Mag. Tamás Tóth e.U. szerződéses szakmai alvállalkozójának / GDPR Art. 28 szerinti adatfeldolgozójának közreműködésével történhet. A feldolgozás ChatGPT, Claude, Grok, Gemini és Copilot AI-eszközök támogatásával, emberi szakmai kontroll mellett történhet. A form nem kér különleges kategóriájú személyes adatot.
