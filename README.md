# GitHub Repos Viewer (`repositories_toc`)

Page web listant les dépôts GitHub de **nmarchand73** avec liens, dates de création, infos clés, catégories et recherche.

**Déploiement en ligne :** après activation de GitHub Pages (voir ci-dessous), le site est généralement disponible à  
`https://nmarchand73.github.io/repositories_toc/` (si le dépôt s’appelle `repositories_toc`).

## GitHub Pages

1. Pousser ce dépôt sur GitHub : `https://github.com/nmarchand73/repositories_toc` (ou le nom de ton dépôt).
2. **Settings → Pages → Build and deployment**
   - **Source** : **GitHub Actions** (pas « Deploy from a branch » si tu utilises le workflow).
3. Le workflow **Deploy GitHub Pages** (`.github/workflows/pages.yml`) se déclenche à chaque push sur `main` ou `master`.
4. À la fin du premier run, l’URL du site apparaît dans l’onglet **Actions** et dans **Settings → Pages**.

Sans workflow : tu peux aussi choisir **Deploy from a branch** → branche `master` / `main`, dossier **`/` (root)** — `index.html` à la racine suffit.

## Lancement local

### Option 1 — Ouverture directe
Ouvrir `index.html` dans le navigateur (double-clic ou `start index.html`).

### Option 2 — Serveur local (pour rafraîchir via API)
```powershell
cd c:\DATA\DEV\PROJETS\github-repos
python -m http.server 8080
# Puis ouvrir http://localhost:8080
```

## Fonctionnalités

- **Recherche** : filtre par nom, description, langage, topics, catégorie
- **Affichage par catégories** avec descriptions
- **Token GitHub** (optionnel) : pour inclure les repos privés
- **Rafraîchir** : charge les données en direct depuis l’API GitHub (recommandé en HTTP)

## Mettre à jour la liste hors ligne

Le tableau `FALLBACK_REPOS` dans `index.html` est synchronisé avec l’API publique GitHub (repos publics). Pour régénérer : appeler l’API `GET /users/nmarchand73/repos?per_page=100` et mettre à jour les entrées + `REPO_CATEGORY` / `REPO_DESCRIPTIONS` pour les nouveaux dépôts.
