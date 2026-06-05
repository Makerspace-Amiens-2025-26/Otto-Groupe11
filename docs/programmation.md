---
layout: default
nav_order: 3
title: Programmation
---

# 💻 Programmation

## Contexte du programme

Pour la partie Arduino, notre objectif principal était de rendre le robot le plus rapide et le plus efficace possible afin de maximiser ses performances lors des différentes épreuves des Ottolympiades.

Pour démarrer, nous avons trouvé une esquisse de programme sur GitHub que nous avons ensuite adaptée et modifiée afin qu'elle corresponde à notre robot et à nos besoins.

Le déplacement de notre Otto-BDS repose principalement sur une rotation synchronisée des jambes et des pieds. Cette technique donne l'impression que le robot glisse sur le sol plutôt qu'il ne marche réellement.

Cependant, nous avons rencontré plusieurs difficultés lors du développement. Le principal problème concernait la trajectoire du robot : malgré l'ajout d'offsets pour corriger les servomoteurs, Otto-BDS avait tendance à dévier lorsqu'il avançait.

Après de nombreux essais, nous avons constaté que certains servomoteurs n'avaient pas exactement le même comportement, ce qui rendait difficile l'obtention d'une trajectoire parfaitement droite.

> 💡 Si votre robot rencontre le même problème, n'hésitez pas à remplacer les servomoteurs concernés ou à développer une fonction de correction de trajectoire plus avancée.

---

# 🚀 Optimisation avant les Ottolympiades

Au cours de la compétition, nous nous sommes rapidement rendu compte que notre robot n'était pas suffisamment rapide pour conserver sa place dans le classement du Chrono Challenge.

Nous avons donc modifié plusieurs paramètres du programme afin d'augmenter la vitesse des déplacements tout en conservant une bonne stabilité.

Ces modifications ont porté leurs fruits puisque notre temps est passé d'environ **30 secondes à seulement 17,9 secondes**, ce qui nous a permis d'obtenir la **deuxième place** dans cette épreuve.

Cette optimisation a également eu un impact positif sur la course d'obstacles, où Otto-BDS a finalement remporté la première place avec un temps record de **15 secondes**.

---

# ⚙️ Fonctions principales

Afin de rendre notre robot opérationnel, nous avons développé plusieurs fonctions essentielles à son fonctionnement.

---

## 🚶 Fonction de marche avant

Cette fonction constitue la base du déplacement du robot.

Elle permet de synchroniser les mouvements des jambes et des pieds afin de faire avancer Otto-BDS le plus rapidement possible tout en conservant son équilibre.

<img width="544" height="537" alt="Marche_avant" src="https://github.com/user-attachments/assets/f8479dc7-f620-4e2f-8559-6a722f5571ae" />

---

## 🔙 Fonction de marche arrière

Cette fonction reprend le même principe que la marche avant mais en inversant les mouvements des servomoteurs.

Elle permet notamment de repositionner rapidement le robot ou de reculer face à un obstacle.

<img width="452" height="532" alt="Marche_arrière" src="https://github.com/user-attachments/assets/65535bb9-f476-4098-b18a-9002c4b7f533" />

---

## ↩️ Fonction de rotation vers la gauche

Pour certaines épreuves, il était indispensable que le robot puisse s'orienter rapidement.

Cette fonction permet à Otto-BDS d'effectuer une rotation vers la gauche afin d'ajuster sa trajectoire ou de se réaligner sur un parcours.

<img width="352" height="433" alt="Rotation gauche" src="https://github.com/user-attachments/assets/38c0c0b9-322a-4d92-a31a-6dc639efccee" />

---

## ↪️ Fonction de rotation vers la droite

Cette fonction est similaire à la précédente mais permet une rotation dans le sens opposé.

Elle était particulièrement utile lorsque le robot déviait légèrement de sa trajectoire.

<img width="352" height="433" alt="Rotation droite" src="https://github.com/user-attachments/assets/ff18cb59-14d7-4aa3-a775-4abebd2c3447" />

---

## 🎵 Fonction de lecture d'une mélodie

Cette fonction permet au robot de jouer une petite mélodie grâce à son buzzer intégré.

Même si elle n'améliore pas directement les performances du robot, elle apporte un aspect plus vivant et interactif à Otto-BDS.

<img width="352" height="433" alt="Mélodie" src="https://github.com/user-attachments/assets/b6ae449f-081a-420c-bb5d-2026002fd21d" />

---

## 💃 Fonction de danse

Cette fonction réalise une courte chorégraphie en combinant plusieurs mouvements du robot.

Initialement développée pour le côté amusant du projet, elle s'est révélée particulièrement utile lors des épreuves de Otto-Sumo.

En effet, une danse effectuée avant le début d'un combat permettait d'obtenir des points bonus. Cette petite animation a donc contribué à améliorer notre classement.

<img width="370" height="535" alt="Danse" src="https://github.com/user-attachments/assets/1b1d8214-ff88-42a3-a91b-d809ef7f50a6" />

---

# 🤖 Conclusion

La programmation a joué un rôle essentiel dans les performances de Otto-BDS.

Au-delà des fonctions de déplacement de base, les nombreux réglages et optimisations réalisés tout au long du projet ont permis d'améliorer progressivement les capacités du robot.

Les modifications effectuées avant les Ottolympiades se sont révélées particulièrement efficaces puisqu'elles ont directement contribué aux résultats obtenus lors des différentes épreuves.

Cette partie du projet nous a permis d'apprendre les bases de la programmation embarquée tout en comprenant l'importance des phases de test, d'analyse et d'amélioration continue dans le développement d'un système robotique.

Aujourd'hui, lorsque nous regardons Otto-BDS parcourir une piste, réaliser une danse ou affronter un adversaire en sumo, nous savons que derrière chacun de ses mouvements se cachent de nombreuses heures de programmation, de tests et de corrections.
