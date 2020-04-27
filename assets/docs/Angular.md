# Angular Quest 1


## General information

To see this file with VSCODE preview `Shift + cmd + v` or ⇧⌘V.

## Prérequis

Typescript and NodeJS

### Objectifs:

- Installer tous les outils nécéssaires pour Angular,

- Créer son premier projet Angular,

- Comprendre la structure d'un projet

### Angular Install:

`npm install -g @angular/cli` with ShCmd* (*Shell command).

### 1 Creating angular project:

Create a folder for your project with ShCmd
`mkdir Angular_Projects`

Go inside your folder project with ShCmd
`cd Angular-Projects/`

Generate a new Angular Project
`ng new myFirstApp`

Go inside your folder project
`cd my firstApp/` 

A basic Angular project structure:

![Angular Basic Structure](https://images.innoveduc.fr/angular/angular_part1_structure.png)

Here are the most important folder and files :

• Le fichier package.json contiendra toutes les dépendances de notre projet.

Pour ajouter une librairie au projet on l'installe : `npm i libraryName --save`
Penser au paramètre de la commande --save afin d'jouter la librairie au fichier package.json.

• Si on clone un projet ou qu'on pull une branche `npm i` pour installer les dépendances nouvellement listées dans le fichier package.json

•
Le dossier src contiendra tous le code du projet.

•
Le dossier app est le dossier module, il est généré par défault lors de la création d'un projet Angular.

•
Le app.module.ts est le fichier module. C'est un fichier de configuration essentiel.
Parfois si on veut utiliser une librairie additionnelle installée vie npm, il sera nécéssaire de déclarer ses modules à l'intérieur de ce fichier.

Il faudra aussi lister tous nos services à l'intérieur de ce fichier (à compléter via une prochaine quete).

•
Le fichier app.component.ts contient tous le code typescript du composant.
Il contient une class nommée AppComponent. Cette class contient un attirbut nommé title, qui sera affiché dans la partie HTML du composant.

•
Le fichier app.component.html contient tout le HTML du composant du projet. On peut voir dans ce fichier “Welcome to {{title}}!” , les doubles accolades (braces) sont appelées interpolation. Celà veut dire qu'Angular les remplaces avec la valeur de l'attribut "title" présent dans la partie Typescript du composant (voir au dessus). 

• Le fichier app.component.css contient tous le CSS qui sera appliqué à ce composant.

• Le dossier assets contiendra tous les fichiers images, polices, fichiers pdf ... de notre projet.

•Le fichier index.html contiendra la structure HTML de base de notre site web.
Si on veut ajouter des métadatas ou autre choes dans l'en-tête on doit le faire dans ce fichier.
Pas de code dans ce fichier, tous le code doit être mis dans les composants.

• Le fichier style.css contiendra le code CSS qui affectera tous le site web.
En cas de CSS inhérant à un composant particulier le placer directement dans le fichier CSS du dit composant.

## 2 Run your project

Run your project `ng serve -o` le paramètre -o oruvrira le navigateur. l'adresse par défaut est (http://localhost:4200/).

Le projet par défaut :

![Angular default website](https://images.innoveduc.fr/angular/angular_part1_welcomepage.png).

On peut voir le site web montrer le AppComponent. C’est parce que dans le fichier index.html, il y a cette balise `<app-root></app-root>`. Si on coche le début du fichier app.component.ts, on voit que le sélecteur de ce composant est app-root. Cela signifie que nous pouvons montrer un composant simplement en ajoutant la balise correcte qui correspond au sélecteur du composant.

## 02 - Angular - Le binding

Le système de template d’Angular nous propose une syntaxe puissante pour exprimer les parties dynamiques de notre HTML. Elle nous permet de faire du binding de données, de propriétés, d’événements, et des considérations de templating.

### Objectifs

• Comprendre l’interpolation

• Comprendre le property binding

• Comprendre l’event-binding

• Comprendre le two-way binding

#### L'interpolation

L'interpolation sert à afficher le contenu d'une variable dans la page HTML. Pour cela, on peut utiliser le signe `{{ }}`.

#### Le binding de propriété

Ce binding permet d'injecter une variable dans une propriété HTML. Pour cela, on utilise le signe `[]`.

#### Le binding d'événements

Ce binding permet de passer de l'information du HTML vers le TS. Pour cela, on utiliser le signe `()`.

On peut écouter les événements de l'utilisateur, comme par exemple le clic de la souris, ou encore la frappe sur le clavier.

#### Le binding two-way

Ce binding permet de passer de l'information du HTML vers le TS. Pour cela, tu peux utiliser le signe `[()]`.

Ajouter les `FormsModule`das les imports[] de app.module.ts 
On peut écouter les événements de l'utilisateur et mettre à jour directement l'information dans le composant et le template HTML.
Désormais, à la saisie dans le champ input, l'utilisateur sera changé dynamiquement.

