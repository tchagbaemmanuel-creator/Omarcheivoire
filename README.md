# Site vitrine O'Marché Ivoire

Page statique : présentation, catalogue démo et **téléchargement de l'application Android**.

## En ligne

- **Render** : https://omarcheivoire.onrender.com/
- **API mobile** : https://appomarcheivoire.onrender.com

## Déploiement Render

1. Créer un service **Static Site** lié à ce dépôt ([Omarcheivoire](https://github.com/tchagbaemmanuel-creator/Omarcheivoire)).
2. Branche `main`, dossier racine.
3. Le fichier `render.yaml` configure la publication statique.

## Mettre à jour le lien APK

Après un build EAS :

```bash
cd ../omarche-main/mobile
npx eas build -p android --profile preview
npx eas build:list
```

Copier l'URL **Application Archive** (`.apk`) dans `site-config.js` → `APK_DOWNLOAD_URL`, puis commit et push.

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
