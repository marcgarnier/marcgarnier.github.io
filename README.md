# Site personnel — Marc Garnier

Site statique (HTML / CSS / JS, aucune dépendance à installer), publié sur GitHub Pages.

## Structure

- `index.html` — accueil : présentation courte + liste des recherches (lien GitHub ou article pour chacune)
- `thesis.html` — projet de thèse détaillé (sommaire, sections numérotées, références)
- `cv.html` — expériences, formation, certifications, outils
- `projects.html` — redirige vers `index.html#research` (anciens liens)
- `404.html` — page « Page not found », affichée par GitHub Pages pour toute adresse inexistante (chemins depuis la racine)
- `robots.txt` — autorise l'indexation et indique l'adresse du sitemap
- `sitemap.xml` — liste des pages à indexer (accueil, thèse, CV) avec leur date de mise à jour
- `css/style.css` — tout le style (couleurs et polices dans `:root` en haut du fichier)
- `js/main.js` — année du footer

Pour ajouter une recherche : copier un bloc `<li class="entry">` dans `index.html`.

## PDF du CV

`assets/marc-garnier-cv.pdf` (bouton « Download PDF » de `cv.html`) est le CV LaTeX,
copie de `Bureau\ID\CV_Marc_Garnier.pdf`. Il n'est pas généré depuis `cv.html` :
après une mise à jour du CV LaTeX, recopier le PDF ici sous le même nom.

## Après une modification

1. Mettre à jour la date `<lastmod>` de la page modifiée dans `sitemap.xml`.
2. Après une modification de `css/style.css`, incrémenter `?v=` dans **toutes** les pages,
   y compris `404.html`.
3. Garder le même texte dans la `meta description` et dans `og:description` de chaque page.
