# Site vitrine L'Épi d'Or, Bingerville

Site statique en un seul fichier (`index.html`). Aucune installation requise.

## Ouvrir en local
Double-cliquez sur `index.html`.

## Points à vérifier avant la mise en ligne
1. **Numéro WhatsApp** : dans `index.html`, cherchez `var WA="2250507111013"`.
   Format international sans + ni espaces. Numéro à confirmer avec la boulangerie.
   Le même numéro est aussi dans le bloc JSON-LD (`"telephone"`) en haut du fichier.
2. **Coordonnées GPS** : cherchez `5.3530283` (JSON-LD, lien Google Maps du bouton
   « Ouvrir l'itinéraire »). Remplacez par la position exacte relevée sur place.
3. **Prix et poids** : tableau `P=[...]` dans le script. Chaque ligne :
   `[catégorie, nom, poids, prix FCFA, type de dessin, couleur1, couleur2, photo]`.
   Un prix à `0` affiche « Sur devis ». Les prix actuels sont des exemples.
4. **Domaine** : remplacez `VOTRE-DOMAINE` dans `robots.txt` et `sitemap.xml`,
   puis ajoutez dans le `<head>` : `<link rel="canonical" href="https://VOTRE-DOMAINE/">`
   et une image de partage `og:image` (1200 x 630 px).

## Ajouter de vraies photos
1. Placez les photos (JPG ou WebP, 800 px de large, moins de 150 Ko) dans `photos/`.
2. Dans le tableau `P`, ajoutez le chemin en 8e position, par exemple :
   `["Pains","Baguette","150 g",150,"bag",.75,null,"photos/baguette.jpg"]`
   La photo remplace automatiquement le dessin.

## Mise en ligne
- **Vercel** : glissez le dossier sur vercel.com/new, ou `vercel --prod`.
- **Netlify** : glissez le dossier sur app.netlify.com/drop.
- Domaine : achetez-le chez LWS et pointez-le vers l'hébergeur.

## Après la mise en ligne (référencement local)
- Compléter la fiche Google : téléphone, horaires, photos, lien du site.
- Soumettre le site dans Google Search Console avec le sitemap.
- Ajouter le lien du site dans les bios Facebook et Instagram.
