
# Documentation : Projet de Conversion PNG en WebP

Ce projet permet de convertir des images PNG en WebP pour améliorer les performances des sites web. Ce format est plus léger et adapté à une utilisation sur le web, garantissant un meilleur temps de chargement des pages.

## Structure du Dossier

```
clientsPngToWebp/
├── clients/
│   ├── client-1.png
│   ├── client-2.png
│   ├── client-3.png
│   ├── client-4.png
│   ├── client-5.png
│   ├── client-6.png
│   ├── client-7.png
│   ├── client-8.png
```

### Détails de la structure :
- **`clients/`** : Contient les fichiers PNG originaux que vous souhaitez convertir.
- **Format de fichier :** `.png`

---

## Objectif du Projet

Le but de ce projet est de convertir des fichiers image au format PNG en WebP. Le format WebP est choisi pour sa capacité à réduire la taille des fichiers tout en maintenant une qualité élevée. 

### Pourquoi WebP ?
- **Compression supérieure** : Réduit la taille des images jusqu'à 50% par rapport au PNG sans perte notable de qualité.
- **Support moderne** : Bien pris en charge par la plupart des navigateurs modernes.
- **Temps de chargement réduit** : Améliore la performance des sites web.

---

## Processus de Conversion

Les fichiers PNG dans le dossier `clients/` ont été convertis au format **WebP** avec une qualité de compression de **80%** pour un compromis entre taille et qualité.

### Commande utilisée pour la conversion :
```bash
sharp input.png --output output.webp --quality 80
```

---

## Fichiers Convertis

Après conversion, les fichiers WebP sont stockés dans un répertoire séparé (`clientsPngToWebp_converted/`).

### Exemple de structure du dossier après conversion :
```
clientsPngToWebp_converted/
├── client-1.webp
├── client-2.webp
├── client-3.webp
├── client-4.webp
├── client-5.webp
├── client-6.webp
├── client-7.webp
├── client-8.webp
```

---

## Exemple d'Utilisation

Vous pouvez utiliser les images WebP directement dans votre HTML comme suit :

```html
<img src="clientsPngToWebp_converted/client-1.webp" alt="Client 1">
```

### Fallback pour les anciens navigateurs :

Si vous devez supporter des navigateurs plus anciens qui ne prennent pas en charge WebP, vous pouvez utiliser le tag `<picture>` pour fournir un fallback en PNG :

```html
<picture>
  <source srcset="clientsPngToWebp_converted/client-1.webp" type="image/webp">
  <img src="clients/client-1.png" alt="Client 1">
</picture>
```

---

## Recommandations pour Aller Plus Loin

### 1. **Optimisation de la Taille des Fichiers**
   Vous pouvez encore réduire la taille des images en utilisant un outil comme **ImageOptim** ou **TinyPNG**.

### 2. **Automatisation de la Conversion**
   Utilisez un script d'automatisation pour convertir de nouveaux fichiers PNG en WebP au fur et à mesure de leur ajout. Par exemple, un script Node.js qui surveille le dossier `clients/` et effectue la conversion dès qu'un nouveau fichier est ajouté.

### 3. **Lazy Loading des Images**
   Pour améliorer les performances, activez le **lazy loading** des images :
   ```html
   <img src="clientsPngToWebp_converted/client-1.webp" loading="lazy" alt="Client 1">
   ```

---

## Conclusion

Ce projet offre une méthode simple et efficace pour convertir des fichiers PNG en WebP. Il permet d'améliorer les performances du site en réduisant la taille des images tout en conservant une qualité élevée. Vous pouvez désormais intégrer ces fichiers WebP dans vos projets web pour optimiser leur temps de chargement.

---
