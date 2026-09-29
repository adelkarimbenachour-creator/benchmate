# Mettre BenchMate en ligne gratuitement (avec droit d'usage commercial)

Ce dossier contient `index.html`, la version actuelle de BenchMate prête à héberger.
Vercel Hobby fonctionne très bien pour tester, mais son plan gratuit interdit
l'usage commercial. **GitHub Pages** offre l'équivalent (gratuit, HTTPS automatique,
fichier statique) sans cette restriction : tu peux t'en servir même si tu factures
l'accès plus tard.

## Option recommandée : GitHub Pages

1. Va sur [github.com](https://github.com) et crée un compte si tu n'en as pas.
2. Crée un nouveau dépôt (bouton **New**), nomme-le par exemple `benchmate`, coche **Public**.
3. Sur la page du dépôt, clique **Add file → Upload files**, glisse `index.html`
   (ce fichier, à la racine du dépôt, pas dans un sous-dossier), puis **Commit changes**.
4. Va dans **Settings → Pages** (menu de gauche).
5. Sous **Build and deployment → Source**, choisis **Deploy from a branch**.
6. Choisis la branche `main` et le dossier `/ (root)`, puis **Save**.
7. Attends 1 à 2 minutes. Ton adresse apparaît en haut de cette page, du style :
   `https://TON-PSEUDO.github.io/benchmate/`

Chaque fois que tu remplaces `index.html` dans le dépôt (via **Add file → Upload files**
à nouveau), le site se met à jour automatiquement en une minute environ.

## Alternative : Cloudflare Pages

Aussi gratuit et sans restriction d'usage commercial, avec un tableau de bord un peu
plus simple pour glisser-déposer un fichier :
1. [dash.cloudflare.com](https://dash.cloudflare.com) → **Workers & Pages → Create → Pages → Upload assets**.
2. Glisse `index.html`, donne un nom au projet, **Deploy**.
3. Tu obtiens une adresse `https://TON-PROJET.pages.dev`.

## Ce qui ne change pas

- Toujours aucune clé API stockée de mon côté : chaque visiteur entre la sienne
  (Gemini, Groq ou OpenRouter) dans « ⚙︎ IA gratuite », gardée dans son propre
  navigateur.
- La caméra, le QR code de connexion au smartphone et l'appel aux IA ont besoin
  du HTTPS : GitHub Pages et Cloudflare Pages le fournissent automatiquement,
  comme Vercel.
- Domaine personnalisé (ex. `benchmate.fr`) : possible gratuitement sur les deux
  (il faut juste acheter le nom de domaine séparément, ce n'est pas gratuit).

## Limite à garder en tête pour la suite

Toutes ces offres gratuites restent pensées pour un usage léger. Si l'appli
attire beaucoup de visiteurs ou que tu veux gérer des comptes utilisateurs et
protéger les clés API côté serveur (recommandé avant de vraiment vendre l'accès),
il faudra à un moment ajouter un petit serveur — ce que Vercel, Cloudflare et
GitHub Pages permettent tous, sur leurs offres payantes ou via des fonctions
serverless dans leurs offres gratuites limitées.
