# Ce que j'ai appris en TP Web (TP1 à TP5bis)

Polytech Lyon, 3A, 2026-2027. Récapitulatif de ce que je suis censé maîtriser en partant de zéro.

## TP1 : HTML

- Créer une page web structurée (balises `<html>`, `<head>`, `<body>`) en HTML5
- Écrire des titres (`<h1>` à `<h6>`), des paragraphes et du texte mis en forme (gras, italique…)
- Faire des liens, y compris des liens internes dans une même page (sommaire cliquable)
- Faire des listes à puces et numérotées
- Utiliser les entités HTML (caractères spéciaux)
- Construire un tableau (`<table>`, lignes, cellules, en-têtes)
- Insérer une image et organiser ses fichiers (dossiers `web` et `images`)
- Comprendre la mise en page avec Flexbox (lire un layout existant)
- Valider ses pages avec le validateur officiel du W3C

## TP2 : CSS

- Séparer le contenu (HTML) de la présentation (CSS) dans un fichier `style.css` lié à la page
- Sélectionner des éléments par balise, par `id` (`#info`) et par classe (`.code`)
- Changer couleurs, polices, tailles, marges (`margin`), marges intérieures (`padding`) et bordures
- Utiliser `box-sizing: border-box`
- Centrer un bloc avec `margin: auto` et fixer une largeur
- Arrondir des coins et styler du texte (centré, petites majuscules, majuscule à chaque mot)
- Styler les liens et leur survol (`:hover`)
- Styler un tableau, dont les lignes paires et la dernière ligne
- Organiser une page en `<header>`, `<section>`, `<article>` et `<footer>`
- Afficher une page dans une autre avec `<iframe>`
- Mettre un commentaire d'en-tête dans un fichier

## TP3 : JavaScript

- Tester du code dans la console de Firefox
- Déclarer des variables et connaître les types (`typeof`, `instanceof`) : texte, nombre, booléen, objet, tableau, date, fonction, `null`, `undefined`
- Utiliser le débogueur : point d'arrêt, exécution pas à pas, observation des variables
- Écrire des fonctions (Fibonacci, `Range`) avec une boucle `for`, des valeurs par défaut et des tableaux
- Lancer une fonction au clic avec `onclick`
- Modifier la page depuis JavaScript (DOM) : contenu, attributs (`src` d'une image), styles
- Séparer le code dans un fichier `.js` externe
- Réagir à des événements (`onclick`, `onmouseover`, `onmouseout`)

## TP4 : stockage dans le navigateur

### Cookies

- Ce que c'est : un petit fichier stocké dans le navigateur, envoyé au serveur à chaque requête
- Les créer, lire, modifier et supprimer avec `document.cookie`
- Les options : `path`, `domain`, `expires`, `max-age`, `secure`, `samesite`, `httpOnly`
- Ils ne sont pas dangereux en soi, mais il faut les sécuriser

### localStorage et sessionStorage

- Ils stockent des paires clé/valeur, uniquement du texte
- Les méthodes `setItem`, `getItem`, `removeItem`, `clear`, `key` et `length`
- Différence entre les deux : `localStorage` reste après la fermeture du navigateur, `sessionStorage` non
- Pourquoi les préférer aux cookies : les données ne sont pas envoyées au serveur

### IndexedDB

- Une base de données dans le navigateur pour de gros volumes de données structurées
- Elle est asynchrone et utilise des transactions
- Les opérations de base : `add`, `put`, `get`, `delete`

### Sécurité

- La politique de même origine (une origine = protocole + hôte + port)

## TP5 : Alpine.js

- Ce qu'est Alpine.js : un petit framework qui ajoute de l'interactivité via des attributs HTML, sans étape de build
- L'installer avec une balise `<script>` (CDN)
- Les directives principales :
  - `x-data` : déclarer les données
  - `x-show` : afficher ou cacher
  - `x-bind` ou `:` : lier un attribut (par exemple `:class`)
  - `x-on` ou `@` : réagir à un événement (`@click`, `@keydown.escape`, `.prevent`, `.away`)
  - `x-text` : afficher du texte
  - `x-model` : lier un champ de formulaire à une donnée
  - `x-for` : répéter un élément pour chaque élément d'une liste
  - `x-if` : ajouter ou retirer un élément du DOM
  - `x-init` : lancer du code au démarrage
  - `x-ref`, `x-transition`, `x-cloak`
- Les propriétés magiques : `$refs`, `$event`, `$nextTick`, `$watch`…
- Construire des composants : modale, sidebar, onglets, menu déroulant, formulaire avec validation (regex)

## TP5bis : Todo List

- Ajouter un thème clair/sombre avec `:class` et une donnée booléenne
- Penser l'accessibilité : lecture facilitée (espacement, taille, largeur des lignes)
- Combiner plusieurs classes dynamiques
- Garder les préférences après actualisation avec `localStorage` (et convertir texte ↔ booléen)
- Écrire `setCookie`, `getCookie` et `deleteCookie`
- Sauvegarder des tâches : `JSON.stringify()` pour enregistrer, `JSON.parse()` pour relire
- Distinguer les données métier (les tâches) des préférences utilisateur (thème, lecture)
- Assembler une appli complète : ajout, suppression, validation, statistiques et persistance
