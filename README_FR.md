# Pokemon Project

Le projet **Pokemon** est une application Java qui simule un jeu Pokémon au tour par tour. Ce projet a été conçu dans le cadre d'un projet universitaire avec des exigences spécifiques en termes de gameplay, de conception logicielle et de fonctionnalités.

## 🎯 Objectifs du Projet
- Créer un jeu Pokémon en Java où deux joueurs s'affrontent, un humain et une IA.
- Implémenter des mécanismes de pioche, de défausse, d'attaques et de gestion de terrain.
- Ajouter une dimension stratégique avec des **affinités élémentaires** et des **pouvoirs spéciaux** pour certains Pokémons.
- Realiser le jeu en mode console.

---

## 🚀 Fonctionnalités Implémentées

### Mécanismes de Base
- **Gestion des Pokémons :** Chaque Pokémon possède un **nom**, des **points de vie**, une **force d'attaque**, et une **affinité élémentaire**.
- **Éléments et Affinités :**
  - Terre > Eau > Feu > Air > Terre.
  - Un avantage d'affinité augmente une attaque de 10 points, un désavantage la diminue de 10 points.
- **Attaques et Défausse :** Les Pokémons attaquent leurs adversaires, infligeant des dégâts basés sur leur force et les affinités. Les Pokémons ayant 0 points de vie sont envoyés dans la défausse.

### Gameplay
- **Tour par tour :** Le joueur humain et l'ordinateur alternent leurs actions :
  1. Pioche de Pokémons.
  2. Placement sur le terrain.
  3. Exécution des attaques.
- **Stratégie IA :** L’ordinateur évalue les affinités élémentaires et les points de vie pour déterminer la cible optimale de ses attaques.

### Interface Utilisateur
- **Affichage textuel :** Visualisation claire des Pokémons en jeu, des Pokémons en main, et des actions disponibles.
- **Retour utilisateur :** Actions de l'IA visibles pour le joueur, avec un suivi des tours.

### Pouvoirs Spéciaux
- Implémentation de **8 pouvoirs uniques** pour certains Pokémons, tels que :
  - **Résistance**, à utilisation unique : le Pokémon choisit un Pokémon de son camp (éventuellement lui-même). Jusqu'à la fin de la partie ou à la mort du Pokémon choisi, à chaque attaque reçue celui-ci subit subit 10 points de dégâts de moins.
  - **Ferveur guerrière**, à utilisation unique : le Pokémon choisit un Pokémon de son camp (éventuellement lui-même). Jusqu'à la fin de la partie ou à la mort du Pokémon choisi, les attaques de celui-ci infligent 10 points de dégâts de plus.
  - **Peur**, à utilisation unique : le Pokémon choisit un Pokémon du camp adverse. Jusqu'à la fin de la partie ou à la mort du Pokémon choisi, les attaques de celui-ci infligent 10 points de dégats de moins.
  - **Berserk**, à utilisation unique : le Pokémon choisit un Pokémon de son camp (éventuellement lui-même). Pour le tour en cours, l'attaque de ce Pokémon est doublée.
  - **Intimidation**, à utilisation unique : le Pokémon choisit un Pokémon du camp adverse. Pour le prochain tour de l'adversaire, les dégats infligés par le Pokémon choisi sont réduits de moitié.
  - **Soin total**, à utilisation unique : le Pokémon choisit un Pokémon de son camp (éventuellement lui-même). Celui-ci regagne toute sa vie.
  - **Soin simple**, utilisable à chaque tour : le Pokémon choisit un Pokémon de son camp (éventuellement lui-même). Celui-ci regagne 30 points de vie (mais ne peut pas dépasser son nombre de points de vie initial).
  - **Kamikaze**, à utilisation unique : le Pokémon choisit un Pokémon du camp adverse. Les deux Pokémons sont alors éliminés.

### Génération Aléatoire des Pokémons
- Points de vie : Multiples de 10, entre 100 et 200.
- Attaque : Multiples de 10, entre 10 et 40.
- Affinité : Choix aléatoire parmi les 4 éléments.
- Noms : Générés aléatoirement à partir d'une liste prédéfinie.

---

## 🛠️ Structure Technique

- **Langage :** Java
- **Architecture :** 
  - Classes pour représenter les **Pokémons**, le **jeu**, et les actions des joueurs.
  - Séparation des responsabilités pour une conception modulaire et extensible.
- **Tests :** Suite de tests unitaires pour valider les mécaniques de base et les pouvoirs.

---

## 🏆 Résultat Final

Le jeu se termine lorsque tous les Pokémons d'un joueur sont éliminés.

## 📚 Ressources et Références

Une documentation JavaDoc ainsi qu’un diagramme UML sont disponibles pour plus de détails. Vous pouvez les retrouver dans les répertoires `uml` et `JavaDoc` du projet.  
Vous pouvez exécuter le programme depuis n’importe quel IDE, personnellement, j’utilise IntelliJ IDEA.
Il est également possible de compiler le programme vous-même et de l’exécuter directement depuis une ligne de commande.

<div align="center">
  <img src="./ReadMeImages/start.png" alt="EStart image" width="90%" style="border: 1px solid #ccc; border-radius: 8px; box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);">
  <img src="./ReadMeImages/game.png" alt="Game Image" width="90%" style="border: 1px solid #ccc; border-radius: 8px; box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);">
</div>