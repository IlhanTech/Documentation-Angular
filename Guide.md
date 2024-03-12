# Documentation apprentissage d'Angular

# Sommaire 

### 1. Première grande partie
   #### 1.1 Introduction
   - Mise en contexte
   #### 1.2 Prérequis
   - Connaissances de base en HTML, CSS, et JavaScript
   - Introduction à TypeScript
   #### 1.3 Premiers pas avec Angular
   - Installation et configuration de l'environnement
   - Le premier composant Angular
   #### 1.4 Construisez des components
   - Data binding d'Angular et Affichez des données
   - Réagissez aux événements
   - Ajoutez des propriétés personnalisées
   #### 1.5 Structurez un document avec des directives
   - Conditionnez l'affichage des éléments
   - Affichez des listes
   - Ajoutez du style dynamique
   - Mettez de la classe
   #### 1.6 Modifiez l'affichage des données avec les pipes
   - Changez la casse
   - Formatez les dates
   - Formatez les chiffres
   #### 1.7 Introduction aux services et au routing
   - Partagez des données avec les Services
   - Centralisez votre logique avec les Services
   - Passez en SPA avec le routing
   - Passez d'une route à l'autre
   - Création et Utilisation d'une Route avec Paramètre
### 2. Deuxième grande partie
   #### 2.1 Les Observables
   - Comprendre la notion d'Observable
   - Opérateurs bas niveaux
   - Observables et Opérateurs hauts niveaux
   - Évitez les fuites mémoires
   #### 2.2 Les Formulaires
   - Formulaire basique avec Template Forms
   - Les formulaires réctifs avec Reactive Forms
   - Utilisation des Validators
   #### 2.3 Les requêtes
   - Envoyer des requêtes
   - Sécurisez vos requêtes
   #### 2.4 Modulariser son application
   - Organiser son code par module
   - Comprendre et utiliser le Lazy Loading
   - Contrôlez les accès avec les guards
### 3. Deuxième grande partie

# 1. Première grande partie

Dans cette première grande partie, nous jetterons les bases d'Angular, explorant son écosystème, ses composants, directives, et plus encore, pour bien démarrer votre voyage de développement d'applications web.


## 1.1 Introduction

### Mise en contexte :

Angular est un framework de développement pour construire des applications web dynamiques. Créé par Google, il a été lancé pour la première fois en 2010 sous le nom d'AngularJS, pour ensuite évoluer en Angular 2 (et versions ultérieures), marquant un changement significatif tant au niveau de l'architecture que de la performance. Angular utilise TypeScript, une surcouche de JavaScript, qui apporte des fonctionnalités de typage statique et d'orienté objet, facilitant le développement de grandes applications complexes.

L'un des principaux avantages d'Angular est sa capacité à créer des Single Page Applications (SPA) réactives et performantes. Le framework fournit une structure organisée pour le développement, comprenant des composants, des services, des directives, des modules, et plus encore, permettant ainsi une grande modularité et réutilisabilité du code. Angular intègre également un système de détection de changement efficace, un routing avancé, des formulaires dynamiques, et une communication HTTP simplifiée, entre autres.

Avec une communauté active et le soutien de Google, Angular continue d'évoluer, proposant régulièrement des mises à jour et des améliorations, ce qui en fait l'un des frameworks les plus populaires pour le développement front-end.

## 1.2 Prérequis

## Connaissances de base en HTML, CSS, et JavaScript

Pour suivre sans problème cette documentation sur Angular CLI il va vous falloir des bases dans les différents langages pilier du développement web.

Voici des ressources pour vous former dans ses grandes thématiques : 

### HTML

Voici les différentes ressources pour devenir opérationnel en HTML : 
- https://www.w3schools.com/html/html_intro.asp
- https://htmlreference.io/
- https://html.com/
- https://www.youtube.com/watch?v=mJgBOIoGihA&feature=youtu.be
- https://github.com/denysdovhan/learnyouhtml

### CSS

Voici les différentes ressources pour devenir opérationnel en CSS :
- https://www.youtube.com/watch?v=n4R2E7O-Ngo&feature=youtu.be
- https://www.w3schools.com/css/
- https://cssreference.io/
- https://learn.shayhowe.com/html-css/building-your-first-web-page/
- https://www.freecodecamp.org/learn/responsive-web-design/

### JAVASCRIPT

Voici les différentes ressources pour devenir opérationnel en Javascript : 

- https://roadmap.sh/javascript
- https://www.w3schools.com/js/
- https://javascript.info/
- https://www.javascripttutorial.net/
- https://www.youtube.com/watch?t=22&v=P7t13SGytRk&feature=youtu.be

### Introduction à TypeScript

Pour être alaise sur le Framework Angular vous allez avoir besoin de voir le TypeScript. Pour vous formez rapidement la dessus vous pouvez utiliser le site : 

- https://scrimba.com/learn/typescript/

Si vous souhaitez voir Typescript dans les moindres détails vous pouvez utiliser cette Roadmap pour être sur de ne rien oublier :

- https://roadmap.sh/typescript


## 1.3 Premiers pas avec Angular 

### Installation et configuration de l'environnement

Nous allons débuter cette introduction à Angular avec un tutoriel d'installation :

#### Étape 1: Vérifiez votre installation de Node.js et npm

Angular CLI requiert Node.js version 10.13 ou plus récente, ainsi que npm (Node Package Manager), qui est installé avec Node.js par défaut.

Ouvrez un terminal ou une invite de commande.

Tapez `node -v` pour vérifier votre version de Node.js. Elle doit être 10.13 ou plus récente.

Tapez `npm -v` pour vérifier votre version de npm.

Si vous n'avez pas Node.js ou si votre version est trop ancienne, téléchargez et installez la dernière version stable de Node.js depuis le site officiel de Node.js : 

- https://nodejs.org/en

#### Étape 2: Installer Angular CLI

Dans votre terminal, exécutez la commande suivante pour installer Angular CLI globalement sur votre machine :

```sh
npm install -g @angular/cli
```

Cette commande télécharge et installe la dernière version d'Angular CLI, la rendant accessible depuis n'importe quel dossier sur votre système.

#### Étape 3: Vérifiez l'installation d'Angular CLI

Une fois l'installation terminée, vous pouvez vérifier si Angular CLI a été correctement installé en exécutant :

```sh
ng version
```

Cette commande affiche la version d'Angular CLI installée ainsi que quelques détails sur l'environnement de développement, comme les versions de Node.js et npm.

#### Étape 4: Créer un nouveau projet Angular

Maintenant que Angular CLI est installé, vous pouvez créer un nouveau projet Angular en exécutant :

```sh
ng new "Nom du Projet" --no-standalone --routing --ssr=fals --style=scss --skip-tests=true
```
Avant de passer à la suite j'aimerais faire un point sur les différents flags que nous utilisons ici pour la création de votre environnement de développement Angular : 

`ng new "Nom du Projet"` : Crée un nouveau projet Angular avec le nom spécifié.

`--no-standalone` : Ce drapeau spécifie que les nouveaux composants, directives et pipes créés dans le projet ne seront pas en mode standalone par défaut. Cela signifie que l'utilisation traditionnelle des NgModules est privilégiée dans ce projet. Dans le contexte actuel d'Angular, où les composants standalone commencent à être une option pour simplifier les applications en réduisant la dépendance aux NgModules, utiliser `--no-standalone` pourrait être une manière de maintenir une approche plus traditionnelle pendant la transition vers des pratiques de développement plus modernes.

`--routing` : Active le système de routage Angular dans le projet. Cela crée un module de routage (AppRoutingModule), qui est utilisé pour configurer les routes de l'application.

`--ssr=false` : Désactive la configuration du rendu côté serveur (Server-Side Rendering, SSR) pour le projet. Le SSR est une technique utilisée pour améliorer le référencement (SEO) et la performance initiale de l'application en rendant les pages côté serveur.

`--style=scss` : Configure le préprocesseur CSS à utiliser pour les styles de l'application. En choisissant SCSS, vous pourrez utiliser les fonctionnalités avancées de Sass pour écrire des feuilles de style plus expressives et maintenables.

`--skip-tests=true` : Désactive la génération de fichiers de test pour les nouveaux composants. Cela peut être utile pour accélérer la création initiale du projet si vous prévoyez d'ajouter des tests plus tard ou si vous utilisez une stratégie de test différente.

Chacun de ces drapeaux est conçu pour vous permettre de personnaliser l'initialisation de votre projet Angular selon vos besoins spécifiques, que ce soit en termes de structure de projet, de préférences de style, de stratégie de test, ou d'autres considérations de développement.


### Le premier composant Angular

Le mot component en anglais signifie "composant", et à juste titre : les components sont les composants de base d'une application Angular. Une application Angular peut être vue comme une arborescence de components avec AppComponent comme component racine.

Pour générer un component il faut vous mettre à la racine de votre projet et faire la commande : 

```sh
ng generate component "nom du composant"
```

Vous pouvez aussi juste faire : 

```sh
ng g c "nom du composant"
```

Vous aurez alors ça :

- https://user.oc-static.com/upload/2021/11/04/16360244739337_Screenshot%202021-11-04%20at%2012.14.22.png

Un nouveau dossier avec : 
  - Un fichier .scss
  - Un fichier .html
  - Un fichier .ts

Le framework mettra automatiquement votre app.module.ts à jour de cette manière votre composant sera inclus à la racine de votre application.

Pour en savoir plus sur le contenu de votre fichier .ts et du fichier app.module.ts vous pouvez vous rendre dans ce cours où tout est détaillé et expliqué :

- https://openclassrooms.com/fr/courses/7471261-debutez-avec-angular/7549291-construisez-votre-premier-component

Si vous voulez lancer votre application Angular, vous allez devoir vous rendre à la racine de votre projet et exécuter la commande : 

```sh
ng serve
```

Cela lancera votre application en mode watcher ainsi vous pourrez la laisser tourner sans l'arrêter et chaque modification que vous enregistrerez dans votre IDE sera automatique reporter sur le code, vous pourrez ainsi voir votre page web ou votre projet se construire sans relancer l'application.


## 1.4 Construisez des components

### Data binding d'Angular et Affichez des données

Dans une application Angular, le data binding (liaison de données) est un concept clé qui permet l'interaction entre le modèle de données de l'application (généralement défini dans les classes de composants TypeScript) et la vue (les templates HTML). Angular fournit plusieurs formes de data binding pour gérer différentes situations:

