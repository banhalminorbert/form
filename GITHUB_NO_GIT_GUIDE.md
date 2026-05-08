# GitHub feltöltés GIT NÉLKÜL — Teljes útmutató

**[Your Organization Name] GmbH**

---

## 🎯 CÉL: Fájlok feltöltése közvetlenül GitHub web felületen

**Szükséges:** Csak böngésző + GitHub account + fájlok

---

## 📋 LÉPÉSRŐL LÉPÉSRE

### 1️⃣ GITHUB ACCOUNT & REPOSITORY (5 perc)

**Ha nincs GitHub accountod:**
- https://github.com/signup
- E-mail, jelszó, felhasználónév

**Új repository létrehozása:**
1. https://github.com/new
2. **Repository name:** `form`
3. **Description:** "Digital Entity Audit Framework"
4. **Public** (nyilvános)
5. **Initialize this repository with:**
   - [ ] README.md (ne jelöld be!)
   - [ ] .gitignore (ne jelöld be!)
   - [ ] License (ne jelöld be!)
6. **Create repository**

---

### 2️⃣ FÁJLOK FELTÖLTÉSE (GitHub Web UI)

#### **Módszer A: Egy fájl feltöltése (egyenként)**

1. A repository-n belül: **Add file** > **Upload files**
2. Drag & drop vagy klikkelj: **choose your files**
3. Válassz egy fájlt (pl. `index.html`)
4. **Commit changes** gomb alul
5. Ismételd meg minden fájlhoz

#### **Módszer B: Több fájl feltöltése egyszerre (gyorsabb)**

1. A repository-n belül: **Add file** > **Upload files**
2. Drag & drop **összes fájlt** egyszerre:
   ```
   index.html
   README.md
   GDPR_COMPLIANCE.md
   TERMS_OF_SERVICE.md
   IMPRESSUM.md
   LICENSE.md
   00_START_HERE.md
   GITHUB_DEPLOYMENT_GUIDE.md
   Digital_Entity_Audit_Template.md
   DOWNLOAD_INFO.txt
   package.json
   .gitignore
   ```
3. A GitHub automatikusan felismeri őket
4. **Commit changes** gomb

#### **Módszer C: GitHub Web Editor (másodikként)**

Ha már vannak fájlok:
1. Klikkelj egy fájlra (pl. `index.html`)
2. **Edit this file** (ceruza ikon)
3. Módosítsd az e-mail címet: `[your-email@example.com]` → **SAJÁT EMAIL**
4. **Commit changes**

---

### 3️⃣ GITHUB PAGES AKTIVÁLÁSA

1. Repository > **Settings** (fogaskerék ikon)
2. Bal oldal: **Pages**
3. **Source** szekció:
   ```
   ┌─────────────────────────┐
   │ Deploy from a branch    │
   ├─────────────────────────┤
   │ Branch: main            │
   │ Folder: / (root)        │
   │ [Save]                  │
   └─────────────────────────┘
   ```
4. **Custom domain** (ha szeretnéd):
   ```
   form.digitallagentur.at
   [✓] Enforce HTTPS
   [Save]
   ```

---

### 4️⃣ DNS KONFIGURÁLÁS (ha custom domain)

**Ha szeretnéd: https://form.digitallagentur.at/**

A domain kezelőjében (pl. GoDaddy, Namecheap, Cloudflare):

```
Rekord típusa: CNAME
Név: form
Érték: [USERNAME].github.io
TTL: 3600
```

**Utána:** 24-48 óra várakozás

---

## ⚠️ FONTOS MÓDOSÍTÁSOK FELTÖLTÉS ELŐTT

### A. index.html módosítása

**Mielőtt feltöltöd, módosítsd az e-mail címet:**

1. `index.html` megnyitása egy szövegszerkesztővel (NotePad++, VS Code, stb.)
2. Ctrl+F (Keresés): `[your-email@example.com]`
3. Cserelje le: **[SAJÁT EMAIL-CÍMed]**
4. Ctrl+S (Mentés)
5. Feltöltés

