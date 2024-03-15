# 04 Challenge: projet

## 1. Présentation

L'application permet de sauvegarder des messages que l'on peut 
customiser, incluant la taille des caractères ou la couleur.
Ces messages sont ensuite affichés, et peuvent être supprimés si
nécessaire.


## 2. Contenu

Cette application web est réalisée sur une page simple et utilise
de l'HTML/CSS pour la mise en page, ainsi que React pour toute la 
structure qui s'occupe de l'interaction avec l'utilisateur. 

### 2.1. Initialisation

Ici, nous allons voir tous nos composants qui vont définir les paramètres
de l'application. Voici la partie représentant ceci.

```js
//tailles proposées par l'application
const tailles = []
for (let i = 15; i < 21; i++) {
    tailles.push(`${i}px`)
}

//couleurs proposées par l'appli
const colors = ['palevioletred', 'tomato']

//incrémenteur pour générer l'id du texte
let textId=0

//état initial
const initialState = {
    taille: tailles[0],
    style: colors[0],
    text: '',
    texts: [],
    error: ''
}
```

Nous en avons actuellement 4: 
-Un tableau contenant les tailles, elles sont générées à partir d'une boucle afin
de ne pas avoir à les écrire manuellement,
-Un tableau contenant des couleurs pré-définies, écrites manuellement dû à leur nom spécifique
-Un incrémenteur qui servira pour la fonction de suppression d'un message
-Un état initial au démarrage de l'application