- String Interpolation: Utilisez `{{ }}` pour afficher le contenu des propriétés TypeScript dans votre HTML. Par exemple, {{ title }} affichera la valeur de la propriété title dans le template.

- Property Binding: Utilisez `[ ]` pour lier une propriété d'un élément HTML à une propriété du composant. Par exemple, `[src]="imageUrl"` relie l'attribut src d'une balise `<img>` à la propriété imageUrl du composant.

- Event Binding: Utilisez `( )` pour répondre aux événements du DOM dans votre composant. Par exemple, `(click)="handleClick()"` appelle la méthode `handleClick()` de votre composant lorsque l'élément est cliqué.

- Two-way Binding: Utilisez `[( )]` pour créer une liaison bidirectionnelle, principalement utilisée avec les formulaires. Par exemple, `[(ngModel)]="username"` lie la propriété `username` à un champ de formulaire, permettant une mise à jour mutuelle de la valeur entre le modèle et la vue.

En résumé, le data binding en Angular facilite la communication entre le modèle de données et la vue, permettant ainsi une programmation réactive et dynamique des applications web.

Voici un exemple d'un fichier component.ts avec les différentes déclarations et l'initialisation de certaines valeurs : 

```typescript
import { Component, OnInit } from '@angular/core';

@Component({
   selector: 'app-face-snap',
   templateUrl: './face-snap.component.html',
   styleUrls: ['./face-snap.component.scss']
})
export class FaceSnapComponent implements OnInit {
   title!: string;
   description!: string;
   createdDate!: Date;
   snaps!: number;

   ngOnInit() {
      this.title = 'Archibald';
      this.description = 'Mon meilleur ami depuis tout petit !';
      this.createdDate = new Date();
      this.snaps = 6;
   }
}
```

Ce code définit un composant Angular nommé FaceSnapComponent, qui affiche des informations sur un élément appelé "FaceSnap". Ce composant est décoré avec @Component pour spécifier son sélecteur CSS, le chemin vers son template HTML, et le chemin vers son fichier de styles SCSS.

Le composant implémente l'interface OnInit, ce qui signifie qu'il contient une méthode ngOnInit() qui est appelée automatiquement par Angular lors de l'initialisation du composant. Dans cette méthode, les propriétés title, description, createdDate, et snaps sont initialisées avec des valeurs spécifiques. Ces propriétés sont ensuite prêtes à être utilisées dans le template HTML du composant pour afficher dynamiquement les données à l'utilisateur.

Ensuite dans la template html nous allons pouvoir faire notre string interpolation et ainsi retrouver les variables de la classe FaceSnapComponent que nous avons déclaré plus tôt : 

```html
<h2>{{ title }}</h2>
<p>Mis en ligne le {{ createdDate }}</p>
<p>{{ description }}</p>
<p>🤌 {{ snaps }}</p>
```

Ainsi une fois appeler comme ceci dans app.component.html :

```html
<app-face-snap></app-face-snap>
<app-face-snap></app-face-snap>
<app-face-snap></app-face-snap>
<app-face-snap></app-face-snap>
```

Nous pourrons voir afficher sur notre page les informations suivantes : 

- https://user.oc-static.com/upload/2021/11/04/16360383799626_Screenshot%202021-11-04%20at%2016.05.39.png

En Angular nous pouvons aussi faire de l'Attribut Binding ça veut dire que vous pouvez avec des simples `[ ]` donner à un attribut Html une propriété TypeScript, par exemple si dans notre classe nous rajoutons une propriété :

```typescript
imageUrl!: string;
// ...
this.imageUrl = 'https://cdn.pixabay.com/photo/2015/05/31/16/03/teddy-bear-792273_1280.jpg';
```

Nous allons pouvoir les associés avec nos crochets comme ceci : 

```html
<img [src]="imageUrl" [alt]="title">
```

Ensuite nous pouvons ajouter du style à notre composant en rajoutant par exemple une Div. Globalement le CSS Angular fonctionne comme du CSS classique. 


Ajoutons notre div : 

```html
<div class="face-snap-card">
  <h2>{{ title }}</h2>
  <p>Mis en ligne le {{ createdDate }}</p>
  <img [src]="imageUrl" [alt]="title">
  <p>{{ description }}</p>
  <p>🤌 {{ snaps }}</p>
</div>
```

Ensuite nous pouvons ajouter du CSS dans le fichier .scss de notre composant : 

```css
.face-snap-card {
  width: 35%;
  img {
    width: 100%;
  }
}
```

Si vous voulez approfondir cette partie vous pouvez retrouver la plupart des exemples dans ce chapitre de ce cours : 

- https://openclassrooms.com/fr/courses/7471261-debutez-avec-angular/7549296-affichez-des-donnees


### Réagissez aux événements

La gestion des événements dans Angular est très largement simplifiée. Par exemple pour le click.
Nous allons ajouter un bouton dans le fichier html de notre composant : 

```html
<p>
  <button>Oh Snap!</button>
  🤌 {{ snaps }}
</p>
```

Une fois le bouton ajouté nous allons faire une nouvelle méthode dans notre classe afin d'interagir avec celui-ci : 

```typescript
onAddSnap() {
  this.snaps++;
}
```

La méthode étant implémentée nous pouvons tout simplement la lier à notre bouton comme ceci afin de gérer notre premier événement et ainsi incrémenter notre compteur à chaque fois que le bouton sera cliqué :

```html
<button (click)="onAddSnap()">Oh Snap!</button>
```

### Ajoutez des propriétés personnalisées

Nous allons maintenant créer un modèle de classe ce qui va nous de créer plusieurs instances de la même classe avec des données différentes.

Pour créer un modèle de cette classe nous allons tout simplement créer un dossier avec tous nos modèles que nous allons appeler models et dedans nous allons créer un fichier pour notre classe nommé `face-snap.model.ts`. Dedans nous allons tout simplement mettre notre classe avec nos différentes propriétés : 

```typescript
export class FaceSnap {
  id!: number;
  title!: string;
  description!: string;
  imageUrl!: string;
  createdDate!: Date;
  snaps!: number;
  location?: string;
}
```

Pour qu'une propriété puisse être injectée depuis l'extérieur d'un component, il faut lui ajouter le décorateur `@Input()`, à l'intérieur du composant dans lequel on veut l'utiliser, comme ceci : 

```typescript
@Input() faceSnap!: FaceSnap;
```

Attention n'oubliez pas d'importer votre modèle : 

```typescript
import { FaceSnap } from '../models/face-snap.model';
```

Vous pouvez maintenant l'utiliser de cette mannière : 

Déclaration des objets : 

```typescript
mySnap!: FaceSnap;
myOtherSnap!: FaceSnap;
myLastSnap!: FaceSnap;
```

Initialisation des objets :

```typescript
this.mySnap = {
  title: 'Archibald',
  description: 'Mon meilleur ami depuis tout petit !',
  imageUrl: 'https://cdn.pixabay.com/photo/2015/05/31/16/03/teddy-bear-792273_1280.jpg',
  createdDate: new Date(),
  snaps: 0
};
this.myOtherSnap = {
  title: 'Three Rock Mountain',
  description: 'Un endroit magnifique pour les randonnées.',
  imageUrl: 'https://upload.wikimedia.org/wikipedia/commons/thumb/0/08/Three_Rock_Mountain_Southern_Tor.jpg/2880px-Three_Rock_Mountain_Southern_Tor.jpg',
  createdDate: new Date(),
  snaps: 0
};
this.myLastSnap = {
  title: 'Un bon repas',
  description: 'Mmmh que c\'est bon !',
  imageUrl: 'https://wtop.com/wp-content/uploads/2020/06/HEALTHYFRESH.jpg',
  createdDate: new Date(),
  snaps: 0
};
```

Ensuite dans la partie html grâce à `@Input()` crée comme un attribut HTML auquel on peut lier une valeur, tout comme vous l'avez fait avec l'attribut  src  de l'élément image !. Nous pourrons ainsi utiliser l'attribute binding pour lier ces objets à la propriété personnalisée `faceSnap` : 


```html
<app-face-snap [faceSnap]="mySnap"></app-face-snap>
<app-face-snap [faceSnap]="myOtherSnap"></app-face-snap>
<app-face-snap [faceSnap]="myLastSnap"></app-face-snap>
```

Afin de rendre le composant générique et qu'il soit réutilisable nous pouvons modifier ça template HTML pour utiliser les bonnes propriétés : 

```html
<div class="face-snap-card">
  <h2>{{ faceSnap.title }}</h2>
  <p>Mis en ligne le {{ faceSnap.createdDate }}</p>
  <img [src]="faceSnap.imageUrl" [alt]="faceSnap.title">
  <p>{{ faceSnap.description }}</p>
  <p>
    <button (click)="onSnap()">{{ buttonText }}</button>
    🤌 {{ faceSnap.snaps }}
  </p>
</div>
```

Si vous voulez approfondir cette partie vous pouvez retrouver la plupart des exemples dans ce chapitre de ce cours : 

- https://openclassrooms.com/fr/courses/7471261-debutez-avec-angular/7549306-ajoutez-des-proprietes-personnalisees

## 1.5 Structurez un document avec des directives

### Conditionnez l'affichage des éléments

Dans notre classe `FaceSnap` nous avons une propriété non obligatoire déclarée comme ceci : 

```typescript
location?: string;
```

Avec Angular nous pouvons utiliser des directives afin de conditionner des appels de certains blocs HTML dans le DOM comme ci-dessous :

```html
<p *ngIf="faceSnap.location">Photo prise à {{ faceSnap.location }}</p>
```

Nous avons `*ngIf` qui va détecter si la propriété non obligatoire `location` existe bel et bien, si oui le bloc dans lequel elle se situe sera insérer au DOM. Si `location` n'est pas détecté le bloc HTML ne sera pas inséré.

### Affichez des listes

Il existe beaucoup d'autres directive mais nous allons voir la directive `*ngfor`, qui est une directive permettant d'itérer sur des tableaux et créer autant d'élément HTML que nous aurons des cases dans notre tableau. Pour cela nous allons devoir créer un array de FaceSnap comme ceci :

```typescript
faceSnaps!: FaceSnap[];
```

