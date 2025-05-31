# Compte Rendu - Implémentation de l'Injection de Dépendances

## Introduction

Dans le domaine de l'informatique, il est fondamental de concevoir des applications évolutives, maintenables, extensibles, et capables de s'adapter aux changements. Pour atteindre ces objectifs, plusieurs principes sont essentiels :

- Injection de dépendances
- Inversion de contrôle
- Faible couplage

## Énoncé

Ce travail pratique a pour objectif de mettre en œuvre le concept d'injection de dépendances, à la fois de manière statique et dynamique. La version dynamique s'appuie sur le framework Spring, en utilisant les annotations ainsi qu'un fichier de configuration XML.

## Structure et Implémentation

### Architecture du projet
*L'architecture du projet est organisée avec plusieurs packages incluant les interfaces, leurs implémentations, et différentes méthodes d'injection de dépendances.*

### Interface IDao et sa méthode getData
*Une interface IDao est définie, contenant une méthode getData() qui retourne une valeur numérique. Cette interface représente la couche d'accès aux données.*

### Interface métier
*Une interface IMetier est définie, déclarant une méthode calcul() qui effectuera un traitement métier.*

### Implémentation de l'interface IMetier
*La classe MetierImpl implémente l'interface IMetier. Elle contient une dépendance vers l'interface IDao et implémente la méthode calcul() qui utilise la valeur retournée par getData() pour effectuer un calcul métier.*

### Injection de dépendances de manière statique
*Démonstration de l'injection statique où les objets sont instanciés directement dans le code, créant un couplage fort entre les classes.*

### Injection de dépendances de manière dynamique
*Implémentation d'injection dynamique utilisant la réflexion Java pour instancier les classes depuis leurs noms qualifiés dans un fichier de configuration, réduisant ainsi le couplage.*

### Configuration Spring via un fichier XML
*Utilisation de Spring Framework avec un fichier de configuration XML définissant les beans et leurs dépendances, permettant une injection plus flexible et déclarative.*

### Configuration Spring via annotations
*Configuration de l'injection de dépendances avec Spring en utilisant des annotations comme @Component, @Service, @Repository et @Autowired pour définir et injecter les dépendances.*

## Conclusion

Ce projet démontre les différentes approches d'injection de dépendances, progressant des méthodes statiques fortement couplées vers des méthodes dynamiques et déclaratives qui favorisent un meilleur découplage et une maintenance plus aisée. L'utilisation du framework Spring simplifie considérablement la mise en œuvre de ces principes et offre une grande flexibilité dans la configuration des dépendances.
