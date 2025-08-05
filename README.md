# Portfolio de Charles Kone - Guide d'hébergement sur GitHub Pages

Ce document vous guide pas à pas pour héberger votre portfolio personnel sur GitHub Pages, un service gratuit de GitHub qui permet d'héberger des sites web statiques.

## Prérequis

Avant de commencer, assurez-vous d'avoir :
- Un compte GitHub (gratuit) - créez-en un sur [github.com](https://github.com)
- Git installé sur votre ordinateur
- Les fichiers de votre portfolio (index.html, style.css, script.js)

## Étape 1 : Création du repository GitHub

1. **Connectez-vous à GitHub** et cliquez sur le bouton "New" ou "+" en haut à droite pour créer un nouveau repository.

2. **Nommez votre repository** : 
   - Option 1 (recommandée) : `votre-nom-utilisateur.github.io` (remplacez par votre nom d'utilisateur GitHub)
   - Option 2 : `portfolio` ou tout autre nom de votre choix

3. **Configurez le repository** :
   - Assurez-vous qu'il soit **Public**
   - Cochez "Add a README file"
   - Cliquez sur "Create repository"

## Étape 2 : Upload des fichiers du portfolio

### Méthode 1 : Via l'interface web GitHub (plus simple)

1. Dans votre nouveau repository, cliquez sur "uploading an existing file" ou "Add file" > "Upload files"

2. Glissez-déposez ou sélectionnez vos fichiers :
   - `index.html`
   - `style.css`
   - `script.js`

3. Ajoutez un message de commit comme "Ajout du portfolio initial"

4. Cliquez sur "Commit changes"

### Méthode 2 : Via Git en ligne de commande

```bash
# Cloner le repository
git clone https://github.com/votre-nom-utilisateur/votre-repository.git
cd votre-repository

# Copier vos fichiers dans le dossier
# (copiez index.html, style.css, script.js dans ce dossier)

# Ajouter les fichiers
git add .

# Créer un commit
git commit -m "Ajout du portfolio initial"

# Pousser vers GitHub
git push origin main
```

## Étape 3 : Activation de GitHub Pages

1. **Accédez aux paramètres** : Dans votre repository, cliquez sur l'onglet "Settings"

2. **Trouvez la section Pages** : Faites défiler vers le bas jusqu'à la section "Pages" dans le menu de gauche

3. **Configurez la source** :
   - Source : Sélectionnez "Deploy from a branch"
   - Branch : Sélectionnez "main" (ou "master" selon votre configuration)
   - Folder : Laissez "/ (root)"

4. **Sauvegardez** : Cliquez sur "Save"

## Étape 4 : Accès à votre site

Après quelques minutes (généralement 5-10 minutes), votre site sera accessible à l'adresse :

- Si votre repository s'appelle `votre-nom-utilisateur.github.io` : 
  `https://votre-nom-utilisateur.github.io`

- Si votre repository a un autre nom (ex: "portfolio") :
  `https://votre-nom-utilisateur.github.io/nom-du-repository`

## Étape 5 : Mise à jour du portfolio

Pour mettre à jour votre portfolio :

1. **Modifiez vos fichiers** localement
2. **Uploadez les modifications** via l'interface GitHub ou Git
3. **Attendez quelques minutes** pour que les changements soient visibles

### Via l'interface web :
- Cliquez sur le fichier à modifier
- Cliquez sur l'icône crayon (Edit)
- Effectuez vos modifications
- Commitez les changements

### Via Git :
```bash
# Après avoir modifié vos fichiers
git add .
git commit -m "Mise à jour du portfolio"
git push origin main
```

## Personnalisation avancée

### Domaine personnalisé (optionnel)

Si vous possédez un nom de domaine, vous pouvez l'utiliser :

1. Dans les paramètres Pages, ajoutez votre domaine dans "Custom domain"
2. Configurez les DNS de votre domaine pour pointer vers GitHub Pages
3. Activez "Enforce HTTPS" pour la sécurité

### Optimisations SEO

Pour améliorer le référencement de votre portfolio :

1. **Ajoutez un fichier `robots.txt`** :
```
User-agent: *
Allow: /
Sitemap: https://votre-domaine.com/sitemap.xml
```

2. **Créez un fichier `sitemap.xml`** :
```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://votre-domaine.com/</loc>
    <lastmod>2024-01-01</lastmod>
    <priority>1.0</priority>
  </url>
</urlset>
```

3. **Optimisez les métadonnées** dans votre `index.html` :
```html
<meta name="description" content="Portfolio de Charles Kone - Développeur Web Full-Stack">
<meta name="keywords" content="développeur web, portfolio, HTML, CSS, JavaScript, Python, Django">
<meta property="og:title" content="Charles Kone - Développeur Web">
<meta property="og:description" content="Portfolio professionnel de Charles Kone">
<meta property="og:image" content="https://votre-domaine.com/image-preview.jpg">
```

## Dépannage

### Problèmes courants

**Le site ne s'affiche pas :**
- Vérifiez que GitHub Pages est activé dans les paramètres
- Assurez-vous que votre fichier principal s'appelle `index.html`
- Attendez 10-15 minutes après l'activation

**Erreur 404 :**
- Vérifiez l'URL (respectez la casse)
- Assurez-vous que les fichiers sont dans la branche correcte

**Les modifications ne s'affichent pas :**
- Videz le cache de votre navigateur (Ctrl+F5)
- Attendez quelques minutes pour la propagation

**Problèmes de CSS/JS :**
- Vérifiez les chemins relatifs dans vos fichiers
- Assurez-vous que tous les fichiers sont uploadés

### Support

- [Documentation officielle GitHub Pages](https://docs.github.com/en/pages)
- [Communauté GitHub](https://github.community/)
- [Support GitHub](https://support.github.com/)

## Bonnes pratiques

1. **Sauvegardez régulièrement** : Commitez vos changements fréquemment
2. **Utilisez des messages de commit clairs** : "Ajout section projets", "Correction bug navigation"
3. **Testez localement** : Vérifiez votre site avant de le publier
4. **Optimisez les images** : Compressez les images pour un chargement plus rapide
5. **Maintenez à jour** : Mettez régulièrement à jour votre portfolio

## Sécurité

- **Ne jamais commiter** d'informations sensibles (mots de passe, clés API)
- **Utilisez HTTPS** : Activez "Enforce HTTPS" dans les paramètres
- **Surveillez votre repository** : GitHub vous notifiera des vulnérabilités

Votre portfolio est maintenant prêt à être partagé avec le monde entier ! N'hésitez pas à partager le lien sur vos réseaux sociaux et dans vos candidatures.

