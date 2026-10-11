# Portfolio — Tsadok Adido

Portfolio statique bilingue FR/EN, HTML/CSS/JavaScript vanilla, hébergé sur GitHub Pages.

## Structure
- `index.html` : structure sémantique des sections.
- `assets/css/styles.css` : design system « Atelier Bénin × Constructeur », thèmes clair/sombre et responsive.
- `assets/js/main.js` : rendu depuis les JSON, langue et thème persistants.
- `data/*.json` : contenu éditorial bilingue.
- `admin/` : interface Decap CMS et schéma des collections.
- `assets/cv/` : CV français et anglais attendus.
- `assets/img/` : médias et captures d’interface à venir.

## Développement local
Les données sont chargées avec `fetch()`; il faut servir le dossier via un serveur HTTP local (pas ouvrir `index.html` en `file://`). Par exemple : `python -m http.server 8000`, puis ouvrir `http://localhost:8000`.

## Déploiement
Le site est destiné à GitHub Pages depuis la branche `main`. Après revue de la branche de refonte, fusionner les changements vers `main`. Les chemins sont relatifs pour fonctionner sous le sous-chemin du dépôt GitHub Pages.

## Decap CMS — authentification à finaliser
GitHub Pages ne fournit pas de callback OAuth. La configuration CMS attend un proxy OAuth externe et gratuit, par exemple un Cloudflare Worker. Le champ `backend.base_url` dans `admin/config.yml` est volontairement un repère de configuration et doit être remplacé par l’URL réelle du Worker avant d’utiliser l’admin.

1. Créer une GitHub OAuth App dans les paramètres développeur GitHub.
2. Déployer un proxy OAuth Decap compatible sur Cloudflare Workers et y configurer le Client ID et le Client Secret comme secrets (ne jamais les committer dans ce dépôt).
3. Définir l’URL de callback de l’OAuth App selon la documentation du proxy.
4. Remplacer `https://YOUR-CLOUDFLARE-WORKER.workers.dev` par l’URL réelle dans `admin/config.yml`.
5. Déployer le site sur `main`, puis tester `/admin/` en production avec un compte ayant les droits d’écriture sur ce dépôt.

La documentation officielle Decap décrit le flux proxy OAuth : https://decapcms.org/docs/backends-overview/. Un exemple de Worker communautaire est disponible ici : https://github.com/sterlingwes/decap-proxy.

## Assets attendus
Les PDF `CV_Tsadok_Adido_FR.pdf` et `CV_Tsadok_Adido_EN.pdf` doivent être placés dans `assets/cv/`. Le bouton CV reste masqué tant que le PDF correspondant à la langue active n’existe pas. Les liens Instagram/Discord et les captures UX restent absents tant que les vraies informations ne sont pas fournies.