Ensuite nous allons le remplir : 

```typescript
ngOnInit() {
  this.faceSnaps = [
    {
      title: 'Archibald',
      description: 'Mon meilleur ami depuis tout petit !',
      imageUrl: 'https://cdn.pixabay.com/photo/2015/05/31/16/03/teddy-bear-792273_1280.jpg',
      createdDate: new Date(),
      snaps: 0,
      location: 'Paris'
    },
    {
      title: 'Three Rock Mountain',
      description: 'Un endroit magnifique pour les randonnées.',
      imageUrl: 'https://upload.wikimedia.org/wikipedia/commons/thumb/0/08/Three_Rock_Mountain_Southern_Tor.jpg/2880px-Three_Rock_Mountain_Southern_Tor.jpg',
      createdDate: new Date(),
      snaps: 6,
      location: 'la montagne'
    },
    {
      title: 'Un bon repas',
      description: 'Mmmh que c\'est bon !',
      imageUrl: 'https://wtop.com/wp-content/uploads/2020/06/HEALTHYFRESH.jpg',
      createdDate: new Date(),
      snaps: 0
    }
  ];
}
```

Ensuite une fois que cela est fait nous allons dans notre `app.component.html` appeler notre component avec la directive `*ngFor` afin d'itérer sur notre tableau de `FaceSnap` et créer autant d'élément qu'il y aura de case dans notre tableau.

```html
<app-face-snap *ngFor="let faceSnapElementInArray of faceSnaps" [faceSnap]="faceSnapElementInArray"></app-face-snap>
```

### Ajoutez du style dynamique

Pour ajoutez du style dynamique nous allons pouvoir utiliser la directive `[ngStyle]`. La directive `[ngStyle]` offre une méthode flexible et puissante pour appliquer dynamiquement des styles CSS aux éléments HTML.

Voici un petit exemple : 

```typescript
import { Component } from '@angular/core';

@Component({
  selector: 'app-mon-composant',
  templateUrl: './mon-composant.component.html',
  styleUrls: ['./mon-composant.component.css']
})
export class MonComposantComponent {
  taille: number = 20; // Taille de police initiale
  couleur: string = 'blue'; // Couleur initiale
}

```

Dans le fichier template de votre composant (HTML), utilisez la directive `[ngStyle]` pour lier dynamiquement les propriétés de style à vos données de composant.

```html
<div [ngStyle]="{'font-size.px': taille, 'color': couleur}">
  Texte stylé dynamiquement
</div>
```

Vous pouvez modifier les styles dynamiquement en changeant les valeurs des propriétés dans votre composant. Voici comment vous pourriez ajouter des méthodes pour changer la taille et la couleur:

```typescript
changerTaille(taille: number) {
  this.taille = taille;
}

changerCouleur(couleur: string) {
  this.couleur = couleur;
}
```

### Mettez de la classe

Avec Angular il existe une directive permettant d'appliquer une classe à un élément HTML en fonction d'une condition. Cette directive s'appelle `[ngClass]`. Ci-dessous vous retrouverez un exemple d'une classe CSS attribué à un élément HTML grâce à une condition.


```css
.snapped {
  background-color: rgba(lightgreen, 0.4);
  color: darkgreen;
  button {
    box-shadow: lightgreen 3px 3px 7px;
    color: darkgreen;
    &:active {
      box-shadow: lightgreen 0 0 5px;
    }
  }
}
```

```html
<div class="face-snap-card" [ngClass]="{ snapped: buttonText === 'Oops, unSnap!' }">
```

Vous pouvez retrouver la condition qui dit que si la propriété TypeScript `buttonText` vient à être strictement égal à `Oops, unSnap!` la classe CSS s'appliquera.


## 1.6 Modifiez l'affichage des données avec les pipes

### Changez la casse

Avec Angular nous avons les pipes qui nous permette de formater une valeur qu'on lui passe sans toucher à la donnée sous-jacente. Voici un exemple ci-dessous des différents pipes existant : 

```html
<h2>{{ faceSnap.title | uppercase }}</h2>
<h2>{{ faceSnap.title | lowercase }}</h2>
<h2>{{ faceSnap.title | titlecase }}</h2>
```

Je tiens à répéter que les pipes ne changent rien à la valeur des variables sous-jacentes. Les pipes existent uniquement pour modifier le formatage affiché d'une donnée : on ne peut pas les utiliser ailleurs que dans le template, et il est fortement déconseillé de les utiliser ailleurs que dans une string interpolation.

### Formatez les dates

En Angular il existe aussi des pipes configurables comme le `DatePipe`. Vous retrouverez ci-dessus différentes configurations de ce `DatePipe` :

```html
<p>Mis en ligne le {{ faceSnap.createdDate | date }}</p>
<p>Mis en ligne le {{ faceSnap.createdDate | date: 'longDate' }}<p>
<p>Mis en ligne le {{ faceSnap.createdDate | date: 'dd/MM/yy, à HH:mm' }}</p>
<p>Mis en ligne {{ faceSnap.createdDate | date: 'à HH:mm, le d MMMM yyyy' }}</p>
```

Vous pouvez aussi configurer le fuseau horaire que vous souhaitez dans `app.module.ts` comme ceci : 


```typescript
import { LOCALE_ID, NgModule } from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';

import { AppComponent } from './app.component';
import { FaceSnapComponent } from './face-snap/face-snap.component';
import { registerLocaleData } from '@angular/common';
import * as fr from '@angular/common/locales/fr';

@NgModule({
  declarations: [
    AppComponent,
    FaceSnapComponent
  ],
  imports: [
    BrowserModule
  ],
  providers: [
    { provide: LOCALE_ID, useValue: 'fr-FR'}
  ],
  bootstrap: [AppComponent]
})
export class AppModule {
  constructor() {
    registerLocaleData(fr.default);
  }
}
```

### Formatez les chiffres

Vous pouvez de la même manière que le `DatePipe` configurer votre pipe `number` pour afficher les décimals souhaitées :

```html
<p>{{ 4346234.36 | number }}</p>
<p>{{ 4346234.36 | number: '1.0-0' }}</p>
<p>{{ 4346234.36 | number: '1.0-1' }}</p>
```

Vous pouvez faire ça aussi avec les pourcentages avec le pipe `percent` : 

```html
<p>{{ 0.336 | percent }}</p>
<p>{{ 0.336 | percent: '1.0-1' }}</p>
```

Vous avez aussi le pipe `currency` :

```html
<p>{{ 344.36 | currency }}</p>
<p>{{ 344.36 | currency: 'EUR' }}</p>
<p>{{ 344.36 | currency: 'EUR' : 'code' }}</p>
```
## 1.7 Introduction aux services et au routing

### Partagez des données avec les Services

Pour partager les données et que tous vos composants s'échangent les mêmes données nous allons utiliser les services. Par exemple dans le cas présent nous créons un service qui va contenir un array où seront stockées des informations que nos components vont devoir restituer.

Nos services se trouveront dans le dossier `app` qui lui contiendra un dossier `services` avec un fichier `"nomduservice".service.ts` .
Un service est une classe, et la façon la plus simple de déclarer une classe comme étant un service est d'utiliser le décorateur  @Injectable()  qui s'importe depuis  @angular/core :

```typescript
import { Injectable } from '@angular/core';
import { FaceSnap } from './models/face-snap.model';

@Injectable({
  providedIn: 'root'
})
export class FaceSnapsService {
  faceSnaps: FaceSnap[] = [
      // vos FaceSnap ici
  ]
}
```

L'objet de configuration qui spécifie `providedIn: 'root'`  dit à Angular d'enregistrer ce service à la racine de l'application. Ce sera très souvent le cas pour vos services, car ça permet de s'assurer de n'avoir qu'une seule instance du service, partagée par tous les partis intéressés.

Ensuite pour pouvoir utiliser un service dans un component nous utiliserons le système d'injection de dépendances que fournit Angular : 

```typescript
import { FaceSnapsService } from '../services/face-snaps.service';
//...
constructor(private faceSnapsService: FaceSnapsService) { }
```

Vous pouvez ainsi l'utiliser dans la classe suivante comme ceci : 

```typescript
ngOnInit(): void {
    this.faceSnaps = this.faceSnapsService.faceSnaps;
}
```

### Centralisez votre logique avec les Services

Vous pouvez retrouver une façon de centraliser la logique de vos services dans le chapitre de ce cours :

- https://openclassrooms.com/fr/courses/7471261-debutez-avec-angular/7567851-centralisez-votre-logique-avec-les-services


### Passez en SPA avec le routing

Angular fait partie des singles Pages Applications qui permettent une performance sans égale en enlevant le besoin d'une application de demander, recevoir, puis afficher une nouvelle page HTML à chaque changement d'URL. Le système de routing d'Angular nous permet de lier une URL (route) à un composant et voici comment le faire : 

```typescript
import { NgModule } from '@angular/core';
import { RouterModule, Routes } from '@angular/router';
import { FaceSnapListComponent } from './face-snap-list/face-snap-list.component';
import { LandingPageComponent } from './landing-page/landing-page.component';
import { SingleFaceSnapComponent } from './single-face-snap/single-face-snap.component';

const routes: Routes = [
  { path: 'facesnaps/:id', component: SingleFaceSnapComponent },
  { path: 'facesnaps', component: FaceSnapListComponent },
  { path: '', component: LandingPageComponent }
];
@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
})
export class AppRoutingModule { }

```

À la création de votre environnement de développement Angular normalement un fichier `app-routing.module.ts` a dû être créé. Ce fichier est celui qui va gérer la liaison entre vos routes et vos composants. 

### Passez d'une route à l'autre

Pour passer d'une route à une autre vous avez deux manières. Vous pouvez le faire via la template HTML de votre composant ou alors vous pouvez passer par une méthode Typescript que vous pourrez ensuite lier à un événement : 

```html
<a routerLink="facesnaps">Continuer vers Snapface</a>
```

Vous utilisez `routerLink` avec le nom de votre route.
Sinon vous pouvez injecter le Router dans votre composant : 

```typescript
import { Router } from '@angular/router';
//...
constructor(private router: Router) { }
```

Pour ensuite utiliser `navigateByUrl()` dans la méthode que vous souhaiterez : 

```typescript
onContinue() {
    this.router.navigateByUrl('facesnaps');
}
```

