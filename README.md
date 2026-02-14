# FALOBOULA AGROBUSINESS SUARL — Site Web

Site vitrine professionnel pour **FALOBOULA AGROBUSINESS SUARL**, entreprise sénégalaise spécialisée dans la transformation, distribution et valorisation de produits agricoles.

## Aperçu

- **Thème** : Noir luxe avec accents dorés et verts
- **Technologie** : HTML5, CSS3, JavaScript vanilla (aucun framework)
- **Hébergement** : Compatible Netlify, GitHub Pages, Vercel
- **Formulaire** : Netlify Forms (zéro backend nécessaire)

## Arborescence du projet

```
faloboula/
├── index.html                 # Page principale
├── confidentialite.html       # Politique de confidentialité
├── netlify.toml               # Configuration Netlify
├── README.md                  # Ce fichier
├── css/
│   └── styles.css             # Feuille de styles principale
├── js/
│   └── main.js                # JavaScript principal
└── assets/
    ├── icons/
    │   ├── favicon.svg        # Favicon SVG
    │   └── apple-touch-icon.png  # Icône Apple (à créer, 180x180px)
    └── images/
        ├── og-cover.jpg       # Image Open Graph (1200x630px)
        ├── galerie-1.webp     # Galerie : transformation céréales
        ├── galerie-2.webp     # Galerie : produits laitiers
        ├── galerie-3.webp     # Galerie : élevage & aviculture
        ├── galerie-4.webp     # Galerie : récolte & production
        ├── galerie-5.webp     # Galerie : logistique
        ├── galerie-6.webp     # Galerie : matériels agricoles
        ├── actu-1.webp        # Actualité 1 (campagne agricole)
        ├── actu-2.webp        # Actualité 2 (partenariat)
        └── actu-3.webp        # Actualité 3 (modernisation)
```

## Déploiement

### Option 1 : Netlify (recommandé)

1. Créez un compte sur [netlify.com](https://netlify.com)
2. Créez un repo GitHub et poussez les fichiers
3. Connectez le repo à Netlify via « New site from Git »
4. Le formulaire de contact fonctionnera automatiquement grâce aux attributs `data-netlify="true"`
5. Personnalisez le domaine dans les paramètres Netlify

### Option 2 : GitHub Pages

1. Créez un repo GitHub (ex: `faloboula-agrobusiness`)
2. Poussez les fichiers
3. Allez dans Settings → Pages → Source: « Deploy from a branch » (main)
4. **Note** : le formulaire Netlify ne fonctionnera pas sur GitHub Pages. Remplacez par [Formspree](https://formspree.io) ou [Web3Forms](https://web3forms.com)

### Option 3 : Glisser-déposer

1. Zippez le dossier `faloboula/`
2. Allez sur [app.netlify.com/drop](https://app.netlify.com/drop)
3. Déposez le fichier ZIP
4. Le site est en ligne instantanément

## Personnalisation

### Images

Remplacez les placeholders SVG dans la galerie et les actualités par vos propres images :

```html
<!-- Remplacez le placeholder par : -->
<img src="assets/images/galerie-1.webp"
     alt="Description de l'image"
     loading="lazy"
     width="600"
     height="400">
```

**Format recommandé** : WebP pour la performance, JPEG en fallback. Dimensions suggérées :
- Galerie : 800×500px
- Actualités : 600×340px
- OG Cover : 1200×630px

### Google Analytics

Dans `index.html`, remplacez `G-XXXXXXXXXX` par votre ID Google Analytics :

```html
<script async src="https://www.googletagmanager.com/gtag/js?id=G-VOTRE-ID"></script>
```

### Google Maps

Pour afficher l'emplacement exact, remplacez les coordonnées dans l'iframe Google Maps de la section contact par vos coordonnées GPS réelles.

### Coordonnées

Mettez à jour les coordonnées dans :
- `index.html` : section contact, footer, lien WhatsApp, structured data JSON-LD
- `confidentialite.html` : section responsable du traitement

### Réseaux sociaux

Mettez à jour les URLs des réseaux sociaux dans le footer et le JSON-LD :
- Facebook : `https://www.facebook.com/faloboulaagrobusiness`
- LinkedIn : `https://www.linkedin.com/company/faloboula-agrobusiness`
- WhatsApp : `https://wa.me/221781373952`

## Fonctionnalités

| Fonctionnalité | Status |
|---|---|
| SEO (meta, OG, JSON-LD, sitemap-ready) | ✅ |
| Accessibilité (ARIA, skip-link, labels) | ✅ |
| Formulaire Netlify Forms + validation JS | ✅ |
| Bouton WhatsApp flottant | ✅ |
| Bouton retour en haut | ✅ |
| Galerie de réalisations | ✅ |
| Témoignages clients | ✅ |
| Section actualités / blog | ✅ |
| Timeline historique | ✅ |
| Fiche fondateur | ✅ |
| Carte Google Maps | ✅ |
| Icônes réseaux sociaux (FB, LI, WA) | ✅ |
| Page confidentialité | ✅ |
| Responsive mobile/tablette | ✅ |
| Animations au scroll | ✅ |
| Compteurs animés | ✅ |
| Headers de sécurité (Netlify) | ✅ |
| Configuration déploiement | ✅ |
| Google Analytics (snippet) | ✅ |

## Performance

Le site est conçu pour un score Lighthouse élevé :
- **Aucune dépendance externe** hormis Google Fonts
- **CSS et JS séparés** pour mise en cache optimale
- **Images lazy-loaded** (`loading="lazy"`)
- **Fonts préconnectées** (`preconnect`)
- **Pas de framework lourd** : HTML/CSS/JS vanilla

## Informations légales

- **Dénomination** : FALOBOULA AGROBUSINESS SUARL
- **NINEA** : 007698153
- **RCCM** : SN DKR 2019 B 18441
- **Capital** : 1 000 000 F CFA
- **Siège** : Pikine Route des Niayes, Lot N°30, Dakar, Sénégal
- **Gérant** : Abdoulaye BA
- **Date de création** : 17/07/2019

---

© 2025 FALOBOULA AGROBUSINESS SUARL — Tous droits réservés
