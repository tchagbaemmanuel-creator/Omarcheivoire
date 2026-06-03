# Site vitrine O'Marché Ivoire

Page statique : présentation, catalogue démo et **téléchargement de l'application Android**.

## En ligne

- **Render** : https://omarcheivoire.onrender.com/
- **API mobile** : https://appomarcheivoire.onrender.com

## Déploiement Render

1. Créer un service **Static Site** lié à ce dépôt ([Omarcheivoire](https://github.com/tchagbaemmanuel-creator/Omarcheivoire)).
2. Branche `main`, dossier racine.
3. Le fichier `render.yaml` configure la publication statique.

## Lien APK (permanent)

Le bouton « Télécharger » pointe vers **`/downloads/omarche-ivoire.apk`** (fichier sur le site, pas de lien EAS temporaire).

Après un build EAS :

```bash
cd ../omarche-main/mobile
npm run build:android:preview
npm run sync:apk-to-site
cd ../../omarche-site
git add downloads/omarche-ivoire.apk site-config.js
git commit -m "Mise à jour APK"
git push
```

Render redéploie automatiquement. Si l’APK dépasse 100 Mo, utiliser [Git LFS](https://git-lfs.github.com/) pour `downloads/*.apk`.

## Fichiers

| Fichier | Rôle |
|---------|------|
| `index.html` | Site complet |
| `site-config.js` | URL APK + API |
| `assets/logo-omarche-ivoire.png` | Logo |
| `render.yaml` | Config Render |

## Développement local

Ouvrir `index.html` dans un navigateur, ou :

```bash
npx serve .
```
