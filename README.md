# Landing page — Collection Théologie Niveau 3

Landing page statique (HTML/CSS/JS vanilla, sans dépendance ni build) dont le
seul but est de présenter la collection (14 cours, 16 livres, bonus de
+400 livres chrétiens) et de rediriger le visiteur vers la fiche produit
Chariow. Aucune logique de panier, de compte ou de paiement n'est codée ici,
et aucun prix n'est affiché sur la page.

## Aperçu local

Ouvrez `index.html` directement dans un navigateur, ou servez le dossier avec
n'importe quel serveur statique (`npx serve .`, `python3 -m http.server`, etc.).

## Lien Chariow

Déjà configuré dans `script.js`, ligne 4 :
```js
const CHARIOW_URL = "https://livresenligne.mychariow.shop/prd_eq8dt0/checkout";
```
C'est le seul endroit à modifier si le lien change : tous les boutons CTA
(`data-cta` — nav, hero, bonus, CTA intermédiaire, CTA final, barre sticky
mobile) reçoivent automatiquement cette URL au chargement de la page.

## Contact

- **E-mail :** `libraryonline65@gmail.com` (footer, lien `mailto:`)
- **WhatsApp :** bouton visible dans le footer vers
  `https://wa.me/243823226790` avec un message préformaté ; le numéro n'est
  affiché nulle part ailleurs sur la page.
- **Site :** `https://libraryonline.online` (footer)

## Assets

- `cover.jpg` — couverture de la collection, utilisée dans le Hero et comme
  image `og:image` / `twitter:image`.
- `proof/whatsapp-01.jpg` à `whatsapp-04.jpg` — captures WhatsApp de la
  section « Témoignages ». Les liens de livraison, numéros de téléphone et
  photos de profil visibles dans ces captures ont été masqués avant
  publication ; le reste des échanges est authentique.

Une fois l'URL de déploiement connue, pensez à mettre à jour `og:image` /
`twitter:image` dans `index.html` avec une URL absolue
(ex. `https://votre-site.pages.dev/cover.jpg`) pour un meilleur aperçu de
partage sur les réseaux sociaux et messageries.

## Déploiement sur Cloudflare Pages

1. Créez un projet Pages à partir de ce dépôt GitHub.
2. **Root directory** : laissez `/` (racine du dépôt).
3. **Build command** : laissez vide. **Build output directory** : `/`
   (ou laissez vide, valeur par défaut).
4. Déployez. Le fichier `_headers` configure automatiquement les en-têtes
   de sécurité.

## Déploiement sur Vercel

Ce dépôt contient son propre `vercel.json` (en-têtes de sécurité ; aucune
commande de build nécessaire, site 100 % statique).

1. Sur [vercel.com](https://vercel.com), **Add New → Project**, importez ce
   dépôt GitHub.
2. **Framework Preset : Other**. Laissez **Root Directory**, **Build
   Command** et **Output Directory** à leurs valeurs par défaut.
3. Déployez.

## Déploiement sur Netlify

Ce dépôt contient aussi son propre `netlify.toml` (`publish = "."`).
Importez-le comme nouveau site Netlify : aucune configuration
supplémentaire n'est nécessaire.

## Déploiement sur GitHub Pages

Déployable tel quel (aucune étape de build) : activez GitHub Pages sur ce
dépôt (branche `main`, dossier racine `/`).
