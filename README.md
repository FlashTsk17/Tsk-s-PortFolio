# Tsadok ADIDO — Portfolio

**Dev · Infographie · UX/UI · Fondateur de Tsk's Tech Services**

---

## 🚀 Déploiement sur GitHub Pages — 5 minutes

### Structure du repo
```
tsadok-portfolio/        ← nom suggéré pour le repo
├── index.html           ← fichier principal
└── tsadok.jpg           ← ta photo (déjà en place)
```

### Étapes

**1. Crée le repo GitHub**
- Va sur github.com → New repository
- Nom : `tsadok-portfolio` (ou `FlashTsk17.github.io` pour URL courte)
- Visibilité : Public
- Ne coche rien d'autre → Create repository

**2. Push les fichiers**
```bash
git init
git add .
git commit -m "🚀 Portfolio initial — Tsadok ADIDO"
git branch -M main
git remote add origin https://github.com/FlashTsk17/tsadok-portfolio.git
git push -u origin main
```

**3. Active GitHub Pages**
- Dans ton repo → Settings → Pages
- Source : `Deploy from a branch`
- Branch : `main` / `/ (root)`
- Save

**4. Ton portfolio est live !**
URL : `https://flashtsk17.github.io/tsadok-portfolio`

---

## 🔗 Liens à compléter dans index.html

Recherche `REMPLACE` dans index.html pour trouver les 3 endroits à compléter :

| Élément | Action |
|---|---|
| `Formspree` | Va sur formspree.io → New form → copie l'ID |
| `Mon CV` (nav) | Lien Google Drive de ton CV PDF |
| `LinkedIn` | Ton URL LinkedIn |
| `Instagram` | Ton URL Instagram |
| Liens GitHub projets | URLs de tes repos publics |

---

## 📸 Photo
Ta photo `tsadok.jpg` est déjà branchée. ✅

---

## 📬 Formspree — Brancher le formulaire

1. Va sur [formspree.io](https://formspree.io)
2. Crée un compte gratuit
3. New Form → donne un nom (ex: "Portfolio Contact")
4. Copie l'endpoint : `https://formspree.io/f/xxxxxxxx`
5. Dans `index.html`, cherche `REMPLACE_PAR_TON_ID` et remplace par ton ID

Le formulaire enverra les messages directement sur `adidomahukpeou@gmail.com`.

---

*Tsk's Tech Services · Cotonou, Bénin · 2026*