Ensuite cette méthode vous n'aurez plus qu'à la lier à un bouton appeler dans la template HTML de votre composant, qui réagira une fois cliquer : 

```html
<button (click)="onContinue()">Continuer vers Snapface</button>
```

### Création et Utilisation d'une Route avec Paramètre

```typescript
const routes: Routes = [
  { path: 'facesnaps/:id', component: SingleFaceSnapComponent },
];
```

Avec Angular nous avons accès dans Router à une propriété nommée `ActivatedRoute`. Cette propriété nous permet d'avoir des routes paramétrables c'est-à-dire qu'elles vont prendre un paramètre par exemple un id : 

```typescript
import { Component, OnInit } from '@angular/core';
import { FaceSnap } from '../models/face-snap.model';
import { FaceSnapsService } from '../services/face-snaps.service';
import { ActivatedRoute } from '@angular/router';

@Component({
  selector: 'app-single-face-snap',
  templateUrl: './single-face-snap.component.html',
  styleUrl: './single-face-snap.component.scss'
})
export class SingleFaceSnapComponent implements OnInit {
  faceSnap!: FaceSnap;
  buttonText!: string;

  constructor(private faceSnapsService: FaceSnapsService,
    private route: ActivatedRoute) {
  }

  ngOnInit() {
    const snapId = +this.route.snapshot.params['id'];
    this.faceSnap = this.faceSnapsService.getFaceSnapById(snapId);
  }
}
```

Nous pouvons ainsi récupérer le paramètre de la route et l'assigner à une variable dans notre code.

# 2. Deuxième grande partie

Dans cette seconde partie nous allons entrer plus en profondeur dans le langage Angular et voir davantage d'interaction que ça soit avec le serveur ou encore avec l'utilisateur. Vous verrez aussi la modularité et comment tirer parti de cette modularité afin de gagner en performances.

## 2.1 Les Observables

### Comprendre la notion d'Observable

Dans les applications web sans framework, la gestion de l'asynchrone se fait généralement avec trois outils :

- les callbacks : des fonctions appelées lorsque l'événement attendu a lieu
 
- les Promise : des objets avec des méthodes `then()` et `catch()` qui sont appelées lorsque l'événement attendu a lieu

- les fonctions async/await : des fonctions qui mettent leur exécution en attente jusqu'à l'arrivée de l'événement attendu.

Angular, étant un framework très complet, nous fournit un nouvel outil pour gérer des événements qui ont lieu au cours du temps : la library RxJS et ses Observables.

Un Observable est un objet qui émet des valeurs au cours du temps, il est typé, il émettra toujours des valeurs du même type. Si un Observable émet une erreur à ce moment la il est détruit et n'émet plus de valeurs. Un Observable peut également être complété c'est-à-dire qu'il accomplira entièrement la tâche pour laquelle il a été déclaré.

Pour qu'un Observable fonctionne ou se mette à faire la tâche qu'on lui demande il faut y souscrire avec sa propre méthode `subscribe()`.

Voici un exemple ci-dessous de la création d'un Observable :

```typescript
import { Component, OnInit } from '@angular/core';
import { interval } from 'rxjs';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss']
})
export class AppComponent implements OnInit {

  ngOnInit() {
    const interval$ = interval(1000);
    interval$.subscribe(value => console.log(value));
  }
}
```

Dans cette exemple nous importons la méthode `interval()` depuis `rxjs` pour créer un Observable qui émet des nombres croissants, en passant le nombre de millisecondes qui doit séparer les émissions. Vous stockez cet Observable dans une constante nommée  `interval$`. 

La norme est d'ajouter un `$` à la fin du nom de toute variable qui contient un Observable. 

Pour illustrer très simplement le système d'Observable nous allons y souscrire directement récupérer ça valeur et la print dans la console du navigateur.

Si vous ouvrez la console du navigateur vous pourrez voir ça : 

- https://user.oc-static.com/upload/2021/11/29/16382242493648_Screenshot%202021-11-29%20at%2023.17.07.png


La plupart du temps quand vous voudrez afficher les émissions d'un Observable vous voudrez les afficher dans le DOM et non uniquement dans la console de votre navigateur. Pour faire cela Angular nous founit le pipe `async`. Contrairement à tous les autres pipes que vous avez rencontrés jusqu'ici, le pipe `async` ne formate pas des données : il souscrit à un Observable et insère les émissions dans le DOM. 

Voici un exemple de l'utilisation d'un Observable avec le pipe `async` : 

Dans le fichier `.ts` :

```typescript
import { Component, OnInit } from '@angular/core';
import { interval, Observable } from 'rxjs';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss']
})
export class AppComponent implements OnInit {

  interval$!: Observable<number>;

  ngOnInit() {
    this.interval$ = interval(1000);
  }
}
```

Dans la template HTML : 

```html
<h1>{{ interval$ | async }}</h1>
```

Comme vous pouvez le constater, quand on déclare le type de `interval$`, on le déclare comme `Observable` qui émet des `number` en passant `number` entre chevrons `<>`.

Certes cet exemple est très simple et n'est pas très utile, mais le concept de souscrire à un Observable, que ce soit avec la méthode `subscribe()` ou le pipe `async`, est très important – vous vous en servirez très, très souvent.

Dans le DOM, vous voyez maintenant les nombres qui augmentent :
- https://user.oc-static.com/upload/2021/11/30/16382650189947_Screenshot%202021-11-30%20at%2010.35.24.png


### Opérateurs bas niveaux

Les Observables occupent une place très importante dans le framework d'Angular, et nous permettent de créer des fonctionnalités très avancées et complexes beaucoup plus facilement. Il est donc essentiel de maîtriser la manipulation de ces Observables. Cette manipulation se fait avec les opérateurs.

Il existe deux types principaux d'opérateurs :

- les opérateurs bas niveau – ces opérateurs touchent aux émissions directement, généralement pour transformer ou filtrer ces émissions, et sont le sujet de ce chapitre

- les opérateurs haut niveau – ces opérateurs touchent à l'Observable lui-même, et nous en parlerons dans le prochain chapitre.

Pour appliquer des opérateurs à un Observable, on les passe, dans l'ordre, à une méthode qui s'appelle `pipe()` :

```typescript
const modifiedObservable$ = originalObservable$.pipe(
    firstOperator(),
    secondOperator(arguments),
    thirdOperator
);
```

Vous pouvez voir un exemple de l'utilisation de pipe bien sûr les noms ne sont pas les bons c'est un exemple.

Vous créez un nouvel Observable en branchant un "tuyau" à un autre Observable et en y ajoutant les opérateurs que vous voulez y ajouter. Le concept de "tuyau", pipe, en anglais, est très utile : chaque émission de l'Observable traverse le tuyau et donc les opérateurs dans l'ordre.

Voici un exemple concret.

Le premier opérateur que vous allez utiliser est l'opérateur `map()`qui permet de transformer les émissions d'un Observable. Utilisons notre Observable `interval$` pour un premier exemple simple :

```typescript
interval$!: Observable<number>;
```

```typescript
this.interval$ = interval(1000).pipe(
    map(value => value * 10)
);
```
N'oubliez pas d'importer `map` depuis `rxjs/operators`.

Voici un exemple très simple de l'utilisation de l'opérateur `map()` qui définit la transformation à effectuer. Ici, on multiplie chaque émission par 10.

Essayons quelque chose d'un peu plus complexe :

```typescript
this.interval$ = interval(1000).pipe(
    map(value => value % 2 === 0 ?
        `Je suis ${value} et je suis pair` :
        `Je suis ${value} et je suis impair`
    )
);
```

L'opérateur modulo `%` divise un nombre par un autre et retourne le reste. Si un nombre entier modulo 2 est égal à 0, le nombre est pair ; sinon, il est impair.

Mais vous allez vous apercevoir que ça ne compile pas. Parce qu'on a dit que `interval$`  allait émettre des `number`, et ici on lui demande d'émettre une `string` ! C'est bien l'émission finale qui définit le type de l'Observable global. Modifiez donc le type d' `interval$` :

```typescript
interval$!: Observable<string>;
```

Vous aurez alors un changement visuel entre pair et impair en fonction des émissions de votre Observable.

Ensuite vous allez être amenés à utiliser l'opérateur `filter()` qui va vous permettre de filtrer les émissions, laissant passer uniquement celles qui vous intéressent. Vous pouvez l'importer depuis `rxjs/operators` et l'ajoutez à `interval$` :

```typescript
this.interval$ = interval(1000).pipe(
    filter(value => value % 3 === 0),
    map(value => value % 2 === 0 ?
        `Je suis ${value} et je suis pair` :
        `Je suis ${value} et je suis impair`
    )
);
```

Comme vous pouvez le voir l'opérateur `filter()` va avoir une condition qui va lui permettre de laisser passer à l'opérateur `map()` uniquement les émissions qui nous intéressent, qui remplisse cette condition de filtrage.

Autre notion importante, la notion d'effets secondaires.

En programmation réactive, un effet secondaire est une fonction qui fait quelque chose avec les émissions d'un Observable sans les modifier. Pour ajouter un effet secondaire à un Observable, on utilise l'opérateur `tap()`.

D'abord nous allons implémenter une méthode très simple pour illustrer les effets secondaires : 

```typescript
logger(text: string): void {
    console.log(`Log: ${text}`);
}
```

Maintenant, en important  tap  depuis `rxjs/operators`, ajoutez l'opérateur à `interval$` :

```typescript
this.interval$ = interval(1000).pipe(
    filter(value => value % 3 === 0),
    map(value => value % 2 === 0 ?
        `Je suis ${value} et je suis pair` :
        `Je suis ${value} et je suis impair`
    ),
    tap(text => this.logger(text))
);
```

Vous pouvez voir que l'opérateur `tap()` va récupérer dans `text` la sortie de `map()` et va lancer avec son résultat la fonction logger qui va tout simple print dans la console le résultat de `map()` comme ceci : 

- https://user.oc-static.com/upload/2021/11/30/16382778957117_Screenshot%202021-11-30%20at%2014.10.02.png

### Observables et Opérateurs hauts niveaux

Les opérateurs hauts niveaux où Observable haut niveau est un Observable dont le travail est d'aller souscrire à d'autres Observables.

Prenons un cas concret pour illustrer ce propos.