### B. Formspree endpoint módosítása

Az index.html-ben keresés után találj:
```html
<form id="assessmentForm" action="https://formspree.io/f/mgvwyvoa"
```

**Saját endpoint beszerzése:**
1. https://formspree.io
2. "New Form" > e-mail-cím megadása
3. Kapsz egy endpoint-ot: `f/xyz123`
4. Az index.html-ben cseréld: `f/mgvwyvoa` → `f/xyz123`
5. Mentés

### C. IMPRESSUM.md kitöltése

Az IMPRESSUM.md-ben keresés után találj:
```
[Konkrét cím szükséges az osztrák E-kereskedelem törvény szerint]
```

Kitöltsd:
- FN (Firmenregister-Nummer)
- UID (Adóazonosító)
- Konkrét Wien-es cím
- Telefon szám
- Biztosítás adatai

---

## 🎬 TELJES WORKFLOW (GIT NÉLKÜL)

```
1. GitHub account: https://github.com/signup
   Idő: 5 perc

2. New repository: https://github.com/new
   Idő: 1 perc

3. Fájlok módosítása:
   - index.html: e-mail + Formspree
   - IMPRESSUM.md: cégadatok
   Idő: 5 perc

4. Fájlok feltöltése:
   a) GitHub > Add file > Upload files
   b) Drag & drop összes fájlt
   c) Commit changes
   Idő: 3 perc

5. GitHub Pages aktiválása:
   a) Settings > Pages
   b) Deploy from a branch: main / root
   c) Custom domain (opcionális)
   Idő: 2 perc

6. DNS beállítása (ha custom domain):
   a) DNS kezelő > CNAME rekord
   b) form → [USERNAME].github.io
   Idő: 2 perc

7. Várakozás:
   - DNS propagáció: 24-48 óra
   - HTTPS tanúsítvány: 1-24 óra

TELJES IDŐ: ~20 perc (várakozás nélkül)
```

---

## ✅ ELLENŐRZÉSI LISTA

### Feltöltés előtt:
- [ ] Összes fájl a gépedön
- [ ] index.html: e-mail cím módosítva
- [ ] index.html: Formspree endpoint beállítva
- [ ] IMPRESSUM.md: cégadatok kitöltve
- [ ] Szövegszerkesztő mentése (Ctrl+S)

### Feltöltés után:
- [ ] GitHub repository létrehozva
- [ ] Összes fájl a repo-ban
- [ ] Settings > Pages aktív
- [ ] Custom domain (opcionális)
- [ ] DNS CNAME rekord (opcionális)

### Végső teszt:
- [ ] https://github.com/[USERNAME]/form elérhető
- [ ] index.html megjelenik a repo-ban
- [ ] https://form.digitallagentur.at/ működik (ha custom domain)
- [ ] Forma kitölthető
- [ ] E-mail érkezik Formspree-ből

---

## 📸 KÉPEK A GITHUB UI-BÓL

### Add file > Upload files
```
┌─────────────────────────────────────────┐
│ Your repository                         │
│                                         │
│ [Add file ▼]                            │
│    ├─ Create new file                   │
│    └─ Upload files ← KATTINTS IDE       │
│                                         │
│ Or drag files here                      │
│ to upload them                          │
└─────────────────────────────────────────┘
```

### Drag & drop fájlok
```
┌─────────────────────────────────────────┐
│ Drag additional files here or           │
│ click to select                          │
│                                         │
│ [Rá húzod az összes fájlt]              │
│                                         │
│ index.html                              │
│ README.md                               │
│ GDPR_COMPLIANCE.md                      │
│ ... (összes fájl)                       │
└─────────────────────────────────────────┘
```

