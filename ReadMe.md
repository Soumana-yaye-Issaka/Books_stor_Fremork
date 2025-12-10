# 📚 Book Store - Deuxième Projet

Bienvenue sur **Book Store** (BOOTIN), un site e-commerce moderne de vente de livres construit avec **Bootstrap 5.3.8**. C'est mon **deuxième projet** et il démontre l'utilisation complète du framework Bootstrap pour créer une interface responsive et professionnelle.

## 🎯 À propos du Projet

Ce projet est une application web multipage dédiée à la vente de livres en ligne. Il présente:
- Une page d'accueil avec produits en vedette
- Un catalogue de produits (Shop)
- Une section de blog (Post)
- Une page de contact
- Un pied de page complet

**Stack Technologique:**
- HTML5
- CSS3
- Bootstrap 5.3.8
- Bootstrap Icons 1.13.1

---

## 📱 Comprendre Bootstrap et la Conception Responsive

### Qu'est-ce que Bootstrap ?

Bootstrap est un framework CSS et JavaScript qui facilite la création de sites web **responsives** (adaptatifs). Il fournit des composants prêts à l'emploi, un système de grille 12 colonnes, et des utilitaires pour créer des mises en page flexibles.

### Les Breakpoints de Bootstrap 5

Les **breakpoints** sont les points de rupture responsive. Ils définissent à quelles largeurs d'écran le design doit changer. Bootstrap utilise des **suffixes de classe** pour appliquer les styles à partir d'une certaine taille d'écran.

#### Tableau des Breakpoints:

| Breakpoint | Suffixe | Largeur de l'écran |
|-----------|---------|-------------------|
| **Extra Small** | (aucun) | < 576px (Mobile) |
| **Small** | `-sm` | ≥ 576px (Petit téléphone) |
| **Medium** | `-md` | ≥ 768px (Tablette) |
| **Large** | `-lg` | ≥ 992px (Desktop) |
| **Extra Large** | `-xl` | ≥ 1200px (Grand écran) |
| **XXL** | `-xxl` | ≥ 1400px (Très grand écran) |

#### Exemples dans le Projet:

