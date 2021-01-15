# Javascript

- [Javascript](#javascript)
  - [Définitions](#définitions)
    - [Objets, Methodes, Propriétés](#objets-methodes-propriétés)
  - [Debugger](#debugger)
  - [Structures](#structures)
  - [Fonctions/propriétés](#fonctionspropriétés)

## Définitions
### Objets, Methodes, Propriétés
- **Propriétés** = association entre clé => valeur (dans un objet)
- **Objet** = plusieurs clé => valeurs donc plusieurs propriétés. Peut aussi contenir des méthodes.
- **Méthode** = association clé => fonction / c'est une propriété avec comme valeur une fonction.
- **Handler** = une fonction qui s'execute lors de l'execution d'un evenement écouté. Pas spécifique aux objets.

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

- Déclarer une méthode (uniquement à l'intérieur d'un objet)
```js
name: function() {
}  
```

- Récupérer un élément
```js
let name = document.getElementById('id-name');
let name = document.querySelector('#id-ciblé');
let name = document.querySelector('.class-cibléé'); //si plusieurs éléments portent la classe, renvoie le premier élément uniquement.
let name = document.querySelector('body||form||element-ciblé');
let name = document.querySelectorAll('.class-ciblée || élément HTML || ...');
// cibler plusieurs élements  / mais renvoi une collection indéxée
// il en existe d'autres : ElementsbyName, ElementsByTagName
```

- Ajout d'un écouteur d'évenement
```js
document.element.addEventListener('click', handleFunctionName);
// élément_auquel_ajouter_événement.addEventListener('type d'evenement', fonction à appeler)

window.addEventListener('DOMContentLoaded', handleFunctionName);
// l'événement DOMContentLoaded correspond au chargement complet de la page. On l'applique à l'élément window
```

- Déclaration d'un handler
```js
function handleFunctionName(evt) {
    instructions;
}

// si à l'intérieur d'un module, syntaxe de la méthode :
handleFunctionName: function(evt) {
    instructions;
},
```

## Fonctions/propriétés
```js
evt.preventDefault(); // pour stopper une action ou un fonctionnement par défaut / parentheses restent vides. Généralement sur un événement 'submit' pour éviter le refresh de la page



//méthodes relatives à des éléments du DOM

let elementDuDOM = document.querySelector('p#paragraphe');
//elementDuDom contient l'élément p avec l'id paragraphe


.textContent // définir le contenu texte d'un élement
elementDuDOM.textContent = 'Aurevoir' // remplace le contenu du paragraphe ciblé par Aurevoir
elementDuDOM.textContent += ' toi !' // renvoi "Aurevoir toi !"

.className // définir le nom de classe de l'élément ciblé
elementDuDOM.className = 'f0f'; // elementDuDOM a pour classe f0f

.style // change la ou les propriétés css
elementDuDOM.style.color = "red"; // renvoi "Aurevoir toi !" en couleur rouge
document.getElementById('#paragraphe').style.color = "red"; // syntaxe alternative

// Dataset 

elementDuDOM.dataset.name = "Jacky";
elementDuDOM.dataset.age = "15 ans";
console.log(elementDuDOM.dataset); // retourne name = Jacky; age = 15 ans;
//l'élément HTML ciblé dispose maintenant des attributs suivants :
//data-name="Jacky"
//data-name="Jacky"
//Ils sont visibles dans la balise ouvrante, par exemple ici :
// <p id="paragraphe" data-name="Jacky" data-age="15 ans">

//propriété value : spécifique aux éléments HTML de type input (input type text, textarea, select, boutons radio... tous éléments qui contiennent une valeur choisie ou saisie par l'utilisateur)
.value // atrribut ou valeur d'un element de type input
//par ex. l'élément avec l'id #select_language est un input de type select

let inputElement = document.querySelector("#select_language");
console.log(inputElement.value) // renvoi par exemple "fr" si la langue française est sélectionnée


// Les autres fonctions propriétés ---------------

.lentgh // la longeur de la chaine de caractère
let varName = 'Bonjour',
console.log(varName.length) // renvoi 7

.substring(1,4) // selectionne une partie des caractères de la chaine.
varName.substring(1,4); //renvoi onj de Bonjour / selectionne après le 1er et avant le 4ème

.includes("Bonjour"); // vérifie si la variable contient le mot Bonjour et renvoi true or false
```