Imaginez une application qui permet, avec un bouton, de basculer entre deux flux de caméra. Dans cette situation, on commence avec trois Observables :

- un Observable pour chaque caméra
- l'Observable des clics sur le bouton

Pour afficher le flux sélectionné, il faudra composer ces Observables pour créer un Observable haut niveau. On observera les clics du bouton, et selon la sélection, on ira souscrire au flux correspondant. 

Dans ce cas, on appellera le flux de clics l'Observable extérieur, et les flux des caméras les Observables intérieurs.

Un Observable haut niveau consiste donc en un Observable extérieur qui souscrit à des Observables intérieurs selon ses émissions. Quand l'Observable extérieur émet "caméra 1", il souscrit à l'Observable intérieur qui y correspond.

Ce sont les opérateurs haut niveau qui permettent ce type de souscription.

Ce qui fait la différence entre ces opérateurs, c'est comment ils gèrent la situation suivante :

- l'Observable extérieur a émis, et donc on a une première souscription à un Observable intérieur

- l'Observable extérieur émet de nouveau alors que l'Observable souscrit précédemment n'a pas encore complété.

RxJS nous propose quatre stratégies, et donc quatre opérateurs, précisément pour cette situation. Voici une analogie pour expliquer ces opérateurs.

Pour que vous puissiez mieux visualiser et comprendre le fonctionnement nous allons commencer avec le premier opérateur de haut niveau `mergeMap()`. L'opérateur haut niveau va : 

- Crée un nouvel observable pour chaque valeur émise par l'observable source.

- Souscrire immédiatement à chaque nouvel observable créé, permettant ainsi leur exécution "en parallèle".

- Fusionner les résultats de tous ces observable de sortie dès qu'elles sont disponibles, sans attendre que les autres observables aient complétés.

Pour résumer mergeMap prend chaque valeur émise par l'observable source, et pour chaque valeur, il crée un nouvel observable basé sur cette valeur (par exemple, en appliquant une fonction qui retourne un observable). mergeMap s'abonne ensuite à chaque nouvel observable créé et permet à chacun de ces observables de s'exécuter de manière asynchrone et indépendante. Dès qu'un de ces observables internes émet une valeur ou une série de valeurs, mergeMap les transmet immédiatement à l'observable de sortie. Ce processus continue jusqu'à ce que l'observable source soit complété.

mergeMap représente la mise en parallèle, nous l'utiliserons quand l'odre des souscriptions n'a pas besoin d'être conservé.


Ensuite nous verrons l'opérateur haut niveau `concatMap()` L'opérateur haut niveau va : 

- Créer un nouvel observable pour chaque valeur émise par l'observable source.

- Souscrire à chaque nouvel observable créé, mais de manière séquentielle, c'est-à-dire attendre que l'observable précédent ait terminé avant de souscrire au suivant.

- Fusionner les résultats de tous ces observables de sortie dans l'ordre où ils ont terminé, en respectant la séquence d'origine.

Pour résumer, `concatMap()` prend chaque valeur émise par l'observable source, et pour chaque valeur, il crée un nouvel observable basé sur cette valeur (par exemple, en appliquant une fonction qui retourne un observable). `concatMap()` s'abonne ensuite à chaque nouvel observable créé, mais contrairement à `mergeMap()`, il ne permet pas à ces observables de s'exécuter de manière asynchrone et indépendante. Au lieu de cela, `concatMap()` attend que chaque observable interne soit complété avant de s'abonner au suivant. Dès qu'un de ces observables internes émet une valeur ou une série de valeurs, `concatMap()` les transmet à l'observable de sortie. Ce processus continue jusqu'à ce que l'observable source soit complété.

`concatMap()` représente la mise en série, nous l'utiliserons quand l'ordre des opérations doit être conservé.


Poursuivons avec l'opérateur haut niveau `exhaustMap` : 

- Créer un nouvel observable pour chaque valeur émise par l'observable source.

- Souscrire au premier observable créé et ignorer les autres jusqu'à ce que cet observable soit complété.

- Fusionner les résultats de cet observable de sortie dans l'observable de sortie. Une fois que cet observable est complété, `exhaustMap()` souscrit à l'observable suivant qui a été créé pendant qu'il était occupé, s'il y en a un.

Pour résumer, `exhaustMap()` prend chaque valeur émise par l'observable source, et pour chaque valeur, il crée un nouvel observable basé sur cette valeur (par exemple, en appliquant une fonction qui retourne un observable). `exhaustMap()` s'abonne ensuite au premier observable créé et ignore les autres jusqu'à ce que cet observable soit complété. Contrairement à `mergeMap()` et `concatMap()`, `exhaustMap()` ne permet pas à plusieurs observables de s'exécuter de manière asynchrone ou séquentielle. Au lieu de cela, `exhaustMap()` attend que l'observable interne actuel soit complété avant de s'abonner à un autre. Dès qu'un observable interne émet une valeur ou une série de valeurs, `exhaustMap()` les transmet à l'observable de sortie. Ce processus continue jusqu'à ce que l'observable source soit complété.

`exhaustMap()` représente l'ignorance des valeurs émises pendant qu'un observable interne est en cours d'exécution, nous l'utiliserons quand nous voulons ignorer les nouvelles valeurs jusqu'à ce que l'observable actuel soit complété.


Finissons avec l'opérateur haut niveau `switchMap` :

- Créer un nouvel observable pour chaque valeur émise par l'observable source.

- Souscrire au nouvel observable créé et annuler la souscription à l'observable précédent, s'il y en a un.

- Fusionner les résultats du nouvel observable de sortie dans l'observable de sortie. Si un nouvel observable est créé avant que l'observable précédent ait terminé, `switchMap()` arrête de souscrire à l'observable précédent et commence à souscrire au nouvel observable.

Pour résumer, `switchMap()` prend chaque valeur émise par l'observable source, et pour chaque valeur, il crée un nouvel observable basé sur cette valeur (par exemple, en appliquant une fonction qui retourne un observable). `switchMap()` s'abonne ensuite au nouvel observable créé et annule la souscription à l'observable précédent, s'il y en a un. Contrairement à `mergeMap()`, `concatMap()` et `exhaustMap()`, `switchMap()` permet de changer d'observable en cours d'exécution. Dès qu'un nouvel observable est créé, `switchMap()` arrête de souscrire à l'observable précédent et commence à souscrire au nouvel observable. Ce processus continue jusqu'à ce que l'observable source soit complété.

`switchMap()` représente le changement d'observable en cours d'exécution, nous l'utiliserons quand nous voudrons annuler les effets de l'observable précédent chaque fois qu'une nouvelle valeur est émise par l'observable source.

Voilà vous avez vu les 4 types d'opérateurs aux niveaux existants cette partie est dense et avec beaucoup d'explication mais dans les faits vous allez voir que ce sont des concepts plutôt simples je vous propose un morceau de code tout prêt pour vous démontrer visuellement les différents opérateurs haut niveau, cette démonstration permettra d'illustrer leurs comportements.

Vous pouvez retrouver le code ci-dessous et le déclarer dans votre `AppComponents.ts` : 

```typescript
import { Component, OnInit } from '@angular/core';
import { interval, of } from 'rxjs';
import { concatMap, mergeMap, delay, exhaustMap, map, switchMap, take, tap } from 'rxjs/operators';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss']
})
export class AppComponent implements OnInit {

  redTrainsCalled = 0;
  yellowTrainsCalled = 0;

  ngOnInit() {
    interval(500).pipe(
      take(10),
      map(value => value % 2 === 0 ? 'rouge' : 'jaune'),
      tap(color => console.log(`La lumière s'allume en %c${color}`, `color: ${this.translateColor(color)}`)),
      mergeMap(color => this.getTrainObservable$(color)),
      tap(train => console.log(`Train %c${train.color} ${train.trainIndex} arrivé !`, `font-weight: bold; color: ${this.translateColor(train.color)}`))
    ).subscribe();
  }

  getTrainObservable$(color: 'rouge' | 'jaune') {
    const isRedTrain = color === 'rouge';
    isRedTrain ? this.redTrainsCalled++ : this.yellowTrainsCalled++;
    const trainIndex = isRedTrain ? this.redTrainsCalled : this.yellowTrainsCalled;
    console.log(`Train %c${color} ${trainIndex} appelé !`, `text-decoration: underline; color: ${this.translateColor(color)}`);
    return of({ color, trainIndex }).pipe(
      delay(isRedTrain ? 5000 : 6000)
    );
  }

  translateColor(color: 'rouge' | 'jaune') {
    return color === 'rouge' ? 'red' : 'yellow';
  }
}
```

Comme vous pouvez le voir tout ceci est imagé dans la console de votre navigateur avec un système de trains et de lumière. Cet exemple illustre bien les différents concepts. Je vous invite à jouer avec en modifiant à la ligne 20 la méthode `mergeMap()`, vous pouvez ainsi la remplacer par `concatMap()`, `exhaustMap` ou encore `switchMap`. 

### Évitez les fuites mémoires

Vos Observables sont très puissants : du coup, ils peuvent également être dangereux. Si votre application maintient une souscription à un Observable qui ne sert plus, vous générez une fuite de mémoire. En plus, ces fuites deviennent vite nombreuses et peuvent créer de gros problèmes de performance, même jusqu'à faire planter le navigateur !

Du coup, il vous faut absolument implémenter une stratégie pour unsubscribe (se désabonner) des Observables auxquels vous avez souscrit. 

Il faut uniquement que l'Observable complète si on n'en a plus besoin. Il y a deux cas principaux :

- Vous savez en avance combien d'émissions vous intéressent - souvent, seulement la première émission nous intéresse, ou les quelques premières.

- Vous avez besoin des émissions de l'Observable pendant toute la durée de vie du component.

Dans ces deux cas, vous allez utiliser des opérateurs spécifiques pour assurer la complétion, et donc la destruction, de l'Observable.

Le cas le plus simple est quand vous savez combien d'émissions vous intéressent. Souvent, vous voulez uniquement la première émission d'un Observable. À partir du moment où le nombre d'émissions utiles est connu, vous utiliserez l'opérateur  `take()`. L'opérateur bas niveau `take()` prendra en paramètre un entier qui sera le nombre d'émissions de l'Observable, ainsi une fois les émissions de `take()` effectuer l'Observable complétera et sera automatiquement détruit.

N'oubliez pas d'importer `take` de ``rxjs/operators`

