# FormSubmit.co Beállítási Útmutató

## 🎯 Audit Forma — Mag. Tamás Tóth | Metallagentur GmbH

---

## 📋 Mit Módosítottam

Az audit forma most **FormSubmit.co**-t használ (ugyanúgy, mint a metallagentur.at weboldal).

### ✅ Módosítások:

1. **Form HTML**
   ```html
   <form action="https://formsubmit.co/tamas.toth@metallagentur.at" method="POST">
     <input type="hidden" name="_subject" value="Digitális Entitás Audit - Mag. Tamás Tóth">
     <input type="hidden" name="_captcha" value="false">
     <input type="hidden" name="_template" value="html">
     <input type="hidden" name="_next" value="https://form.digitallagentur.at/">
   ```

2. **JavaScript Feldolgozás**
   - Előtte: Fetch API → Formspree
   - Utána: Natív POST → FormSubmit.co
   - Automatikus e-mail küldés

3. **E-mail Beállítások**
   - Küldő: FormSubmit.co
   - Címzett: **tamas.toth@metallagentur.at**
   - Tárgy: "Digitális Entitás Audit - [Ügyfél Neve]"
   - Template: HTML

---

## 🚀 Telepítés

### Lépés 1: ZIP Letöltése
```bash
Digital_Entity_Audit_Framework_Complete.zip
```

### Lépés 2: Kicsomagolás
```bash
unzip Digital_Entity_Audit_Framework_Complete.zip
cd Digital_Entity_Audit_Framework_Complete
```

### Lépés 3: Fájlok Ellenőrzése
```
├── index.html (formmal + FormSubmit.co)
├── README.md
├── GDPR_COMPLIANCE.md
├── TERMS_OF_SERVICE.md
├── IMPRESSUM.md
├── LICENSE.md
├── és egyéb dokumentumok
```

### Lépés 4: GitHub Feltöltés (GIT nélkül)

1. **GitHub Account**: https://github.com/signup
2. **Új Repository**: https://github.com/new
   - Név: `digital-entity-audit`
   - Nyilvános (Public)
3. **Fájlok Feltöltése**:
   - Add file > Upload files
   - Drag & drop összes fájl
   - Commit changes
4. **GitHub Pages Aktiválás**:
   - Settings > Pages
   - Deploy from: main branch
   - Folder: / (root)
   - Custom domain: `form.digitallagentur.at` (opcionális)

### Lépés 5: DNS Konfigurálás (ha custom domain)
```
Rekord típusa: CNAME
Név: form
Érték: [USERNAME].github.io
TTL: 3600
```

---

## 🧪 Tesztelés

### Helyi Tesztelés (böngészőben)

1. **Nyisd meg az index.html-t böngészőben**
   ```
   File > Open > index.html
   ```

2. **Töltsd ki a formát**
   - Személyes adatok: Név, E-mail
   - Szekciók: Legalább egy kérdésre válaszolj

3. **Klikk: "ÉRTÉKELÉS ELKÜLDÉSE"**

4. **Várj 5-10 másodpercet**
   - FormSubmit.co feldolgozza
   - E-mail érkezik: tamas.toth@metallagentur.at
   - Success üzenet megjelenik

### GitHub Pages Tesztelés

1. **A forma elérhető**: https://form.digitallagentur.at/
2. **Töltsd ki és küldd el**
3. **Verifikálás**: E-mail megérkezik

---

## 📧 E-mail Feldolgozás

### FormSubmit.co Workflow:

1. **Ügyfél kitölt egy formát**
   ```
   Név: Kovács János
   E-mail: janos@example.com
   Szöveg: Ausztriai piacra lépéshez szeretnék segítséget
   ```

2. **Klikk: "ÉRTÉKELÉS ELKÜLDÉSE"**
   ```
   POST → https://formsubmit.co/tamas.toth@metallagentur.at
   ```

3. **FormSubmit.co feldolgozza**
   - Ellenőrzés: CAPTCHA nincs (disabled)
   - Adatok: HTML email formátumban
   - Tárgy: "Digitális Entitás Audit - Kovács János"

4. **E-mail érkezik**
   ```
   To: tamas.toth@metallagentur.at
   From: Kovács János <janos@example.com>
   Subject: Digitális Entitás Audit - Kovács János
   
   [Form adatok HTML táblázatban]
   ```

5. **Válasz küldése (opcionális)**
   - FormSubmit.co automatikusan beállítja a Reply-To-t
   - Egyszerűen válaszolhatsz az e-mailre

---

## ⚙️ FormSubmit.co Konfigurálás

### Hidden Inputs Magyarázata

```html
<!-- Tárgy az e-mailhez -->
<input type="hidden" name="_subject" value="Digitális Entitás Audit - Mag. Tamás Tóth">

<!-- CAPTCHA kikapcsolása (ingyenes verzió) -->
<input type="hidden" name="_captcha" value="false">

<!-- HTML email template -->
<input type="hidden" name="_template" value="html">

<!-- Redirect sikeres submit után -->
<input type="hidden" name="_next" value="https://form.digitallagentur.at/">
```

### Testreszabási Lehetőségek

Ha később módosítani szeretnél:

1. **Tárgy módosítása**: `_subject` input
2. **Email cím módosítása**: Form `action` attribute
3. **Redirect URL módosítása**: `_next` input
4. **Más beállítások**: https://formsubmit.co/docs

---

## 🔒 Biztonsági Megjegyzések

✅ **HTTPS**: FormSubmit.co SSL-t használ  
✅ **GDPR**: Csak szükséges adatokat küld  
✅ **Spam szűrés**: Beépített, aktív  
✅ **Rate limiting**: Automatikus védelem  
✅ **No tracking**: Nincsenek harmadik féltől való követők

---

## 📞 Támogatás

### Ha Problémák Vannak:

1. **Forma nem küldi az e-mailt**
   - Nézz meg: HTTPS-en van-e?
   - Ellenőrizd: Email cím helyesen?
   - Tesztelj: FormSubmit.co demó formával

2. **E-mail nem érkezik**
   - Nézd meg: Spam mappa
   - Várakozz: 5-10 perc, majd újra próbálkozz
   - Tesztelj: Formsubmit.co support

3. **GitHub Pages nem működik**
   - Ellenőrizd: DNS beállítások (CNAME)
   - Várakozz: 24-48 óra DNS propagációra
   - Tesztelj: https://form.digitallagentur.at/

---

## 📊 Verzió Információk

- **Projekt**: Digitális Entitás Audit Framework
- **Verzió**: 1.0.0
- **Form Backend**: FormSubmit.co
- **E-mail Címzett**: tamas.toth@metallagentur.at
- **Fejléc**: Mag. Tamás Tóth | Metallagentur.at
- **Kiadás**: 2026-05-10

---

## ✨ Előnyök

✅ **Egyszerű**: Nincs backend szükséges  
✅ **Ingyenes**: Korlátlan e-mail küldés  
✅ **Megbízható**: FormSubmit.co stabil  
✅ **GDPR-kompatibilis**: Adatkezelés biztonságos  
✅ **Gyors**: Azonnali e-mail küldés  
✅ **Professzionális**: HTML email template  

---

## 🎯 Következő Lépések

1. ✅ ZIP letöltése
2. ✅ Kicsomagolás
3. ✅ GitHub feltöltés (web UI-n)
4. ✅ GitHub Pages aktiválás
5. ✅ DNS beállítás (opcionális)
6. ✅ Tesztelés

---

**© 2026 Mag. Tamás Tóth | Metallagentur GmbH**  
**GDPR-kompatibilis | CC BY-NC-ND 4.0**

