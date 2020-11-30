# Design Patterns

#### Sources :

- [Refactoring : Design Patterns](https://refactoring.guru/design-patterns)
- [Sourcemaking : Design Pattern](https://sourcemaking.com/design_patterns)
- [Wikipédia : Software design pattern](https://en.wikipedia.org/wiki/Software_design_pattern)
- [Wikipédia : Patron de conception](https://fr.wikipedia.org/wiki/Patron_de_conception)
- [PDF : Design pattern](doc/DP.pdf)

#### Exemples de patterns :

- [Refactoring : Design patterns GoF en PHP](https://refactoring.guru/design-patterns/php)

## Introduction

En développement Web, un design pattern est une solution répétable à un problème commun lors de la création d’une application. Un design pattern ( patron de conception , en français) n’est pas un modèle fini pouvant directement être transformé en code. C’est une description ou un guide pour aider à résoudre un problème et pouvant être utilisé dans plusieurs situations

Souvent, les gens comprennent seulement comment appliquer certains schéma techniques à certains problèmes. Ces terchniques sont difficiles à appliquer et c'est ainsi qu'intervient les design patterns qui eux fournissent des solutions plus généralisés, documentés et dans un format qui ne demande pas de lien particulier à un problème.


### Qu'est-ce que c'est 

- C’est une technique d’architecture logicielle
- Description d'une solution classique à un problème récurrent

### Ce que ce n'est pas

- Une brique : Un pattern dépend de son environnement
- Une règle : Un pattern ne peut pas s'appliquer mécaniquement
- Une méthode : Ne guide pas une prise de décision; un pattern est la décision prise
- Nouveau : Lao-Tzu (-550) travaillait déjà sur les patterns...

### Avantges 

- Un vocabulaire commun
- un niveau d'abstraction plus élevé qui permet d'élaborer des constructions logicielles de meilleure qualité
- Réduire la complecité

### Inconvénients

- Effort de synthèse; reconnaître, abstraire...
- Apprentissage: un certain temps d'adaptation est souvent nécéssaire
- Nombreux : De niveaux différents, certains patterns s'appuient sur d'autres


# Gang of Four

**1994** : Design Patterns : Elements of Reusable Object-Oriented Software.
- Les modèles de design ont gagné en popularité en informatique après le livre **Design Patterns**

## Introduits par le Gang of Four (GoF), 3 grandes familles de design patterns voient le jour 

Souvent, la référence **Design Patterns** décrit les formes par des diagrammes OMT ([Object Modeling technique](https://fr.wikipedia.org/wiki/Object_modeling_technique)), auxquels on y retrouve 3 grandes familles... Tous plutôt orienté-objet, mais pas exclusivement, l'héritage et les objets n'étant pas nécessaires.

- **Creational design patterns (Créateurs)**
- **Structural design patterns (Structuraux)**
- **Behavioral design patterns (Comportementaux)**


### [Creational design patterns](https://sourcemaking.com/design_patterns/creational_patterns) (Voir PDF page 8)

Ils définissent comment faire l'instanciation et la configuration des classes et des objets.

En développement Web, cette famille de pattern est là pour gérer le mécanisme de création d'objets d'une façon adaptée à la situation. 
La forme basique de création d'objets pouvant causer certains problèmes ou de compléxifier le modèle, les design patterns de la famille **Creational** vont quant à eux chercher à résourdre ce problème en controllant la création de l'objet.

- [Abstract Factory](https://refactoring.guru/fr/design-patterns/abstract-factory) : Permet de créer des familles d’objets apparentés sans préciser leur classe concrète
- [Builder](https://refactoring.guru/fr/design-patterns/builder) : Permet de construire des objets complexes étape par étape. Ce patron permet de construire différentes variations ou représentations d’un objet en utilisant le même code de construction.
- [Factory Method](https://refactoring.guru/fr/design-patterns/factory-method) : Définit une interface pour la création d’objets dans une classe mère, mais délègue aux sous-classes le choix des types d’objets à créer.
- [Prototype](https://refactoring.guru/fr/design-patterns/prototype) : Permet de créer de nouveaux objets à partir d’objets existants sans rendre le code dépendant de leur classe.
- [Singleton](https://refactoring.guru/fr/design-patterns/singleton) : Permet de garantir que l’instance d’une classe n’existe qu’en un seul exemplaire, tout en fournissant un point d’accès global à cette instance.
- [Object Pool](https://sourcemaking.com/design_patterns/object_pool)

#### Exemple : 
Abstract Factory
![Abstract-Factory](https://refactoring.guru/images/patterns/diagrams/abstract-factory/solution2.png)

### [Structural design patterns](https://sourcemaking.com/design_patterns/structural_patterns) (Voir PDF page 14)

Ils définissent comment organiser les classes d'un programme dans une structure plus large (séparant l'interface de l'implémentation).

En développement Web, cette famille de pattern a pour vocation d'identifier simplement la relation entre les entitié.

- [Adapter](https://refactoring.guru/fr/design-patterns/adapter) : Il est utilisé dans le cas où un programme se sert d'une bibliothèque de classe qui ne correspond plus à l'utilisation qui en est faite, à la suite d'une mise à jour de la bibliothèque dont l'interface a changé.
- [Bridge](https://refactoring.guru/fr/design-patterns/bridge) : Permet de séparer une grosse classe ou un ensemble de classes connexes en deux hiérarchies — abstraction et implémentation — qui peuvent évoluer indépendamment l’une de l’autre.
- [Composite](https://refactoring.guru/fr/design-patterns/composite) : Permet d'agencer les objets dans des arborescences afin de pouvoir traiter celles-ci comme des objets individuels.
- [Decorator](https://refactoring.guru/fr/design-patterns/decorator) : Permet d’affecter dynamiquement de nouveaux comportements à des objets en les plaçant dans des emballeurs qui implémentent ces comportements.
- [Facade](https://refactoring.guru/fr/design-patterns/facade) : Procure une interface qui offre un accès simplifié à une librairie, un framework ou à n’importe quel ensemble complexe de classes.
- [Flyweight](https://refactoring.guru/fr/design-patterns/flyweight) : Permet de stocker plus d’objets dans la RAM en partageant les états similaires entre de multiples objets, plutôt que de stocker les données dans chaque objet.
- [Proxy](https://refactoring.guru/fr/design-patterns/proxy) : Permet de fournir un substitut d’un objet. Une procuration (Proxy) donne le contrôle sur l’objet original, vous permettant d’effectuer des manipulations avant ou après que la demande ne lui parvienne.
- [Private Class Data](https://sourcemaking.com/design_patterns/private_class_data)

#### Exemple : 
![Proxy](https://sourcemaking.com/files/v2/content/patterns/Proxy_example1.png)

### [Behavioral design patterns](https://sourcemaking.com/design_patterns/behavioral_patterns) (Voir PDF page 23)

Ils définissent comment organiser les objets pour que ceux-ci collaborent (distribution des responsabilités) et expliquent le fonctionnement des algorithmes impliqués.

En développement Web, cette famille de pattern est là afin d'identifier certain modèles de communication de base entre les objets. Ce faisant, les design patterns de cathégories **Behavioral**, augmentent ainsi la flexibilité dans la gestion de la communication

- [Chain of responsibility](https://refactoring.guru/fr/design-patterns/chain-of-responsibility) : Permet de faire circuler une demande dans une chaîne de handlers. Lorsqu'un handler reçoit une demande, il décide de la traiter ou de l’envoyer au handler suivant de la chaîne.
- [Command](https://refactoring.guru/fr/design-patterns/command) : Prend une action à effectuer et la transforme en un objet autonome qui contient tous les détails de cette action. Cette transformation permet de paramétrer des méthodes avec différentes actions, planifier leur exécution, les mettre dans une file d’attente ou d’annuler des opérations effectuées.
- [Iterator](https://refactoring.guru/fr/design-patterns/iterator) : Permet de parcourir les éléments d’une collection sans révéler sa représentation interne (liste, pile, arbre, etc.).
- [Mediator](https://refactoring.guru/fr/design-patterns/mediator) : Permet de diminuer les dépendances chaotiques entre les objets. Ce patron restreint les communications directes entre les objets et les force à collaborer uniquement via un objet médiateur.
- [Memento](https://refactoring.guru/fr/design-patterns/memento) : Permet de sauvegarder et de rétablir l'état précédent d’un objet sans révéler les détails de son implémentation.
- [Observer](https://refactoring.guru/fr/design-patterns/observer) : Permet de mettre en place un mécanisme de souscription pour envoyer des notifications à plusieurs objets, au sujet d’événements concernant les objets qu’ils observent.
- [State](https://refactoring.guru/fr/design-patterns/state) : Modifie le comportement d’un objet lorsque son état interne change. L’objet donne l’impression qu’il change de classe.
- [Strategy](https://refactoring.guru/fr/design-patterns/strategy) : Permet de définir une famille d’algorithmes, de les mettre dans des classes séparées et de rendre leurs objets interchangeables.
- [Template method](https://refactoring.guru/fr/design-patterns/template-method) : Permet de mettre le squelette d’un algorithme dans la classe mère, mais laisse les sous-classes redéfinir certaines étapes de l’algorithme sans changer sa structure.
- [Visitor](https://refactoring.guru/fr/design-patterns/visitor) : Permet de séparer les algorithmes et les objets sur lesquels ils opèrent.
- [Interpreter](https://sourcemaking.com/design_patterns/interpreter)
- [Null Object](https://sourcemaking.com/design_patterns/null_object)

#### Exemple :
![Interpreter](https://sourcemaking.com/files/v2/content/patterns/Interpreter1.png)


# Les modèles MVC, MVP, MVVM

MVC, **Model, View, Controller** (Modèle, Vue, Controller, en français), n'est pas un design pattern définie par le **GoF** (Gang of Four). Il s'agit plutôt d'un modèle architectural de plus haut niveau qui englobe plusieurs modèles de conception définis par le GoF. Au minimum, le modèle MVC utilise le modèle Observer qui est un modèle comportemental (**Behavioral**). Il existe d'autres modèles de conception utilisés par MVC. Parfois, les modèles qu'il utilise peuvent également dépendre d'une implémentation particulière dans un projet.

MVP, **Model, View, Presenter** (Modèle, Vue, Présentateur, en français), similaire au MVC traditionnel mais Controller est remplacé par Presenter. Mais le Presenter, contrairement au Controller, est également responsable de la modification de la vue. La vue n'appelle généralement pas le Presenter.

MVVM, **Model, View, View, Model** (Modèle, Vue, Vue, Modèle, en français), la différence ici est la présence de View Model. C'est une sorte d'implémentation d'Observer Design Pattern, où les modifications du modèle sont également représentées dans la vue par la VM. Par exemple: si un curseur est modifié, non seulement le modèle est mis à jour, mais les données qui peuvent être un texte affiché dans la vue sont également mises à jour. Il existe donc une liaison de données bidirectionnelle.

Donc, pour résumer, le MVC comme pour les autres, utilisent plusieurs modèles de conception définis par Gang of Four pour réaliser leur missions. Et sont donc considérés comme des collections de modèle de conception.

Cependant, le MVC est aujourd'hui le pattern design le plus couramment utilisé pour créer des interfaces utilisateur.


#### Exemple :
![mvc-mvp-mvvm](https://i.stack.imgur.com/Y82D3.png)


# [L'Anti-Pattern](https://medium.com/@armandfardeau/quest-ce-qu-un-design-pattern-cac63a3fa642)

**1995** : AntiPatterns : Refactoring Software, Architectures, and Projects in Crisis.
- Référer de manière informelle à toute solution couramment réinventée mais mauvaise à un problème.

Un anti-modèle (anti pattern) est une réponse commune à un problème récurrent qui est généralement inefficace et risque d’être très contre-productif. Identifiable selon 2 critères :
- Un processus, une structure ou un modèle d’action couramment utilisé
- Une autre solution dont l'éfficacité est démontré existe



# Conclusion

Il n’existe pas à proprement parlé de liste exhaustive des design patterns, car des modèles de design utiles sont découverts tout le temps. Néanmoins, **3 grandes familles de design pattern** ont été introduit en 1994 par le Gang of Four incluant **23 pattrons de concéption différents** qui ont été repris et influencé pas mal d'autres design patterns, dont le plus connus à ce jour, le modèle **MVC**.

1 an plus tard (1995), face à l'afflut de design patterns de mauvaise qualité, Andrew Koenig publie le livre AntiPatterns qui permettra par la suite de réguler plus efficacement la qualité des designs pattern dans l'ensemble.