```typescript
interval(1000).pipe(
    take(3),
    tap(console.log),
).subscribe();
```

Vous aurez ce résultat : 

- https://user.oc-static.com/upload/2021/12/03/16385407012844_Screenshot%202021-12-03%20at%2015.11.20.png

L'autre cas de figure très courant de souscription TypeScript est quand vous voulez recevoir toutes les émissions d'un Observable pendant la durée de vie du component. Du coup, il faut trouver un moyen de compléter l'Observable au moment de la destruction du component. Pour cela, vous allez utiliser le pattern "Destroy Subject".

Angular nous fournit des outils extrêmement pratique à l'instar de la méthode `ngOninit()` nous allons utiliser `ngOnDestroy` afin de réaliser le pattern Destroy Subject.

Vous pourrez l'importer comme `OnInit` et vous pourrez l'implémenter à la classe comme lui aussi.

```typescript
export class FaceSnapListComponent implements OnInit, OnDestroy {
    //...
```

Ensuite vous pourrez utiliser la méthode `ngOnDestroy()` comme ceci : 

```typescript
ngOnDestroy(): void {}
```

Ensuite vous allez créer un type spécial d'Observable : un Subject.

Un Subject est un Observable que vous pouvez faire émettre à la demande. Vous allez donc créer un Subject appelé `destroy$`  qui émettra une seule fois, au moment de la destruction du component.

```typescript
private destroy$!: Subject<boolean>;
```

Il faut ensuite initialiser `destroy$` dans `ngOnInit()` :

```typescript
ngOnInit(): void {
    this.destroy$ = new Subject<boolean>();
    //...
```

La dernière étape de la création de `destroy$` est de le faire émettre dans `ngOnDestroy()`. Pour faire émettre un Subject, on appelle sa méthode `next()` :

```typescript
ngOnDestroy(): void {
    this.destroy$.next(true);
}
```

Avec ça, votre Subject est prêt : vous allez maintenant dire à votre Observable qui fuit de compléter lorsque `destroy$`  émettra – au moment de la destruction du component, donc nous allons utiliser l'opérateur ``takeUntill`, nous allons l'ajouter à notre Observable : 

```typescript
interval(1000).pipe(
    tap(console.log),
    takeUntil(this.destroy$)
).subscribe();
```

N'oubliez pas de l'importer depuis `rxjs/operators`.

Cet opérateur dit à l'Observable  interval  de continuer à émettre tant que `destroy$` n'a pas émis, mais dès que  `destroy$` émet, de compléter l'Observable.

Vous avez vu juste avant comment vous pouvez souscrire à un Observable et afficher ses émissions dans le DOM avec le pipe  `async`.

Tout Observable souscrit avec le pipe `async`  est automatiquement unsubscribe lors de la destruction du component qui le consomme. Vous n'avez donc pas à vous inquiéter des fuites de mémoire avec les Observables souscrits avec le pipe  `async`. La conséquence de ce comportement est que seuls les Observables souscrits avec la méthode `subscribe()`  nécessitent une stratégie spécifique de unsubscribe.

## 2.2 Les Formulaires

### Formulaire basique avec Template Forms

En Angular vous avez deux méthodes pour créer des formulaires, celle dite "template" et celle dite "réactive". Nous allons commencer par les formulaires template, il est moins puissant que le formulaire réactif mais dans certains cas il est suffisant.

Avant toute chose, si ce n'est pas déjà le cas dans votre application, il faut ajouter `FormsModule` (importé depuis `@angular/forms` ) aux `imports`  de votre AppModule : 

```typescript
// ...
imports: [
    BrowserModule,
    AppRoutingModule,
    FormsModule
],
//...
```

Comme il s'agit de la méthode template, commençons par ajouter au template HTML du composant ou nous voulons ajouter un formulaire :

```html
<form>
    <label for="emailInput">Inscrivez-vous pour recevoir notre newsletter !</label>
    <input type="email" id="emailInput">
    <button type="submit">OK!</button>
</form>
```

Pour le moment rien de bien compliqué c'est un formulaire classique. Nous allons préparer le fichier TypeScript du composant en y créant une variable `userEmail` qui contiendra la valeur entrée par l'utilisateur, ainsi qu'une méthode  `onSubmit()` pour l'envoi du formulaire :

```typescript
import { Component, OnInit } from '@angular/core';

@Component({
  selector: 'app-landing-page',
  templateUrl: './landing-page.component.html',
  styleUrls: ['./landing-page.component.scss']
})
export class LandingPageComponent implements OnInit {

  userEmail: string;

  constructor(private router: Router) { }

  ngOnInit(): void {
  }

  onSubmitForm() {
    console.log(this.userEmail);
  }
}
```

Pour l'instant, l'envoi du formulaire entraînera seulement un  `console.log()` de la valeur entrée par l'utilisateur.

Comme vous pouvez le constater, la variable `userEmail` est une `string` normale. Pour la lier à la valeur de la balise  `<input>`, vous allez utiliser une nouvelle directive – `ngModel` :

```html
<input id="emailInput" name="userEmail" type="email" [(ngModel)]="userEmail">
```

Comme vous pouvez le voir sur la directive - `ngModel` nous allons utiliser des `[]` pour l'attribute binding, et vous pouvez voir des `()` pour l'event binding mais là vous avez les deux en même temps, on appelle cela le two-way binding, ou liaison à double sens.

Le two-way binding lie totalement la valeur de la variable à la valeur du `<input>`. Si vous modifiez l'une la modification s'appliquera directement sur l'autre et vice-versa. Par exemple si on attribue une valeur par défaut à notre variable TypeScript : 

```typescript
userEmail = 'me@my-house.com';
```

Nous aurons ce résultat dans le DOM : 

- https://user.oc-static.com/upload/2021/12/10/16391572023293_Screenshot%202021-12-10%20at%2018.26.20.png
- https://user.oc-static.com/upload/2021/12/10/16391580825759_Screenshot%202021-12-10%20at%2018.40.37.png

Pour la liaison dans l'autre sens, il faut lier le bouton du formulaire à la méthode `onSubmit` que nous avons créer. Nous aurions pus utiliser `(click)` mais il existe une autre approche pour les formulaires, dans la balise `<form>`

```html
<form (ngSubmit)="onSubmitForm()">
```

Si votre formulaire commence à acquérir des champs supplémentaires, ça deviendra vite lourd et difficile à maintenir de récupérer systématiquement les valeurs de toutes les variables liées aux champs.

Le système de formulaires template vous permet de passer le formulaire complet en argument comme `NgForm`. Modifiez d'abord l'empreinte de `onSubmitForm()` pour accepter le formulaire comme argument :

```typescript
onSubmitForm(form: NgForm) {
    console.log(form.value);
}
```

Le type `NgForm` expose un attribut `value` qui correspond à un objet contenant les champs du formulaire avec leur attribut `name` et les valeurs contenues dans ces champs.

Pour récupérer le `NgForm` correspondant à votre formulaire, vous allez utiliser une référence locale :

```html
<form #emailForm="ngForm" (ngSubmit)="onSubmitForm(emailForm)">
```

Une référence locale, créée avec un dièse `#` comme ci-dessus, permet à Angular d'accéder à l'élément pour, par exemple, l'envoyer comme argument à une méthode comme vous le faites ici.

On passe bien `ngForm` et non `NgForm` à la référence locale, car ce n'est pas le type `NgForm` qui nous intéresse, mais la directive `ngForm`.

Cette directive est appliquée automatiquement à toutes les balises `form` par Angular, et ici vous créez une référence à la directive pour la passer à la méthode `onSubmitForm()`. C'est cette directive qui vous donne accès à l'attribut `value`, entre autres.

Ainsi maintenant quand vous cliquerez sur le bouton `OK!` c'est l'objet `ngForm` qui sera affiché dans la console du navigateur avec la valeur de `userEmail` :

- https://user.oc-static.com/upload/2021/12/12/16393075659029_Screenshot%202021-12-12%20at%2012.12.24.png

### Les formulaires réctifs avec Reactive Forms

Pour des applications web modernes, vous aurez besoin de formulaires complexes et dynamiques. Angular vous propose les formulaires réactifs.

Là où les formulaires template sont définis par le contenu HTML du template, les formulaires réactifs sont d'abord générés en TypeScript – on vient ensuite relier les différents  input  du template à l'objet du formulaire.

Les formulaires réactifs offrent beaucoup plus de possibilités aux développeurs :

- Comme leur nom l'indique, les formulaires réactifs mettent à disposition des Observables pour réagir en temps réel aux valeurs entrées par l'utilisateur.

- Les formulaires réactifs permettent une validation beaucoup plus approfondie.

- Pour générer des formulaires totalement dynamiques – c'est-à-dire des formulaires dont vous ne connaissez pas la structure en amont – les formulaires réactifs sont la seule solution.

Comme pour les formulaires template, il faut ajouter un import à AppModule. Pour les formulaires réactifs, il faut importer `ReactiveFormsModule` depuis `@angular/forms`:

```typescript
// ...
imports: [
    BrowserModule,
    AppRoutingModule,
    FormsModule,
    ReactiveFormsModule
],
//...
```

Tout d'aboard, vous allez déckarer la variable qui contiendra l'objet du formulaire. Son type est `FormGroup` :

```typescript
import { Component, OnInit } from '@angular/core';
import { FormGroup } from '@angular/forms';

@Component({
  selector: 'app-new-face-snap',
  templateUrl: './new-face-snap.component.html',
  styleUrls: ['./new-face-snap.component.scss']
})
export class NewFaceSnapComponent implements OnInit {

  snapForm!: FormGroup;

  constructor() { }

  ngOnInit(): void {
  }

}
```

Ensuite, vous allez injecter un outil qui simplifie largement la génération des formulaires réactifs, le `FormBuilder` :

```typescript
//...
import { FormBuilder, FormGroup } from '@angular/forms';
//...
constructor(private formBuilder: FormBuilder) { }
//...
```

Puis, dans `ngOnInit()`, vous allez utiliser le `FormBuilder` pour construire votre formulaire :

```typescript
ngOnInit(): void {
    this.snapForm = this.formBuilder.group({
        title: [null],
        description: [null],
        imageUrl: [null],
        location: [null]
    });
}
```

