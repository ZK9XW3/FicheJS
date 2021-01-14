# Javascript

- [Javascript](#javascript)
  - [Définitions](#définitions)
    - [Objets, Methodes, Propriétés](#objets-methodes-propriétés)
  - [Debugger](#debugger)
  - [Structures](#structures)
  - [Fonctions/propriétés](#fonctionspropriétés)
  - [Dataset](#dataset)

## Définitions
### Objets, Methodes, Propriétés
- **Propriétés** = association entre clé => valeur.
- **Objet** = plusieurs clé => valeurs donc plusieurs propriétés.
- **Méthode** = association clé => fonction / c'est une propriété avec comme valeur une fonction.
- **Handler** = une fonction qui s'execute lors de l'execution d'un evenement écouté.

## Debugger
```javascript
debugger; // a placer au bon endroit dans le code
```


## Structures
- Déclarer un module
```js
const exo1 = {
// insérer des objets 
// clé: valeur,
};
```

- Déclarer une méthode
```js
name: function() {
}  
```

- Récupérer un élément
```js
let name = document.getElementById('id-name');
let name = document.querySelector('#id-ciblé');
let name = document.querySelector('.class-cibléé');
let name = document.querySelector('body||form||element-ciblé');
let name = document.querySelectorAll('#id-ciblé');
// cibler plusieurs élements  / mais renvoi une collection indéxée
// il en existe d'autres : ElementsbyName, ElementsByTagName
```

- Ajout d'un écouteur d'évenement
```js
document.addEventListener('click', handleFunctionName);
// lieu d'ajout de l'event.addEventListener('type d'evenement', fonction à appeler)

name.addEventListener('DOMContentLoaded', handleFunctionName);
// ajout d'un écouteur sur un element "name" / evenement : quand le contenu de la page est chargé
```

- Déclaration d'un handler
```js
function handleFunctionName(evt) {
    instructions;
}

// OU
handleFunctionName: function(evt) {
    instructions;
}
```

## Fonctions/propriétés
```js
evt.preventDefault(); // pour stopper une action ou un fonctionnement par défaut / parentheses restent vides

.lentgh // la longeur de la chaine de caractère
let varName = 'Bonjour',
console.log(varName.length) // renvoi 7

.value // atrribut ou valeur d'un element 
console.log(varName.value) // renvoi "Bonjour"

.textContent // définir le contenu texte d'un élement
varName.textContent = 'Aurevoir' // remplace bonjour par au revoir
varName.textContent += ' toi !' // renvoi "Bonjour toi !"

.varName // définir le nom de classe de l'élément ciblé
varName.className = 'f0f'; // varName a pour classe f0f

.style // change la ou les propriétés css
varName.style.color = "red"; // renvoi "Bonjour" en couleur rouge
document.getElementById('variable').style.color = "red"; // syntaxe alt

// Les autres fonctions propriétés ---------------
.substring(1,4) // selectionne une partie des caractères de la chaine.
varName.substring(1,4); //renvoi onj de Bonjour / selectionne après le 1er et avant le 4ème

.includes("Bonjour"); // vérifie si la variable contient le mot Bonjour et renvoi true or false
```

## Dataset 
```javascript
varName.dataset.name = "Jacky";
varName.dataset.age = "15 ans";
console.log(varName.dataset); // retourne name = Jacky; age = 15 ans;
```



