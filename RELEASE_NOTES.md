# Form-Main-6 — 2026-06-12 Update (FINAL)

## ✅ Frissítések — A teljes GDPR/AVV megfelelőséggel

### 1. Jelszókapu → GDPR-elfogadásos kapu

- Az oldal bevezetője megmarad („Ez nem egy gyors űrlap...")
- A jelszó-form helyett háromnyelvű GDPR-elfogadásos kapu
- Az **oldal csak akkor oldódik fel**, ha az `consent_0` checkboxot (Art. 13-as tájékoztatás elfogadása) pipálják be

### 2. 30 napos törlési ciklus

**Az audit-projekt kezdetéből kiindulva:**

| Adat | Kezelő | Megőrzés | Törlés után |
|------|--------|----------|-----------|
| **Kérdőív kitöltött adatai** | Mag. Tamás Tóth e.U. | 30 nap | Teljes törlés |
| **Internet-kutatás adatai** | Szerződéses alvállalkozó | 30 nap | Teljes törlés |
| **Stratégiai elemzés** | Szerződéses alvállalkozó | — | **Nem törlésre kerül** (szerzői munka) |
| **Audit HTML-dokumentum** | Alvállalkozó szerzői joga | — | **Nem törlésre kerül** (szállított termék) |
| **Számlázási adatok** | Mag. Tamás Tóth e.U. | 7 év | BAO § 132 után törlés |

### 3. Alvállalkozó szellemi tulajdona

- Az **alvállalkozó szerzői joga**: az internet-kutatás, a stratégiai elemzés, az HTML audit-dokumentum
- Mag. Tamás Tóth e.U.: csak az audit-kérdőív kitöltött adatait és az eredmény-dokumentumot látja
- Az alvállalkozó: az ő szellemi munkája (nem törlésre kerül)

### 4. Betűtípusok Apple-stílusra

- **Serif:** New York (Apple natív)
- **Sans:** San Francisco (via `-apple-system`)
- Google Fonts eltávolítva

### 5. Részletes GDPR-dokumentum oldal

**adatvedelem.html** — 13 nyelvű szekció:
- Adatkezelő és feldolgozási útvonal (Tamás + alvállalkozó + AI)
- 30 napos törlési procedúra részletesen
- Alvállalkozó szellemi tulajdona külön fejezet
- Támogatott: HU/EN/DE nyelvváltó, nyomtatás, PDF

### 6. Frissített GDPR_COMPLIANCE.md

- **30 napos törlési ciklus** dokumentálva
- **Alvállalkozó szerzői joga** kifejezetten megnevezve
- **Törlési procedúra** részletezve: ki, mikor, hogyan, miért
- **Szerzői jog és szellemi tulajdon** külön fejezet
- **Verz. 2.0** — termelésre kész

---

## 📦 Tartalma

```
form-main-6-updated.zip (161 KB)
├── index.html                    (GDPR-elfogadásos kapu, Apple-betűk, 30-nap info)
├── adatvedelem.html              (Részletes 3-nyelvű privacy oldal, 30-nap törlés)
├── GDPR_COMPLIANCE.md            (Teljes dokumentáció, 30-nap ciklus + alvállalkozó IP)
└── [Összes eredeti dokumentum]
```

---

## 🚀 Telepítés

1. Csomagold ki a `form-main-6-updated.zip`-et
2. A `form-main-6` mappát helyezd a GitHub Pages repository gyökerébe
3. Push a módosítást — az oldal automatikusan live lesz

---

## ✅ GDPR/AVV Compliance Checklist

- ✓ **Art. 13 tájékoztatás** — az oldal GDPR-paneljában és az adatvedelem.html-ben
- ✓ **Jogalapok** — Art. 6 szerződés, jogos érdek, jogi kötelezettség
- ✓ **Adatkategóriák** — kapcsolattartás, cég, számlázás, technikai
- ✓ **Art. 9 kizárás** — különleges kategóriájú adatok tiltva
- ✓ **Címzetek** — GitHub Pages, Google Apps Script/Workspace, Google Fonts, alvállalkozó, AI
- ✓ **Nemzetközi adattovábbítás** — SCC + EU–US DPF
- ✓ **Adatmegőrzés** — 30 nap (projekt) / 7 év (számlázás)
- ✓ **Törlési procedúra** — részletez, naplózott, biztosan végrehajtott
- ✓ **Érintetti jogok** — Art. 15–22, kontakt megadva
- ✓ **Szerzői jog + szellemi tulajdon** — alvállalkozó joga védelme
- ✓ **Biztonsági intézkedések** — HTTPS, 2FA, jelszókapu → GDPR-kapu
- ✓ **Incidenskezelés** — 72 órás bejelentési kötelezettség

---

## 📋 Verziók

| Verzió | Dátum | Állapot |
|--------|-------|--------|
| 1.0 | 2026-05-08 | FormSubmit-alapú |
| 2.0 | 2026-06-12 | **GitHub Pages + Google Apps Script, 30-nap törlés, alvállalkozó IP** |

---

**Status:** ✅ Termelésre kész  
**GDPR/AVV:** ✅ Teljes megfelelőség dokumentálva  
**Szerzői jog:** ✅ Alvállalkozó szellemi tulajdona védelme  

© 2026 Mag. Tamás Tóth e.U.
