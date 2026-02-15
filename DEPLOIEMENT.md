# 🚀 Guide de Déploiement - Faboulaagrobusiness

Ce guide explique comment déployer le site Faboulaagrobusiness en ligne.

## ✅ Fichiers de Configuration Créés

- `netlify.toml` - Configuration Netlify avec headers de sécurité et cache
- `.github/workflows/deploy.yml` - Workflow GitHub Actions pour GitHub Pages
- `.gitignore` - Fichiers à exclure du versioning

## 📦 Options de Déploiement

### Option 1: Netlify (Recommandé) 🌟

**Avantages:**
- ✅ Formulaire de contact fonctionnel automatiquement
- ✅ HTTPS automatique
- ✅ CDN global
- ✅ Déploiement automatique à chaque push

**Instructions:**

1. **Créer un compte Netlify**
   - Allez sur [netlify.com](https://netlify.com)
   - Inscrivez-vous gratuitement

2. **Connecter votre repository GitHub**
   - Cliquez sur "Add new site" → "Import an existing project"
   - Sélectionnez "GitHub"
   - Autorisez Netlify à accéder à votre repository
   - Sélectionnez `meliusmum-sketch/Faboulaagrobusiness`

3. **Configuration du déploiement**
   - Branch to deploy: `main`
   - Build command: *(laisser vide)*
   - Publish directory: `.`
   - Cliquez sur "Deploy site"

4. **Configuration du domaine (optionnel)**
   - Allez dans Site settings → Domain management
   - Ajoutez votre domaine personnalisé ou utilisez le sous-domaine Netlify

5. **Activer les formulaires**
   - Les formulaires sont déjà configurés avec `data-netlify="true"`
   - Netlify les détectera automatiquement

### Option 2: GitHub Pages 📄

**Avantages:**
- ✅ Gratuit et hébergé par GitHub
- ✅ Déploiement automatique configuré
- ✅ HTTPS automatique

**Limitations:**
- ⚠️ Le formulaire de contact ne fonctionnera pas (nécessite un service tiers)

**Instructions:**

1. **Merger la branche de développement**
   ```bash
   # Merger copilot/replace-index-html-with-gallery dans main
   git checkout main
   git merge copilot/replace-index-html-with-gallery
   git push origin main
   ```

2. **Activer GitHub Pages**
   - Allez sur le repository: https://github.com/meliusmum-sketch/Faboulaagrobusiness
   - Cliquez sur **Settings** → **Pages**
   - Sous "Build and deployment":
     - Source: `GitHub Actions`
   - Le workflow `.github/workflows/deploy.yml` s'exécutera automatiquement

3. **Accéder au site**
   - URL: `https://meliusmum-sketch.github.io/Faboulaagrobusiness/`
   - Le déploiement prend 2-3 minutes

4. **Configuration du formulaire (requis)**
   - Inscrivez-vous sur [Formspree](https://formspree.io) ou [Web3Forms](https://web3forms.com)
   - Remplacez l'attribut `data-netlify="true"` dans le formulaire
   - Ajoutez l'action du service choisi

### Option 3: Vercel ⚡

**Avantages:**
- ✅ Très rapide
- ✅ Déploiement automatique
- ✅ HTTPS automatique

**Instructions:**

1. **Créer un compte Vercel**
   - Allez sur [vercel.com](https://vercel.com)
   - Inscrivez-vous avec GitHub

2. **Importer le projet**
   - Cliquez sur "Add New" → "Project"
   - Sélectionnez votre repository
   - Cliquez sur "Import"

3. **Configuration**
   - Framework Preset: `Other`
   - Build Command: *(laisser vide)*
   - Output Directory: `.`
   - Cliquez sur "Deploy"

## 🔄 Déploiement Automatique

Une fois configuré, le déploiement est automatique :

1. **Vous faites un changement** dans votre code local
2. **Vous commitez et pushez** sur la branche `main`
3. **Le site se déploie automatiquement** en 1-3 minutes

## 🔍 Vérification du Déploiement

### Netlify
```bash
# Vérifier le statut
curl -I https://votre-site.netlify.app
```

### GitHub Pages
```bash
# Vérifier le déploiement
curl -I https://meliusmum-sketch.github.io/Faboulaagrobusiness/
```

### Actions GitHub
- Allez sur l'onglet "Actions" du repository
- Vérifiez que le workflow "Deploy to GitHub Pages" est en succès ✅

## 📋 Checklist Avant Déploiement

- [ ] Merger la branche de développement dans `main`
- [ ] Remplacer les images placeholder par de vraies photos
- [ ] Tester le site localement
- [ ] Vérifier que tous les liens fonctionnent
- [ ] Configurer Google Analytics (optionnel)
- [ ] Configurer le domaine personnalisé (optionnel)

## 🐛 Dépannage

### Le site ne se charge pas
- Vérifiez que la branche `main` contient les derniers changements
- Vérifiez les logs du déploiement dans Actions/Netlify

### Les images ne s'affichent pas
- Vérifiez que les chemins sont relatifs (pas de `/` au début)
- Vérifiez que les fichiers images existent dans `assets/images/`

### Le formulaire ne fonctionne pas
- Sur Netlify : vérifiez que `data-netlify="true"` est présent
- Sur GitHub Pages : configurez un service tiers (Formspree, Web3Forms)

## 📞 Support

Pour toute question :
1. Consultez la documentation du service de déploiement
2. Vérifiez les logs de déploiement
3. Consultez le README.md principal

---

✅ **Configuration terminée !** Votre site est prêt à être déployé.