### Commit changes
```
┌─────────────────────────────────────────┐
│ Commit changes                          │
│                                         │
│ Add an optional extended description... │
│ [szöveg mező]                           │
│                                         │
│ ○ Commit directly to the main branch    │
│ ○ Create a new branch for this commit   │
│                                         │
│ [Commit changes]  [Cancel]              │
└─────────────────────────────────────────┘
```

---

## 🆘 HIBAELHÁRÍTÁS

### "Nem tudom feltölteni a fájlokat"
**Megoldás:**
- Add file > Upload files (nem az Edit felülettől)
- Drag & drop működik jobbnak
- Egyszerre max ~25 fájl

### "404 hiba az index.html-nél"
**Megoldás:**
- Settings > Pages ellenőrzése
- Source: main branch / root folder
- Várakozz 5 percet az újra betöltésre

### "Formspree nem működik"
**Megoldás:**
- Valóban HTTPS-en vagyunk?
- https://form.digitallagentur.at/ (nem http)
- Formspree endpoint helyesen beállítva?

### "HTTPS nem működik"
**Megoldás:**
- Várakozz 24 órát
- Settings > Pages ellenőrzése
- "Enforce HTTPS" gomb megjelenik, ha ready

---

## 💡 TIPP: Szövegeditor ajánlások

Fájlok módosításához:

**Windows:**
- Notepad++ (ingyenes) - legjobb
- VS Code (ingyenes)
- Sublime Text

**Mac:**
- VS Code (ingyenes)
- TextEdit (alapértelmezett)
- BBEdit

**Linux:**
- VS Code (ingyenes)
- nano / vim

**Online (böngészőben):**
- GitHub web editor (közvetlenül a repo-ban)
- Replit.com (ingyenes)

---

## 📂 FÁJLOK FELÉPÍTÉSE A REPO-BAN

Utána így kell kinézni:

```
form/ (repository)
├── index.html ← FŐOLDAL!
├── README.md
├── GDPR_COMPLIANCE.md
├── TERMS_OF_SERVICE.md
├── IMPRESSUM.md
├── LICENSE.md
├── 00_START_HERE.md
├── GITHUB_DEPLOYMENT_GUIDE.md
├── Digital_Entity_Audit_Template.md
├── DOWNLOAD_INFO.txt
├── package.json
├── .gitignore
└── [GitHub automatikus fájlok]
    ├── .github/
    └── _config.yml (GitHub Pages által)
```

---

## 🎯 VÉGPONTOK

Feltöltés után ezek működnek:

```
✓ https://github.com/[USERNAME]/form
  → A repository GitHub-on

✓ https://[USERNAME].github.io/form/
  → A weboldal (GitHub Pages alapértelmezett)

✓ https://form.digitallagentur.at/
  → A weboldal custom domain-nel (ha beállítottad)
```

Felhasználónak:
```
👉 https://form.digitallagentur.at/
   → Ez az, amit lát (index.html automatikusan betöltődik)
```

---

## ⏱️ IDŐBECSLÉS

| Lépés | Idő |
|------|-----|
| GitHub account | 5 perc |
| Repository | 1 perc |
| Fájlok módosítása | 5 perc |
| Fájlok feltöltése | 3 perc |
| GitHub Pages | 2 perc |
| DNS (opcionális) | 2 perc |
| **AKTÍV: 18 perc** |
| DNS propagáció | 24-48 óra |
| HTTPS tanúsítvány | 1-24 óra |

---

## ✨ VÉGEREDMÉNY

**Semmilyen GIT parancs nélkül:**

1. ✅ Fájlok GitHub-on
2. ✅ Weboldal működik: https://form.digitallagentur.at/
3. ✅ HTTPS biztonságos
4. ✅ Forma működik (Formspree)
5. ✅ GDPR-kompatibilis
6. ✅ Production-ready

---

**© 2026 [Your Organization Name] GmbH | GDPR-kompatibilis | CC BY-NC-ND 4.0**