Vous utilisez la méthode `group` du FormBuilder, en lui passant un objet :

- les clés de l'objet correspondent aux noms des champs – ici, j'ai choisi les quatre champs du modèle FaceSnap que l'utilisateur pourra entrer.

- les valeurs de l'objet correspondent à la configuration de chaque champ – pour l'instant, vous passez uniquement `null` pour dire que la valeur par défaut de ces champs est `null`.

Pour tester vous pouvez implémenter une méthode qui va écrire dans la console les résultats du formulaire réactif : 

```typescript
onSubmitForm() {
    console.log(this.snapForm.value);
}
```

Il est temps maintenant de créer le formulaire dans le template et de le brancher à `snapForm`.

Pour cela vous allez créer une `<div>` et appeler à l'intérieur votre formulaire avec ses différentes propriétés.

```html
<div class="form-card">
    <h2>NOUVEAU FACESNAP</h2>
    <form [formGroup]="snapForm">
    
    </form>
</div>
```

Le fait d'avoir importé `ReactiveFormsModule` vous permet de lier un objet de type FormGroup à un `<form>` avec l'attribut  `formGroup`.

Il faut attribuer un `formControlName` à chaque input que vous ajouterez à ce formulaire : ces noms doivent correspondre aux noms des contrôles créés avec FormBuilder :

```html
<form [formGroup]="snapForm">   
    <div class="form-group">
        <label for="title">Titre</label>
        <input id="title" type="text" formControlName="title">
    </div>
    <div class="form-group">
        <label for="description">Description</label>
        <textarea id="description" type="text" formControlName="description" rows="4">
        </textarea>
    </div>
    <div class="form-group">
        <label for="imageUrl">URL de l'image</label>
        <input id="imageUrl" type="text" formControlName="imageUrl">
    </div>
    <div class="form-group">
        <label for="location">Lieu</label>
        <input id="location" type="text" formControlName="location">
    </div>
    <div class="action-buttons">
        <button type="submit" (click)="onSubmitForm()">Enregistrer</button>
    </div>
</form>
```

Ainsi, si vous remplissez le formulaire et cliquez sur Enregistrer : 

- https://user.oc-static.com/upload/2021/12/12/16393160147578_Screenshot%202021-12-12%20at%2014.32.37.png

- https://user.oc-static.com/upload/2021/12/12/1639316113972_Screenshot%202021-12-12%20at%2014.35.01.png

Vous aurez dans la console de votre navigateur le formulaire sous la forme d'un objet. Pour le moment nous avons implémenté quasiment la même chose que tout à l'heure un formulaire classique. Ce qui différencie les Reactives Forms et les Template Forms c'est la méthode `valueChanges` que nous allons pouvoir utiliser avec la méthode `pipe()` de façon à observer notre Reactive Forms et à réagir en fonction. Voici un exemple : 

```typescript
import { Component, OnInit } from '@angular/core';
import { FormBuilder, FormGroup } from '@angular/forms';
import { tap } from 'rxjs';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss']
})
export class AppComponent implements OnInit {
  snapForm!: FormGroup;

  constructor(private formBuilder: FormBuilder) {}
  
  ngOnInit(): void {
    this.snapForm = this.formBuilder.group({
      title: [null],
      description: [null],
      imageUrl: [null],
      location: [null],
    });
    this.snapForm.valueChanges.pipe(
      tap(formValue => console.log(formValue))
    ).subscribe();
  }
  onSubmitForm() {
    console.log(this.snapForm.value);
  }
}
```

Comme vous pouvez le voir la méthode `valueChanges` avec la méthode `pipe` nous permette d'observer le form et ainsi nous imprimerons dans la console chaque changement, dans n'importe quel input de celui-ci.

### Utilisation des Validators

Même si la majeure partie de la validation se passe côté serveur, Angular vous permet d'ajouter une première couche de validation de formulaire côté front-end.

En Angular nous allons utiliser ce qu'on appelle des Validators pour maintenir l'intégrité des données et ainsi être sûr que la donnée qui nous aient transmis par l'utilisateur est bien toujours celle que nous allons attendre.

Ajouter une validation aux formulaires réactifs est plutôt simple : il suffit de les ajouter à la configuration des champs passés à la méthode `group` de FormBuilder.

La première validation que vous allez ajouter est celle qui vérifie que les champs requis contiennent bien des valeurs. Le Validator correspondant est  `Validators.required`, n'oubliez pas d'importer Validator depuis `@angular/forms` :

```typescript
this.snapForm = this.formBuilder.group({
    title: [null, [Validators.required]],
    description: [null, [Validators.required]],
    imageUrl: [null, [Validators.required]],
    location: [null]
});
```

Les Validators sont des fonctions, mais attention à ne pas mettre les parenthèses `()`. Par exemple, ne mettez pas  Validators.required()  , mais bien `Validators.required`. On passe la fonction comme argument – on ne l'appelle pas.


Pour empêcher l'utilisateur d'envoyer le formulaire s'il n'est pas valable, vous pouvez lier l'attribut `disabled` du bouton d'enregistrement à l'attribut `invalid` du FormGroup – si le formulaire n'est pas valable, le bouton sera désactivé.

Dans la template : 

```html
<!-- ... -->
<button type="submit" (click)="onSubmitForm()" [disabled]="snapForm.invalid">Enregistrer</button>
<!-- ... -->
```

Ainsi, si vous n'entrez rien dans les champs requis :

- https://user.oc-static.com/upload/2021/12/12/16393247764285_Screenshot%202021-12-12%20at%2016.59.23.png


Vous allez maintenant ajouter un deuxième Validator au champ `imageUrl` pour vérifier que le texte entré par l'utilisateur correspond à une URL – il s'agit de `Validators.pattern`, qui compare la valeur entrée à une expression régulière (RegExp).

Déclarez une variable qui contiendra le pattern `RegExp` :

```typescript
urlRegex!: RegExp;
```

Et dans `ngOnInit()`, initialisez-la avec le pattern ci-dessous :

```typescript
this.urlRegex = /(http(s)?:\/\/.)?(www\.)?[-a-zA-Z0-9@:%._+~#=]{2,256}\.[a-z]{2,6}\b([-a-zA-Z0-9@:%_+.~#?&/=]*)/;
```

Ici vous ne vérifiez pas que l'URL est valable : simplement que le texte ressemble à une URL.

Il ne reste plus qu'à ajouter un deuxième Validator – le Validator pattern – à la configuration du contrôle `imageUrl` :

```typescript
this.snapForm = this.formBuilder.group({
    title: [null, [Validators.required]],
    description: [null, [Validators.required]],
    imageUrl: [null, [Validators.required, Validators.pattern(this.urlRegex)]],
    location: [null]
});
```

`pattern` est un Validator qui prend un argument, donc on doit lui ajouter les parenthèses, contrairement à `required`.

Si vous testez le formulaire de nouveau, vous verrez que le bouton Enregistrer ne s'active que si le champ URL contient quelque chose qui ressemble à une URL.

Cependant, si vous regardez la console pendant que vous entrez cette URL, vous voyez des erreurs 404 :

- https://user.oc-static.com/upload/2021/12/12/16393273243528_Screenshot%202021-12-12%20at%2017.41.48.png

Ces erreurs apparaissent parce que l'aperçu du FaceSnap sous le formulaire reçoit toutes les valeurs intermédiaires de l'URL, et essaie de les attribuer comme sources d'image. Du coup, tant que l'URL n'est pas complète, vous aurez des erreurs 404 ou, pire, des requêtes vers des ressources non souhaitées !

Pour éviter ces requêtes inutiles, vous pouvez modifier le déclenchement de `valueChanges` du formulaire pour émettre uniquement lorsque l'utilisateur change de champ, c'est-à-dire lors du `blur` des différents champs. Pour ceci, vous allez passer un objet de configuration à la méthode `group` :

```typescript
this.snapForm = this.formBuilder.group({
    title: [null, [Validators.required]],
    description: [null, [Validators.required]],
    imageUrl: [null, [Validators.required, Validators.pattern(this.urlRegex)]],
    location: [null]
}, {
    updateOn: 'blur'
});
```

## 2.3 Les requêtes

### Envoyer des requêtes

Sur le Repository vous trouverez le dossier angular-intermediate-backend c'est avec ça que nous allons apprendre à faire des requêtes en Angular.

Vous pouvez vous rendre dans le dossier faire un `npm install` puis un `npm run start`.

Pour effectuer des requêtes nous allons utiliser le module HttpClient, il va donc falloir l'importer dans le AppModule : 

```typescript
imports: [
    BrowserModule,
    AppRoutingModule,
    FormsModule,
    ReactiveFormsModule,
    HttpClientModule
],
```

HttpClientModule s'importe depuis `@angular/common/http`.

Nous allons injecter le HttpClient dans un de nos services car c'est nos services qui sont à l'origine de la récupération de nos données en base donc il est naturel de venir implémenter les méthodes lier à cette récupération de données dans nos services.

Injectez HttpClient dans UserService en y créant un constructor, comme pour les components : 

```typescript
export class UserService {

  constructor(private http: HttpClient) {}

  // ...
}
```

Comme vous l'avez appris lors du début de la deuxième grande partie de cette documentation, les Observables existent pour faciliter la gestion de l'asynchrone. Les requêtes HTTP étant asynchrones, le HttpClient génère les requêtes sous forme d'Observables.

Les Observables qui correspondent aux requêtes HTTP ont deux comportements possibles :

- Si le serveur répond normalement, l'Observable émet la réponse et complète immédiatement.

- Si le serveur retourne une erreur, l'Observable émet cette erreur (n'oubliez pas qu'un Observable qui émet une erreur est détruit).

Nous pouvons alors implémenter notre méthode récupération de User par exemple dans notre service : 

```typescript
import { HttpClient, Observable } from '@angular/common/http';

@Injectable({
  providedIn: 'root',
})
export class UserService {
  constructor(private http: HttpClient) { }

  getUsers(): Observable<User[]> {
    return this.http.get<User[]>('https://jsonplaceholder.typicode.com/users');
  }
}
```

Vous pouvez ensuite utiliser ce service dans un composant pour récupérer la liste d'utilisateurs et l'afficher dans le composant en utilisant la méthode subscribe de l'objet Observable retourné par le service.

