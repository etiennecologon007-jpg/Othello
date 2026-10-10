# Othello

Projet Java d'un jeu de Othello sur plateau hexagonal, avec interface en ligne de commande et intelligence artificielle.

## Présentation

Ce repository contient deux modules Maven :

- `HexagonalCoordinates` : gestion des coordonnées hexagonales et utilitaires de grille.
- `OthelloEngine` : moteur du jeu, règles, IA, interface utilisateur et tests.

Le jeu supporte :

- 1 joueur contre 1 joueur (PvP)
- 1 joueur contre l'IA
- phase de placement initiale aléatoire ou choisie
- déplacements sur un plateau hexagonal
- validation des lignes formées et sacrifice d'anneau
- affichage console coloré du plateau

## Structure du projet

```text
Othello/
├── README.md
├── HexagonalCoordinates/
│   ├── pom.xml
│   └── src/
│       ├── main/java/org/Coordinate/
│       └── test/java/org/Coordinate/
├── OthelloEngine/
│   ├── pom.xml
│   └── src/
│       ├── main/java/fr/unicaen/info/othello/
│       └── test/java/fr/unicaen/info/othello/
└──
```

## Prérequis

- Java 21
- Maven 3.9+

## Installation

1. Installer la dépendance `HexagonalCoordinates` dans le dépôt local Maven :

```bash
cd HexagonalCoordinates
mvn install
```

2. Lancer le moteur du jeu :

```bash
cd ../OthelloEngine
mvn javafx:run
```

## Tests

Pour exécuter les tests de chaque module :

```bash
cd HexagonalCoordinates
mvn test

cd ../OthelloEngine
mvn test
```

## Règles du jeu

Le projet implémente une variante du jeu d'Othello sur grille hexagonale. Les joueurs placent puis déplacent des anneaux selon les règles du moteur de jeu, avec gestion des lignes et du sacrifice d'un anneau lorsqu'une ligne est complétée.

## Points d'entrée

Le point d'entrée principal du jeu est :

```text
fr.unicaen.info.othello.ui.CUIMain
```

Il propose au lancement le choix :

- jouer contre l'IA
- jouer en mode PvP
- choisir un départ aléatoire ou non

## Dépendances principales

- JavaFX
- JUnit 5
- Maven

## Auteurs

Projet développé dans le cadre d'un travail sur les structures de coordonnées hexagonales et l'implémentation d'un moteur de jeu de plateau.

## Licence

Aucune licence n'est spécifiée dans le dépôt pour le moment.
