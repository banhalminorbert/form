# GitHub Deployment Guide — Digitális Entitás Audit Framework

## 🚀 Lépésről Lépésre: GitHub Pages Deployment

### 1. GitHub Repository Létrehozása

```bash
# GitHub-on belül (web felületen):
1. Naptál (Login) https://github.com
2. Új repository: "New" > "New Repository"
3. Repository név: digital-entity-audit (vagy saját választás)
4. Leírás: "Professional Digital Identity & Reputation Strategy Assessment Tool"
5. Public (nyilvános)
6. "Create Repository"
```

### 2. Fájlok Feltöltése (Git Parancsokkal)

```bash
# Clone az új repositoryt
git clone https://github.com/[USERNAME]/digital-entity-audit.git
cd digital-entity-audit

# Másolj minden fájlt ide
cp -r /mnt/user-data/outputs/* .

# Git konfig
git config user.name "Tamas Toth"
git config user.email "[your-email@example.com]"

# Hozzáadás és commit
git add .
git commit -m "Initial commit: Digital Entity Audit Framework v1.0 — GDPR-compliant"

# Push GitHub-ra
git push origin main
```

### 3. GitHub Pages Aktiválása

**Web felületen a GitHub-ban:**

```
1. Repository Settings (fogaskerék ikon)
2. Görgetess le: "GitHub Pages"
3. Source: "Deploy from a branch"
4. Branch: "main"
5. Folder: "/ (root)"
6. Save
```

**Vagy parancssorból (Advanced):**
```bash
# GitHub CLI-vel
gh repo edit --enable-wiki=false --enable-projects=false --enable-issues=false
gh repo view --web
```

### 4. Deploy-t Ellenőrizni

```bash
# GitHub Pages URL-je:
https://[USERNAME].github.io/digital-entity-audit/

# Vagy saját domain-nal (opcionális):
https://digital-entity-audit.your-domain.com
```

---

## 📁 Repository Struktúra (GitHub-on)

```
digital-entity-audit/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   └── bug_report.md
│   └── PULL_REQUEST_TEMPLATE.md
├── docs/
│   ├── Digital_Entity_Audit_Template.md
│   ├── ÚTMUTATÓ.txt
│   └── Technikai_Specifikáció.md
├── .editorconfig
├── .gitignore
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── GDPR_COMPLIANCE.md
├── IMPRESSUM.md
├── LICENSE.md
├── README.md
├── TERMS_OF_SERVICE.md
├── index.html (FŐOLDAL)
├── package.json
└── GITHUB_DEPLOYMENT_GUIDE.md (ez a fájl)
```

---

## 🔐 GitHub Security Settings

**Repository Settings > Security & analysis:**

```
✓ Enable Dependabot alerts
✓ Enable Dependabot security updates
✓ Enable code scanning with CodeQL
✓ Enable secret scanning
✓ Block force pushes to main branch
✓ Require status checks before merging
```

---

## 🌐 Custom Domain Beállítása (Opcionális)

**Ha saját domain-t szeretnél (pl. audit.metallagentur.at):**

### 1. DNS Record Hozzáadása

A domain-t kezelő platformon (pl. Cloudflare, GoDaddy):

```
Type: CNAME
Name: audit
Target: [USERNAME].github.io
TTL: 3600
```

### 2. GitHub Pages Konfigurálása

```
Settings > Pages > Custom Domain
```

Írj be: `audit.metallagentur.at`

### 3. SSL/TLS Aktiválása

```
Settings > Pages
[X] Enforce HTTPS
```

---

## 📊 GitHub Actions (Opcionális — Automation)

Automatizált teszteléshez hozz létre `.github/workflows/validate.yml`:

```yaml
name: Validate HTML & GDPR Compliance

on: [push, pull_request]

jobs:
  validate:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      
      - name: Validate HTML
        run: |
          npm install -g html-validate
          html-validate index.html
      
      - name: Check GDPR Compliance
        run: |
          echo "GDPR Compliance Check"
          grep -q "GDPR" GDPR_COMPLIANCE.md || exit 1
          grep -q "[your-email@example.com]" index.html || exit 1
      
      - name: Lighthouse Audit
        run: |
          npm install -g lighthouse
          lighthouse index.html --output-path=lighthouse-report.html
```

