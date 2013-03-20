# Notes

## Plan

* Le context
* Le projet
* Les début, l'euphorie
* La maintenance, la désillusion
* Le projet grossi, la frayeur
* Le projet vis, la réconciliation
* Conclusion

## En vrac

* Est-ce qu'on parle de la configuration ?
* Composer ?

## Présentation

### Le contexte

* Startup, beaucoup de choses à construire
* Projet de zéro
* Equipe d'expert, avec une expérience significative en Symfony 1/2
* Le sentiment d'être plus souvent contraint qu'aidé par le framework

### Les projets

* 2 projets, bien distincts
* "Warehouse"
  * Entrepôt de livres numériques
  * Uniquement des API
  * Pas de vues
  * Pas de gestion d'utilisateurs complexe
* "Backend"
  * Ecrans d'administration
  * Ecran de reporting de données
  * Notion de profils utilisateur
  * Ecrans adaptés en fonction du profil
  * Accès aux API d'autres appications

### Les débuts, l'euphorie

* Feuille blanche, on peut faire ce qu'on veut
* On récupère les bonnées idées, on adapte celles qui nous gènes
  * Arborescence
  * Utilisation d'un ORM
  * Twig

### La maintenance, la désillusion

Puis, un jour, il faut maintenir le projet.
Le backend évolue, il faut rajouter des écrans, retravailler des données

* ORM
  * "Mais pourquoi est-ce qu'on a gardé ça ?"
  * Tout ce qu'on voulait éviter, les contraintes sans la souplesse
* Sécurisation
  * Chaque controlleur fait sa propre vérification
  * Duplication de code, difficulté de maintenance, d'évolution

### Entamons un refactoring

* Retrait de la couche ORM pour ne garder que la couche DBAL

### Le projet vis, la réconciliation

* Une fois ces erreurs apprises, le projet reprend vie

### Conclusion

* Au début, j'ai présenté 2 projets, mais par la suite, je ne parle plus que d'un seul
  * Le warehouse est loin d'un projet web "standard", il n'utilise pas les outils habituels
  * Le backend est un projet plus standard : vue, gestion des utilisateurs, ...
* Après un an, si j'avais à refaire le choix de l'outil a utiliser
  * Pour le backend, je ne reprendrais pas Silex, mais Symfony, car je n'ai fait que réinventer la roue
  * Pour le warehouse, je reprendrais Silex. J'aurais perdu trop de temps à détourner Symfony de son but originel 
* Quitte à enfoncer des portes ouvertes
  * A partir du moment où on passe du temps à réinstaller les composants de Sf2, il faut se poser la question du choix de Silex
  * Se poser la question au moment du démarrage du projet des composants qu'il va falloir embarquer
  * Est-ce un projet "standard" ? Si oui => Symfony2
* Pourquoi réinventer la roue
  * Trouver des exemples de Provider qui ne font que réinventer Symfony2
