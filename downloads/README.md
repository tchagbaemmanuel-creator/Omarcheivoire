# APK Android

Fichier servi en permanence par le site : **`omarche-ivoire.apk`**

Après chaque build EAS, copier le fichier ici (commit Git pour que Render le serve) :

```powershell
cd ..\omarche-main\mobile
npm run sync:apk-to-site
```

Puis commit + push du dépôt **Omarcheivoire** (uniquement si l’APK est ajouté via Git LFS ou release — voir README racine).
