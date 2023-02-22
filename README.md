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

<body>

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
<header class="d-flex flex-wrap align-items-center justify-content-md-between py-3 mb-4 border-bottom">
        <a href="index.html" class="col-md-auto mb-auto mb-md-aut">
            <img src="images/DAGA.svg" alt="Logo" class="ms-4 w-33 img-fluid">
        </a>
        <ul class="nav col-12 col-md-auto mb-2 justify-content-center mb-md-0 fs-5">
            <li><a href="index.html" class="nav-link px-3 link-dark">A propos</a></li>
            <li><a href="simulateur.html" class="nav-link px-3 link-dark">Simulateur</a></li>
        </ul>
        <ul class="col-md-3 text-end">
            <button class="btn btn-dark me-3 mt-3">Login</button>
        </ul>
    </header>
```

Pour la partie body je commence par ajouter le contenu en HTML :
``` html
<main>
        <h1>A propos</h1>
        <p>Bienvenue chez DAGA, votre partenaire informatique de confiance...</p>
        <ul>
          <button>Mail</button>
          <button>Simulateur</button>
        </ul>
    </main>
```