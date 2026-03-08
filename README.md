# GitHub Repos Viewer

Page web listant les dépôts GitHub de **nmarchand73** avec liens, dates de création, infos clés et recherche.

## 🌐 Publication

**GitHub Pages** : [https://nmarchand73.github.io/repositories_toc/](https://nmarchand73.github.io/repositories_toc/)

## Lancement local

### Option 1 — Ouverture directe
Ouvrir `index.html` dans le navigateur (double-clic ou `start index.html`).

### Option 2 — Serveur local (pour rafraîchir via API)
```powershell
cd c:\DATA\DEV\PROJETS\repositories_toc
python -m http.server 8080
# Puis ouvrir http://localhost:8080
```

## Fonctionnalités

- **Recherche** : filtre par nom, description, langage, topics
- **Tri** : par date (récent/ancien), nom (A-Z/Z-A), étoiles
- **Infos affichées** : lien, date de création, langage, étoiles, badge fork
- **Rafraîchir** : charge les données en direct depuis l’API GitHub (nécessite de servir la page en HTTP)