```typescript
import { Component, OnInit } from '@angular/core';
import { UserService } from './user.service';

@Component({
  selector: 'app-user-list',
  templateUrl: './user-list.component.html',
  styleUrls: ['./user-list.component.css']
})
export class UserListComponent implements OnInit {
  users: User[] = [];

  constructor(private userService: UserService) { }

  ngOnInit() {
    this.userService.getUsers().subscribe(users => {
      this.users = users;
    });
  }
}
```

### Sécurisez vos requêtes

Les intercepteurs en Angular sont des outils puissants qui permettent d'intercepter et de manipuler les requêtes HTTP et les réponses HTTP avant qu'elles ne soient envoyées au serveur ou avant que votre application ne traite ces réponses. Ils font partie du module HttpClientModule et offrent une manière flexible de gérer diverses tâches liées aux requêtes HTTP, telles que la modification des en-têtes de requête, la gestion des jetons d'authentification, la mise en cache des réponses, ou encore la gestion globale des erreurs.

Un intercepteur est une classe TypeScript qui implémente l'interface HttpInterceptor et qui comporte le décorateur `@Injectable()`.

Les intercepteurs sont enregistrés différemment des services, donc n'ajoutez surtout pas `{ providedIn: 'root' }`  au décorateur !

Créez un dossier `interceptors`  dans le dossier `app`, et créez-y un fichier `auth.interceptor.ts` :

```typescript
import { HttpInterceptor } from '@angular/common/http';
import { Injectable } from '@angular/core';

@Injectable()
export class AuthInterceptor implements HttpInterceptor {

}
```

Pour implémenter l'interface HttpInterceptor vous allez avoir besoin de la méthode `intercept()` avec l'empreinte suivante : 

```typescript
import { HttpEvent, HttpHandler, HttpInterceptor, HttpRequest } from '@angular/common/http';
import { Injectable } from '@angular/core';
import { Observable } from 'rxjs';

@Injectable()
export class AuthInterceptor implements HttpInterceptor {
  intercept(req: HttpRequest<any>, next: HttpHandler): Observable<HttpEvent<any>> {
    
  }
}
```

La méthode  `intercept()` sera appelée pour chaque requête et recevra cette requête comme argument, en plus d'un objet appelé `next` que vous découvrirez dans un instant.

Avant d'implémenter cette méthode, préparez le service qui renverra le token. Dans le dossier `services`, créez un service `auth.service.ts` qui contient un  `token` privé sous forme de `string`, et une méthode `getToken()` qui la renvoie :

```typescript
import { Injectable } from '@angular/core';

@Injectable({
  providedIn: 'root'
})
export class AuthService {
  private token = 'MyFakeToken';
  
  getToken(): string {
    return this.token;
  }
}
```

Nous allons mettre en place un faux Token pour tester.

De retour dans votre intercepteur, injectez le service que vous venez de créer, et implémentez la méthode `intercept`  comme suit :

```typescript
import { HttpEvent, HttpHandler, HttpHeaders, HttpInterceptor, HttpRequest } from '@angular/common/http';
import { Injectable } from '@angular/core';
import { Observable } from 'rxjs';
import { AuthService } from '../services/auth.service';

@Injectable()
export class AuthInterceptor implements HttpInterceptor {

  constructor(private authService: AuthService) {}

  intercept(req: HttpRequest<any>, next: HttpHandler): Observable<HttpEvent<any>> {
    const headers = new HttpHeaders()
      .append('Authorization', `Bearer ${this.authService.getToken()}`);
    const modifiedReq = req.clone({ headers });
    return next.handle(modifiedReq);
  }
}
```

Dans la méthode :

- Vous créez des `headers` utilisables par Angular avec `new HttpHeaders()` et vous utilisez leur méthode `append()` pour y ajouter un header `Authorization` qui contient `Bearer TOKEN` – c'est souvent la forme requise pour ce type de header.

- Vous créez une nouvelle requête en clonant la précédente et en y ajoutant les `headers` que vous venez de créer – les requêtes sont des objets immuables (qu'on ne peut pas modifier), donc on créera toujours une nouvelle requête qui contient les modifications requises.

- Vous retournez `next.handle()` en y passant la nouvelle requête – c'est ce qui permet à la requête de continuer son chemin.

Votre intercepteur est prêt : il faut maintenant l'enregistrer auprès d'Angular pour qu'il soit appelé pour chaque requête.

Puisqu'une application comporte généralement plusieurs intercepteurs, pour éviter de trop polluer AppModule on commence généralement par créer un fichier d'index qui prépare l'enregistrement de tous les intercepteurs au même endroit.

Dans le dossier `interceptors`, créez un fichier `index.ts` :

```typescript
import { HTTP_INTERCEPTORS } from '@angular/common/http';
import { AuthInterceptor } from './auth.interceptor';

export const httpInterceptorProviders = [
  { provide: HTTP_INTERCEPTORS, useClass: AuthInterceptor, multi: true }
];
```

L'utilisation de `HTTP_INTERCEPTORS` dit à Angular qu'il s'agit ici d'un intercepteur HTTP. Vous y attribuez la classe AuthInterceptor que vous venez de créer. La clé `multi` prévient que vous allez certainement ajouter plusieurs intercepteurs à la clé `HTTP_INTERCEPTORS`.

Il ne reste plus qu'à ajouter cette constante aux  providers  de l'application. Dans AppModule :

```typescript
// ...
import { httpInterceptorProviders } from './interceptors';
// ...
    providers: [
        { provide: LOCALE_ID, useValue: 'fr-FR' },
        httpInterceptorProviders
    ],
// ...
```

Un provider est un objet que l'on déclare à Angular pour qu'il puisse l'injecter à différentes endroits de l'application.

D'ailleurs, même si vos services ne figurent pas ici, ce sont des providers également ! Ils sont déclarés avec `@Injectable()`et Angular peut ensuite les injecter là où vous en avez besoin, comme via le constructor de vos components, par exemple.

Et voilà, c'est terminé ! Pour vérifier que tout fonctionne, ouvrez l'onglet Network (Réseau) des outils de développeur de votre navigateur, cliquez sur la requête, et dans les Request Headers sous l'onglet Headers vous trouverez :

- https://user.oc-static.com/upload/2021/12/14/16395003685864_Screenshot%202021-12-14%20at%2017.45.36.png

## 2.4 Modulariser son application

### Organiser son code par module

Pour comprendre comment bien organiser son code par module vous pouvez aller suivre ce chapitre dans ce cours : 

- https://openclassrooms.com/fr/courses/7471271-completez-vos-connaissances-sur-angular/7549551-facilitez-la-maintenance-avec-les-modules

### Comprendre et utiliser le Lazy Loading

Il existe un concept appeler le Lazy Loading en Angular avec les modules, il est assez important afin de gagner en performance dans vos applications Angular. Vous pouvez aller suivre ce chapitre dans ce cours :

- https://openclassrooms.com/fr/courses/7471271-completez-vos-connaissances-sur-angular/7549556-boostez-la-performance-avec-le-lazy-loading

### Contrôlez les accès avec les guards

Un Guard sur Angular est une fonctionnalité qui vous permet de contrôler l'accès à des routes spécifiques dans votre application. Vous pouvez utiliser des guards pour exécuter certaines vérifications ou actions avant de permettre l'accès à une route, par exemple pour vérifier si l'utilisateur est authentifié ou a les droits d'accès appropriés.

Voici un exemple de service d'authentification que vous pouvez utiliser avec le guard ci-dessus :

```typescript
import { Injectable } from '@angular/core';

@Injectable({
  providedIn: 'root'
})
export class AuthService {
  private isAuthenticated = false;

  login() {
    this.isAuthenticated = true;
  }

  logout() {
    this.isAuthenticated = false;
  }

  isAuthenticated(): boolean {
    return this.isAuthenticated;
  }
}
```

Ce service contient une méthode `login` qui définit la variable `isAuthenticated` sur `true`, une méthode logout qui définit la variable `isAuthenticated` sur `false`, et une méthode `isAuthenticated` qui retourne la valeur de la variable `isAuthenticated`. Vous pouvez utiliser ces méthodes pour gérer l'authentification de l'utilisateur et pour contrôler l'accès à certaines routes avec le guard `AuthGuard`.

Voici un exemple de guard qui vérifie si l'utilisateur est connecté à l'application avant de lui permettre l'accès à une route :

```typescript
import { inject } from "@angular/core";
import { Router } from "@angular/router";
import { AuthService } from "./auth.service";

export const AuthGuard = () => {
    const auth = inject(AuthService);
    const router = inject(Router);

    if(!auth.isAuthenticated()) {
        router.navigateByUrl('/login')
        return false
    }
    return true
}
```

Cet exemple nous permet aussi d'introduire la fonction inject d'Angular permet l'injection de dépendances hors des classes, utile pour des cas spécifiques comme les gardes d'authentification ou les intercepteurs HTTP. Elle complète le système d'injection classique (@Injectable et constructeurs) sans le remplacer, offrant une flexibilité pour des scénarios où l'injection via classes n'est pas idéale.

Dans ce cas, le code crée un "AuthGuard" qui vérifie si un utilisateur est authentifié avant de lui permettre d'accéder à une route protégée.

- On crée la fonction `AuthGuard` qui sera utilisée comme guard. Dans cette fonction, on injecte les dépendances pour `AuthService` et `Router`.

- On vérifie si l'utilisateur est authentifié en utilisant la méthode `isAuthenticated()` de l'instance `auth`. Cette méthode doit être implémentée dans le service d'authentification (`AuthService`) pour déterminer si un utilisateur est authentifié ou non.

- Si l'utilisateur n'est pas authentifié (c'est-à-dire si `auth.isAuthenticated()` renvoie `false`), on redirige l'utilisateur vers la page de connexion en utilisant la méthode `navigateByUrl('/login')` de l'instance `router`. Ensuite, on retourne `false` pour indiquer que l'accès à la route protégée n'est pas autorisé.

- Si l'utilisateur est authentifié, on retourne simplement `true`, ce qui permet l'accès à la route protégée.

Ensuite on doit l'appliquer au routeur : 

```typescript
const routes: Routes = [
  {
    path: 'admin',
    component: AdminComponent,
    canActivate: [AuthGuard], // Utilisation du guard
  }
];
```

# 3. Deuxième grande partie
