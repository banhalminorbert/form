# 🎯 START HERE — Digitális Entitás Audit Framework

**[Your Organization Name] GmbH**

---

## ✅ Mit kaptál?

Egy **teljes, GDPR-kompatibilis, production-ready** digitális entitás audit rendszert:

```
✓ Interaktív HTML kérdőív (index.html)
✓ Teljes jogi dokumentáció (GDPR, Terms, Impressum, License)
✓ Elemzési sablon (audit készítéshez)
✓ GitHub deployment útmutató
✓ Formspree integrálás (e-mail form)
```

---

## 📋 Fájlok Röviden

| Fájl | Tartalom | Használat |
|------|----------|-----------|
| **index.html** | Főoldal - az audit kérdőív | Nyiss meg böngészőben |
| **README.md** | Teljes dokumentáció | Olvasd el GitHub-on |
| **GDPR_COMPLIANCE.md** | GDPR teljes szövege | Jogi referencia |
| **TERMS_OF_SERVICE.md** | Felhasználási feltételek | Szerződési szabályok |
| **IMPRESSUM.md** | Impresszum (kötelező) | Osztrák E-commerce törvény |
| **LICENSE.md** | CC BY-NC-ND 4.0 | Szerzői jogi információ |
| **package.json** | NPM metaadatok | GitHub/build rendszerek |
| **.gitignore** | Git exclusions | GitHub repository |

---

## 🚀 Gyors Indítás

### 1️⃣ Lokálisan Tesztelni

```bash
# Böngészővel nyiss meg
open index.html
# vagy
firefox index.html
```

### 2️⃣ GitHub-ra Feltölteni

```bash
# Repository létrehozása: https://github.com/new
# Nézd meg: GITHUB_DEPLOYMENT_GUIDE.md

git clone https://github.com/[USERNAME]/digital-entity-audit.git
cd digital-entity-audit
cp -r * .
git add .
git commit -m "Initial: Digital Entity Audit Framework v1.0"
git push origin main

# GitHub Pages: Settings > Pages > Source: main > Save
# Elérhető: https://[USERNAME].github.io/digital-entity-audit/
```

### 3️⃣ Formspree Beállítása

Az e-mail forma működéséhez:

```html
<!-- index.html-ben keresed: -->
<form id="assessmentForm" action="https://formspree.io/f/mgvwyvoa" ...>
```

**Saját Formspree-s végponthoz:**

1. https://formspree.io oldalra mész
2. "New Form" gomb
3. Az adatod e-mailét megadod
4. Megkapod az endpoint-ot (f/xyz123)
5. Az index.html-ben ezt az végpontot helyettesítesz

---

## ⚖️ Jogi Szekciók (Kritikus!)

### Kötelezően kitöltendő adatok:

```
IMPRESSUM.md-ben:
  - [ ] Cégbejegyzés szám (FN)
  - [ ] Adóazonosító (UID)
  - [ ] Konkrét cím Wien-ben
  - [ ] Telefon szám
  - [ ] Biztosítás adatai
```

### index.html-ben már benne van:

```
✓ GDPR adatvédelmi nyilatkozat
✓ Impresszum hivatkozás
✓ Felelősség korlátozás
✓ Szellemi tulajdon védelem
✓ Bizalmasság nyilatkozat
```

---

## 📧 E-mail Integráció

Az index.html űrlapja **automatikusan elküldi az e-maileket** a **Formspree** szolgáltatáson keresztül.

**Hogy működik:**

1. Ügyfél kitölti az online formát
2. Formspree elküldi: `[your-email@example.com]`
3. Válaszok **automatikusan estrutúráltan** érkeznek

**Tesetelés:**

```bash
# Formspree teszt
curl -X POST https://formspree.io/f/mgvwyvoa \
  -H "Content-Type: application/json" \
  -d '{"name":"Test User","email":"test@example.com"}'
```

---

## 🎨 Testreszabás

### Szín Módosítása

index.html-ben keresed a `:root` CSS-t:

```css
:root {
  --onyx: #0F0F0F;          /* Sötét szín */
  --ivory: #FFFFF0;         /* Világos szín */
  --gold: #D4AF37;          /* Arany akcentus */
  /* stb. */
}
```

### E-mail Cím Módosítása

Keresés: `[your-email@example.com]` — helyettesítsd a saját e-maileddel

### Weboldal Neve/Branding

Keresés: `[Your Organization Name] GmbH` — helyettesítsd a szervezeted nevével

---

## 🔒 Biztonsági Beállítások

### GitHub

1. **Settings > Security**
   - ✓ Require status checks before merging
   - ✓ Dismiss stale pull request approvals
   - ✓ Require branches to be up to date

2. **Secrets** (ha szükséges)
   - FORMSPREE_ENDPOINT
   - EMAIL_PASSWORD (ha mailgun-t használnál)

### HTTPS & SSL

Az index.html csak HTTPS-en működik Formspree-vel.

```
GitHub Pages: Automatikus SSL/TLS ✓
Saját szerver: Let's Encrypt (ingyenes)
```

---

## 📊 Validation & Testing

### HTML Validáció

```bash
npm install -g html-validate
html-validate index.html
```

### Lighthouse Audit

```bash
npm install -g lighthouse
lighthouse index.html --output-path=lighthouse.html
```

**Cél:** 90+ pontszám

---

## 📱 Responsive Design

Az index.html **teljes mértékben responsív**:

```
✓ Desktop (1200px+)
✓ Tablet (768px–1200px)
✓ Mobile (< 768px)
```

Tesztelés: DevTools > Toggle device toolbar (F12 > Ctrl+Shift+M)

---

## 🌍 Nemzetközi Bővítés

### Multilingvális Támogatás (Tervezett v1.1)

```
Jelenleg: Magyar (hu)
v1.1: Angol (en), Német (de)
v2.0: Spanyol (es), Olasz (it)
```

A fordítások a `docs/` mappában lesznek.

---

## 🆘 Segítség & Támogatás

### Problémák

| Probléma | Megoldás |
|----------|----------|
| Forma nem működik | Formspree endpoint ellenőrzése |
| GDPR hibák | GDPR_COMPLIANCE.md-t olvass |
| Design probléma | CSS `:root` módosítása |
| GitHub Pages nem elérhető | Settings > Pages ellenőrzése |

### Kontakt

```
E-mail: [your-email@example.com]
Website: https://www.your-website.com
GitHub Issues: [GitHub repo]/issues
```

---

## ✨ Végső Checklist

- [ ] index.html megnyitható
- [ ] Formspree integrálva
- [ ] GitHub repository létrehozva
- [ ] IMPRESSUM.md kitöltve
- [ ] SSL/HTTPS működik
- [ ] Lighthouse teszt: 90+
- [ ] GDPR nyilatkozat jó
- [ ] Saját domain konfigurálva (opcionális)
- [ ] Backup készült
- [ ] Teams értesültek

---

## 🎉 Kész!

Az audit-keretrendszer **production-ready**. Üdvözlünk a [Your Organization Name] szövetségében!

```
👉 Indíts el: index.html
👉 GitHub: https://github.com/[USERNAME]/digital-entity-audit
👉 Support: [your-email@example.com]
```

---

**© 2026 [Your Organization Name] GmbH | GDPR-kompatibilis | CC BY-NC-ND 4.0**

*Verzió: 1.0.0 | 2026-05-08*
