La base du code HTML doit contenir ceci :

``` html

<!DOCTYPE html>

<html lang="fr">

<head>

    <meta charset="UTF-8">

    <meta http-equiv="X-UA-Compatible" content="IE=edge">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Website</title>

    <link rel="stylesheet" href="css/bootstrap.min.css">

</head>

<body class="background-image">

    <script src="js/bootstrap.js"></script>

</body>

</html>

```

Les lignes :

```html

<link rel="stylesheet" href="css/bootstrap.css">

<script src="js/bootstrap.js"></script>

```

servent à ajouter le frameworks bootstrap au site.

Bootstrap est un framework développé par l'équipe du réseau social Twitter. Proposé en open source, ce framework utilisant les langages HTML, CSS et JavaScript fournit aux développeurs des outils pour créer un site facilement.

Le site vas être divisé en 3 parties, `<header>` `<main>` `<footer>`. Ces balise permette de mieux distinguer les différente partie par le navigateur, elles remplacent la balise `<div>` pour un meilleur rendue.

Je vais configurer la partie `<header>` :
``` html
<header>
        <a href="index.html" >
            <img src="images/logo.jpg" alt="Logo">
        </a>
        <ul>
            <li><a href="apropos.html">A propos</a></li>
            <li><a href="simulateur.html">Simulateur</a></li>
        </ul>
        <ul>
            <button>Login</button>
        </ul>
</header>
```

Foctionnalité des différentes balise :
	- `<a>` : permet de crée un lien hypertext 
	- `<img>` : permet d'insérer une image au seins du site
	- `<ul>` : permet de créer un liste dite "désordonné"
	- `<li>` : permet de présenté un éléments dans une liste, elle est enfant de `<ul>`, `<ol>` ou `<menu>`
	- `<button>` : permet de créer un bouton cliquable

Je vais ensuite embélire le visuel avec du CSS et surtout des preset CSS de bootstrap:
``` html
<header class="d-flex flex-column flex-md-row flex-wrap align-items-center justify-content-md-between py-3 mb-4 border-bottom bg-white">
        <section class="d-flex flex-wrap justify-content-center">
            <a href="index.html" class="">
                <img src="images/DAGA.svg" alt="Logo" class="logo ms-4 img-fluid">
            </a>
        </section>
        <ul class="nav justify-content-center fs-5 d-flex">
            <li><a href="index.html" class="nav-link px-3 link-dark">A propos</a></li>
            <li><a href="simulateur.html" class="nav-link px-3 link-dark">Simulateur</a></li>
        </ul>
        <ul class="text-end d-flex justify-content-center mx-3">
            <a href="login.html">
            <button class="btn btn-dark me-3 mt-3">Contacter</button>
            </a>
        </ul> 
</header>
```

Pour la partie body je commence par ajouter le contenu en HTML :
``` html
<main>
        <h1>A propos</h1>
        <p>Bienvenue chez DAGA, votre partenaire informatique de confiance...</p>
        <ul>
          <button href="mailto:test@daga.fr">Contacter</button>
          <button href="simulateur.html">Simulateur</button>
        </ul>
</main>
```

`<h1>` : permet d'insérer un Titre qui sera surout utile pour le référencement.

Après avoir ajouter du CSS ça done ceci :
``` html
 <main class="bg-white mx-xxl-20 mx-xl-15 mx-lg-10 mx-md-5 mx-3 flex-column d-flex flex-wrap border-radius">
        <h1 class="h1 text-center py-4">A propos</h1>
        <p class="lead text-center mx-xxl-10 mx-xl-7.5 mx-5 px-3">Bienvenue chez DAGA, votre partenaire informatique de confiance...</p>
        <ul class="text-center justify-content-center px-0">
          <button href="mailto:test@daga.fr" class="btn btn-lg btn-secondary my-4 me-2">Contacter</button>
          <button href="simulateur.html" class="btn btn-lg btn-secondary my-4 ms-2">Simulateur</button>
        </ul>
</main>
```

C'est la même chose pour le `<footer>` :

``` html
<footer>
        <article>
            <p>© 2023 Copyright: DAGA.fr</p>
        </article>
    </footer>
```

L'ajout de CSS :

``` html
<footer class="d-flex flex-wrap justify-content-center align-items-center py-3 mt-4 border-top bg-dark">
        <article class="my-3">
            <p class="text-secondary my-auto">© 2023 Copyright: DAGA.fr</p>
        </article>
    </footer>
```

Le rendu est très agréable mais il y une problème d'affichage sur le bas de l'écran :

![Alt text](/images/probleme_affichage.png)

Afin de corriger les problèmes d'affichage je vais modifier le `<body>` :
``` html
<body class="background-image d-flex flex-column min-vh-100 justify-content-between">
```

je vais traduire les class en css :

	- `d-flex` ou `display: flex;` : permet de contenir la partie `<body>` dans une box qui pourra être manipulé.
	- `flex-column` ou `flex-direction: column;` : permet de positionner les différentes balises enfants en colonne.
	- `min-vh-100` ou `min-height: 100vh;` : permet d'indiquer au site que la balise body doit prendre l'intégralité de l'écran pour afficher son contenu.
	- `justify-content-between` ou `justify-content: space-between` : permet d'écarter les éléments enfants si l'éspace disponible à l'écran est trop élevé.

