Projet : Page d’accueil type Google

Ce projet reproduit une interface simplifiée de la page d’accueil de Google en utilisant uniquement HTML et CSS.  
Il s’agit d’un exercice de conception front-end visant à pratiquer la mise en page, la responsivité, et la stylistique d’interface moderne.


Objectif du projet

L’objectif principal est de :
- Structurer une page web claire avec HTML5 ;
- Appliquer un style moderne et responsive avec CSS3 ;
- Reproduire la logique de l’interface de recherche de Google (logo, barre de recherche, boutons, liens) ;
- Pratiquer les propriétés de Flexbox et Media Queries.

A. Structure HTML (index.html)
Une explication technique de chaque partie du fichier HTML :

1. En-tête du document
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css" />
    <title>Document</title>
</head>
        
<!DOCTYPE html> indique au navigateur que le document suit la norme HTML.
<html lang="fr"> précise la langue du contenu pour l’accessibilité.
<meta charset="UTF-8"> définit l’encodage pour supporter les caractères spéciaux (é, è, etc.).
<meta name="viewport"> garantit une adaptation correcte sur les écrans mobiles.
<link rel="stylesheet" href="style.css"> relie le fichier de styles CSS externe.
<title> définit le titre affiché dans l’onglet du navigateur.

2️. Corps du projet
<body>
    <section class="main">
        <section class="A">
            <div class="nav">
                <a class="nav_1">Gmail</a>
                <a class="nav_2">Image</a>
            </div>
        </section>
    </section>
</body>
        
Le corps (<body>) contient trois grandes sections logiques :

Section A : Navigation principale (liens Gmail et Images)
Section B : Logo Google, barre de recherche, boutons
Section C : Pied de page avec la localisation et les liens légaux

3. Logo Google et champ de recherche
<div class="logo">
    <p>
        <span class="l_1">G</span>
        <span class="l_2">o</span>
        <span class="l_3">o</span>
        <span class="l_4">g</span>
        <span class="l_5">l</span>
        <span class="l_6">e</span>
    </p>
</div>
        
Chaque lettre du logo est un <span> coloré différemment en CSS pour imiter le logo officiel.

B. Feuille de style CSS (style.css)
Le fichier CSS gère la mise en forme visuelle. Il utilise principalement Flexbox pour l’alignement et la répartition des éléments.

1️. Réinitialisation et corps
* {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
}
body {
    display: flex;
    flex-direction: column;
    align-items: center;
    min-height: 100vh;
    width: 100%;
}
        
* applique une réinitialisation globale des marges/paddings.
body utilise display:flex et flex-direction:column pour empiler verticalement les sections.
min-height:100vh garantit que le contenu couvre toute la hauteur de l’écran.

2️. Navigation
.A {
    display: flex;
    justify-content: end;
    align-items: end;
}
.nav {
    display: flex;
    gap: 20px;
    color: #70757a;
}
        
.A place le menu en haut à droite avec justify-content:end.
.nav aligne les liens horizontalement et crée un espace de 20px entre eux.

3️. Logo et boutons
.logo { font-size: 120px; font-weight: 800; }
.l_1{color:#4285F4;} .l_2{color:#EA4335;} .l_3{color:#FBBC05;}
.l_4{color:#4285F4;} .l_5{color:#34A853;} .l_6{color:#EA4335;}      
Chaque couleur correspond à une lettre du logo Google.

input {
    width: 900px;
    height: 50px;
    border-radius: 30px;
    border: solid 1px #f1f3f4;
    padding-left: 20px;
    font-size: 25px;
}      
La barre de recherche est un champ de texte large et arrondi, stylisé pour ressembler à celle de Google.

.button_1, .button_2 {
    background-color: #f1f3f4;
    width: 145px;
    height: 30px;
    border-radius: 30px;
    cursor: pointer;
    border: none;
    font-weight: bold;
}       
Ces propriétés créent des boutons ronds avec un effet de survol défini plus bas dans .button :hover.

4️. Responsivité
@media (max-width: 768px) {
    .main { width: 90%; }
    .logo { font-size: 45px; }
    input { width: 280px; }
}
La règle @media adapte la mise en page pour les écrans mobiles en réduisant la taille du logo et de la barre de recherche.



Ce projet démontre la maîtrise des fondations du front-end : structure sémantique HTML, mise en page en Flexbox, et adaptation responsive. Le résultat est une page fidèle à l’interface originale de Google, à la fois simple, esthétique et compatible sur tout appareil.


[Capture_1](./image/Capture_1.png)
[Capture_2](./image/Capture_2.png)
