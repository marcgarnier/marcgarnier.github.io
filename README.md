# Site personnel — Marc Garnier

Site statique (HTML / CSS / JS, aucune dépendance à installer), publié sur GitHub Pages.

## Structure

- `index.html` — accueil : présentation courte + liste des recherches (lien GitHub ou article pour chacune)
- `thesis.html` — page courte sur la thèse (question, méthode, jalons de la période)
- `cv.html` — expériences, formation, certifications, outils
- `projects.html` — redirige vers `index.html#research` (anciens liens)
- `css/style.css` — tout le style (couleurs et polices dans `:root` en haut du fichier)
- `js/main.js` — année du footer

Pour ajouter une recherche : copier un bloc `<li class="entry">` dans `index.html`.

## PDF du CV

`assets/marc-garnier-cv.pdf` est généré depuis `cv.html` (styles `@media print` dans `css/style.css`).
Après chaque modification du CV, le régénérer (PowerShell, depuis la racine du dépôt) :

```powershell
& "C:\Program Files\Google\Chrome\Application\chrome.exe" --headless=new --no-pdf-header-footer --print-to-pdf="$PWD\assets\marc-garnier-cv.pdf" "file:///$PWD/cv.html"
```