```html
<!-- Navbar: affichage du menu différent selon la taille -->
<nav class="navbar navbar-expand-md">
  <!-- Le menu se replie (collapse) jusqu'à md (≥ 768px) -->
</nav>

<!-- Colonne: prend 12 colonnes sur mobile, 6 sur tablette, 3 sur desktop -->
<div class="col-12 col-md-6 col-lg-3"></div>


🎨 Système de Grille Bootstrap
Bootstrap utilise une grille de 12 colonnes pour organiser le contenu. Chaque ligne (.row) se divise en 12 parts égales.

Principes de Base:
Container (.container ou .container-fluid)

Enveloppe le contenu
Offre un padding et une largeur max
Row (.row)

Crée une nouvelle ligne
Contient des colonnes
Columns (.col-*)

Divisent l'espace horizontal
Le -* indique le nombre de colonnes occupées
Exemple Simple:

<!-- 3 colonnes égales sur desktop, 1 colonne sur mobile -->
<div class="container">
  <div class="row">
    <div class="col-12 col-md-4">Colonne 1 (4/12 sur md)</div>
    <div class="col-12 col-md-4">Colonne 2 (4/12 sur md)</div>
    <div class="col-12 col-md-4">Colonne 3 (4/12 sur md)</div>
  </div>
</div>

Exemple 1: Disposition Contact (Contact.html) :

<div class="container mt-5 gap-5">
  <div class="row gx-4 gy-4">
    <!-- Information (3/12 sur lg, 12/12 sur mobile) -->
    <div class="col-12 col-lg-3 order-1 order-lg-1">
      <!-- Contenu: adresse, téléphone, email -->
    </div>
    
    <!-- Carte (9/12 sur lg, 12/12 sur mobile) -->
    <div class="col-12 col-lg-9 order-2 order-lg-2">
      <!-- Google Maps -->
    </div>
  </div>
</div>

Explications:

col-12: Prend toute la largeur sur mobile (12/12 colonnes)
col-lg-3: Prend 1/4 de l'écran sur desktop (3/12 colonnes)
col-lg-9: Prend 3/4 de l'écran sur desktop (9/12 colonnes)
order-1 / order-lg-1: Définit l'ordre d'affichage (mobile: 1, lg: 1)
gx-4: Espacement horizontal entre colonnes
gy-4: Espacement vertical entre lignes
Exemple 2: Produits (Shop.html)
<div class="row g-4">
  <!-- Cartes de produits: 2 par ligne sur mobile, 4 sur desktop -->
  <div class="col-12 col-sm-6 col-lg-3">
    <!-- Produit -->
  </div>
  <!-- Répété 12 fois pour 12 produits -->
</div>

Disposition:

Mobile (< 576px): 1 colonne (12/12)
Small (≥ 576px): 2 colonnes (6/12 chacune)
Large (≥ 992px): 4 colonnes (3/12 chacune)

🎀 Flexbox avec Bootstrap (d-flex)
Qu'est-ce que Flexbox ?
Flexbox est un modèle de mise en page CSS qui permet d'aligner et de distribuer les éléments facilement dans un conteneur.

Les Utilitaires Flexbox de Bootstrap
1. d-flex - Active Flexbox
<!-- Conteneur flexbox -->
<div class="d-flex">
  <div>Élément 1</div>
  <div>Élément 2</div>
  <div>Élément 3</div>
</div>

Breakpoints supportés:

.flex-row: Horizontal
.flex-column: Vertical
.flex-md-row: Horizontal à partir de md (768px)
.flex-lg-row: Horizontal à partir de lg (992px)
Exemples dans le Projet:
<!-- Navbar icons: verticaux sur mobile, horizontaux sur desktop -->
<div class="d-none d-md-flex fs-4 gap-4">
  <article><i class="bi bi-suit-heart"></i></article>
  <article><i class="bi bi-bookmark"></i></article>
</div>

<!-- Form: inputs en colonne, responsive -->
<form class="d-flex flex-column gap-3">
  <input type="text" placeholder="Name">
  <input type="email" placeholder="Email">
</form>

Options disponibles:

justify-content-start: Début (défaut)
justify-content-end: Fin
justify-content-center: Centre
justify-content-between: Espacement maximal
justify-content-around: Espacement égal autour
justify-content-evenly: Espacement égal entre
Exemples dans le Projet:
<!-- Navbar: contenus espacés au début et à la fin -->
<nav class="navbar d-flex justify-content-between p-3">
  <div>BOOTIN</div>
  <!-- ... menu ... -->
  <div>Icons</div>
</nav>

<!-- Section: contenu centré horizontalement -->
<section class="d-flex justify-content-center">
  <h2>Contact</h2>
</section>

<!-- Footer: colonnes espacées horizontalement -->
<div class="row g-4">
  <div class="col-12 col-md-6"><!-- Contenu --></div>
  <div class="col-12 col-md-6"><!-- Contenu --></div>
</div>
Options disponibles:

align-items-start: Haut
align-items-center: Centre
align-items-end: Bas
align-items-stretch: Étiré (défaut)
align-items-baseline: Ligne de base

 #####---------########
 Breakpoints supportés pour flexbox:

d-flex: Toujours flexbox
d-sm-flex: À partir de sm (576px)
d-md-flex: À partir de md (768px)
d-lg-flex: À partir de lg (992px)
d-xl-flex: À partir de xl (1200px)
Exemples dans le Projet:
<!-- Header: contenu centré sur mobile, espacé sur desktop -->
<div class="d-flex flex-column d-md-flex flex-md-row justify-content-md-between">
  <div>Recherche</div>
  <div>Logo</div>
  <div>Icons</div>
</div>

<!-- Blog: disposition colonne sur mobile, ligne sur desktop -->
<section class="d-flex flex-lg-row flex-column gap-3">
  <div>Articles</div>
  <div>Sidebar</div>
</section>

########_______#########
Breakpoints supportés:

d-none: Masqué
d-sm-none: Masqué à partir de sm
d-md-none: Masqué à partir de md
d-lg-none: Masqué à partir de lg
d-xl-none: Masqué à partir de xl
Exemples dans le Projet:
<!-- Navbar: bouton hamburger visible seulement sur mobile -->
<button class="navbar-toggler d-md-none">
  <!-- Menu burger -->
</button>

<!-- Navbar: menu complet masqué sur mobile, visible sur md+ -->
<div class="collapse navbar-collapse justify-content-center" id="navbarNav">
  <!-- Menu -->
</div>

<!-- Icons du panier: masqués sur mobile, visibles sur md+ -->
<div class="d-none d-md-flex fs-4 gap-4">
  <article>
    <i class="bi bi-suit-heart"></i>
    <div class="Notification">3</div>
  </article>
  <article>
    <i class="bi bi-bookmark"></i>
    <div class="Notification">0</div>
  </article>
  <article>
    <i class="bi bi-person-fill"></i>
  </article>
</div>

<!-- Section spéciale: masquée sur mobile et tablette, visible sur lg+ -->
<section class="d-none d-lg-block">
  <h3>Contenu Desktop Only</h3>
</section>

<!-- Texte centré: masqué sur mobile, visible sur md+ -->
<div class="d-none d-md-block">
  <h2 class="flip-vertical">Contact Us</h2>
</div>

📊 Vue d'ensemble du Système de Grille + Flexbox
Scénario: Disposition 3 colonnes sur Desktop, 2 sur Tablette, 1 sur Mobile
<div class="container">
  <div class="row g-4"> <!-- Espacement vertical et horizontal -->
    
    <!-- Carte 1: 12/12 (100%) sur mobile, 6/12 (50%) sur sm, 4/12 sur md, 3/12 sur lg -->
    <div class="col-12 col-sm-6 col-md-4 col-lg-3">
      <div class="d-flex flex-column align-items-center">
        <!-- Contenu -->
      </div>
    </div>
    
    <!-- Répété pour les autres cartes -->
  </div>
</div>
Comportement Responsive:

Mobile (< 576px): 1 colonne (prend toute la largeur)
Small (≥ 576px): 2 colonnes
Medium (≥ 768px): 3 colonnes
Large (≥ 992px): 4 colonnes

######---------########

🎓 Concepts Clés à Retenir
Concept	Utilité	Exemple
Breakpoints	Adapter le design à différentes tailles	col-12 col-md-6 col-lg-3
Grille 12 colonnes	Organiser le contenu	col-4 = 4/12 = 1/3
d-flex	Activer le flexbox	d-flex justify-content-center
justify-content	Aligner horizontalement	justify-content-between
align-items	Aligner verticalement	align-items-center
gap	Espacement entre éléments	gap-4
d-none / d-block	Masquer/afficher	d-none d-md-block
flex-column / flex-row	Orientation	flex-column flex-md-row

📱 Breakpoints Bootstrap ( utilisés dans BOOTIN )

| Breakpoint | Classe | Taille   |
| ---------- | ------ | -------- |
| **XS**     | (none) | < 576px  |
| **SM**     | `sm`   | ≥ 576px  |
| **MD**     | `md`   | ≥ 768px  |
| **LG**     | `lg`   | ≥ 992px  |
| **XL**     | `xl`   | ≥ 1200px |
| **XXL**    | `xxl`  | ≥ 1400px |

Demo![Lien du Git-Page:]( https://soumana-yaye-issaka.github.io/Books_stor_Fremork/)