---

## 📝 Verziók és Release-k

### Verziózás (Semantic Versioning)

```
1.0.0  = Major.Minor.Patch

1.0.0  → Kezdeti kibocsátás
1.1.0  → Új szekciók, jellemzők
1.0.1  → Bugfix, kis javítások
2.0.0  → Töréspontos változások (új GDPR verzió, etc.)
```

### Release-k Létrehozása

```bash
# GitHub-on a "Releases" fül:
1. "Create a new release"
2. Tag version: v1.0.0
3. Release title: "Digital Entity Audit Framework v1.0"
4. Leírás: Changelog és új jellemzők
5. Assets: Töltsd fel a PDF-eket, ha szükséges
6. "Publish release"
```

---

## 🤝 Hozzájárulás (Contributing)

Hozz létre `CONTRIBUTING.md`:

```markdown
# Hozzájárulás (Contributing)

Köszönjük az érdeklődésedet!

## Hogyan járulhattok hozzá?

1. Fork a repositoryt
2. Hozz létre egy új branch: `git checkout -b feature/[feature-name]`
3. Végezz el módosításokat
4. Commit: `git commit -m "Add [feature name]"`
5. Push: `git push origin feature/[feature-name]`
6. Nyiss egy Pull Request

## Irányelvek

- Betartsd a CC BY-NC-ND 4.0 licencet
- Ne módosítsd a jogi dokumentumokat (GDPR, Terms, etc.) önkényesen
- Angolul vagy magyarul írj
- Teszt a módosítások után

## Kód Stílusa

- 2 szóköz indentáció
- UTF-8 encoding
- HTML5 validáció
- GDPR compliance ellenőrzés
```

---

## 🔒 GitHub Secrets (Ha Szükséges)

**Formspree Integration (E-mail Form):**

```bash
# Settings > Secrets and variables > Actions
# Új secret hozzáadása:
Name: FORMSPREE_ENDPOINT
Value: https://formspree.io/f/[FORM_ID]
```

---

## 📈 Monitorozás és Analytics

### GitHub Stats

```
Repository Insights:
- Traffic (Views, Clones)
- Community (Stars, Forks, Issues)
- Pulse (Activity)
```

### Lighthouse Monitoring

```bash
# Heti Lighthouse teszt:
npm run lighthouse > lighthouse-report.html
```

---

## 🆘 Troubleshooting

### GitHub Pages nem működik

```bash
# 1. Ellenőrizd a Settings:
   - Pages: Source = "main branch, /root folder"
   - Custom domain: helyesen konfigurálva?

# 2. Ellenőrizd a DNS:
   nslookup audit.metallagentur.at
   # Kell mutatni a GitHub IP-ra

# 3. Ellenőrizd az SSL:
   https://audit.metallagentur.at
   # Nem kell hibát mutatni
```

### HTML validáció sikertelen

```bash
# Helyileg tesztelj:
npm run validate

# Javítsd a hibákat és commit:
git add .
git commit -m "Fix HTML validation errors"
git push origin main
```

---

## 📞 Támogatás és Kontakt

**Ha problémáid vannak:**

```
1. GitHub Issues: https://github.com/[USERNAME]/digital-entity-audit/issues
2. E-mail: [your-email@example.com]
3. Website: https://www.metallagentur.at
```

---

## ✅ Deployment Checklist

- [ ] GitHub account létrehozva
- [ ] Repository létrehozva (public)
- [ ] Fájlok feltöltve
- [ ] GitHub Pages aktiválva
- [ ] index.html elérhető: https://[USERNAME].github.io/digital-entity-audit/
- [ ] HTTPS működik
- [ ] Lighthouse audit > 90 pontszám
- [ ] GDPR compliance ellenőrzve
- [ ] README.md megjelenik
- [ ] LICENSE.md látható
- [ ] Impressum jó
- [ ] Formspree e-mail működik

---

## 🎉 Kész!

Az audit-keretrendszer GitHub Pages-en működik:

```
👉 https://[USERNAME].github.io/digital-entity-audit/
```

Köszönjük, hogy a Mag. Tamás Tóth e.U. audit-keretrendszert használod!

---

**© 2026 Mag. Tamás Tóth e.U. | CC BY-NC-ND 4.0 | GDPR-kompatibilis**
