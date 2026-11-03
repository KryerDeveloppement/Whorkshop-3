# BeThom – Portfolio de Thomas, graphiste freelance

Site vitrine responsive pour **Thomas**, graphiste freelance (identité visuelle, UI, illustration). Il présente son profil, ses articles, ses projets et propose un formulaire de contact.

Projet réalisé dans le cadre du challenge d'intégration web de la formation **LearningCampus**, pour l'équipe dev **AgencEco**.

- **Site en ligne :** [kryerdeveloppement.github.io/Whorkshop-3](https://kryerdeveloppement.github.io/Whorkshop-3/)
- **Dépôt GitHub :** [KryerDeveloppement/Whorkshop-3](https://github.com/KryerDeveloppement/Whorkshop-3)
- **Maquette Figma :** [LearningCampus-maquette-portfolio](https://www.figma.com/design/687syGebv93JgNJYw0FbPQ/LearningCampus-maquette-portfolio)

## Table des matières

1. [Contexte](#contexte)
2. [Aperçu](#aperçu)
3. [Fonctionnalités](#fonctionnalités)
4. [Technologies et police utilisée](#technologies-et-police-utilisée)
5. [Structure du projet](#structure-du-projet)
6. [Installation](#installation)
7. [Responsive design](#responsive-design)
8. [Accessibilité et performance](#accessibilité-et-performance)
9. [Validation W3C](#validation-w3c)
10. [Déploiement](#déploiement)
11. [Auteur](#auteur)

## Contexte

Thomas, ancien camarade de classe spécialisé en graphisme, lance son activité en freelance. Il souhaite un site vitrine simple et efficace. Il a fourni une maquette Figma (versions ordinateur et mobile) et confie l'intégration HTML/CSS responsive. La version tablette est laissée libre.

**Objectifs :**
- Respecter fidèlement la maquette (structure, marges, typographies, couleurs)
- Proposer un site responsive, rapide et accessible
- Livrer un code valide W3C, lisible et bien organisé
- Mettre le site en ligne sur un serveur mutualisé

## Aperçu

<!-- Ajoutez vos captures d'écran dans le dossier docs/ -->
| Desktop | Tablette | Mobile |
|---|---|---|
| ![Desktop](docs/apercu-desktop.png) | ![Tablette](docs/apercu-tablette.png) | ![Mobile](docs/apercu-mobile.png) |

## Fonctionnalités

- **Menu de navigation fixe** au défilement, avec liens d'ancre vers les sections : Accueil, Blog (`#blog`), Portfolio (`#projet`) et Contact (`#contact`)
- **Section d'accueil** : présentation de Thomas, photo et bouton **Télécharger mon CV** (fichier PDF)
- **Articles récents** : deux articles de blog avec date et catégories
- **Travaux en vedette** : trois projets (dashboard, illustration, typographie) avec image, date, type et description
- **Formulaire de contact** : nom, email, service souhaité, budget et message
- **Pied de page** : liens vers les réseaux sociaux (Facebook, Instagram, Twitter, LinkedIn)
- Mise en page responsive : desktop, tablette et mobile (menu adapté sur mobile)

## Technologies et police utilisée

| Domaine | Choix |
|---|---|
| Structure | HTML5 sémantique (`header`, `nav`, `main`, `section`, `article`, `footer`) |
| Style | CSS3 (Flexbox et Grid), sans framework |
| Interactivité | JavaScript léger, uniquement si utile |
| Versionnage | Git et GitHub |
| Maquettes | Figma |

**Police principale : [Heebo](https://fonts.google.com/specimen/Heebo)**, chargée via Google Fonts.
**Police de secours : [Poppins](https://fonts.google.com/specimen/Poppins)**, puis `sans-serif`.

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Heebo:wght@100..900&family=Poppins:wght@100..900&display=swap" rel="stylesheet">
```

```css
font-family: "Heebo", "Poppins", sans-serif;
```

## Structure du projet

```
Whorkshop-3/
├── index.html
├── styles.css
├── assets/
│   ├── BeThom.png                 # logo
│   ├── menu.png                   # icône du menu mobile
│   ├── photo_thomas.webp          # photo de Thomas
│   ├── Ellipse.png                # ombre de la photo
│   ├── projet1.png
│   ├── projet2.png
│   ├── projet3.png
│   ├── facebook.png
│   ├── instagram.png
│   ├── twitter.png
│   ├── linkedin.png
│   └── CV_Thomas_Graphiste.pdf    # CV téléchargeable
├── docs/                          # captures d'écran pour ce README
└── README.md
```

## Installation

### Prérequis

- Un navigateur récent (Chrome, Firefox, Edge, Safari)
- [Git](https://git-scm.com/)
- Une connexion Internet (pour charger la police Google Fonts)

### Étapes

```bash
# 1. Cloner le dépôt
git clone https://github.com/KryerDeveloppement/Whorkshop-3.git

# 2. Se placer dans le dossier
cd Whorkshop-3

# 3. Ouvrir le site
# Ouvrir index.html dans le navigateur
# ou lancer un serveur local (ex. extension Live Server de VS Code)
```

Aucune dépendance à installer : le projet est en HTML et CSS natifs.

## Responsive design

Approche **desktop first** : la mise en page de base correspond à la maquette ordinateur, puis une media query `@media (max-width: 700px)` adapte le site au mobile.

| Format | Largeur | Particularités |
|---|---|---|
| Desktop | au-dessus de 700 px | Mise en page fidèle à la maquette, conteneurs centrés de 1200 px maximum, menu horizontal |
| Tablette | environ 700 px à 1200 px | Pas de point de rupture dédié : la mise en page fluide (Flexbox, `max-width`, marges latérales) s'adapte à la largeur disponible |
| Mobile | jusqu'à 700 px | Liens du menu masqués et icône de menu affichée, hero inversé et centré, articles et projets en colonne unique, bloc d'infos de contact masqué, formulaire conservé |

Les mises en page des sections (hero, blog, portfolio, contact) reposent sur Flexbox.

## Accessibilité et performance

- `lang="fr"` sur la balise `<html>`
- Hiérarchie de titres : un seul `h1`, puis `h2` (sections), `h3` et `h4`
- Attributs `alt` descriptifs sur les images
- Labels associés aux champs du formulaire (`for` / `id`)
- Balises sémantiques et landmarks pour faciliter la navigation
- Contrastes de texte vérifiés pour la lisibilité
- Photo au format WebP, images optimisées
- Police chargée avec `display=swap`

## Validation W3C

- HTML : [W3C Markup Validator](https://validator.w3.org/)
- CSS : [W3C CSS Validator](https://jigsaw.w3.org/css-validator/)

Résultat : *à compléter après vérification (ex. « 0 erreur HTML, 0 erreur CSS »).*

## Déploiement

Le site est actuellement publié avec **GitHub Pages** à l'adresse : https://kryerdeveloppement.github.io/Whorkshop-3/

Pour le publier sur un **serveur mutualisé** (FTP ou gestionnaire de fichiers) :

1. Transférer les fichiers via FTP (ex. FileZilla) ou le gestionnaire de fichiers de l'hébergeur
2. Déposer `index.html`, `styles.css` et le dossier `assets/` à la racine du dossier public (`www` ou `public_html`)
3. Vérifier l'URL publique, les ancres du menu, le téléchargement du CV et l'affichage mobile

## Auteur

**Prénom Nom**
- GitHub : [@KryerDeveloppement](https://github.com/KryerDeveloppement)
- Formation : LearningCampus, promotion *[année]*
