# Robotique-et-IA-3
construction d'un petit bras robotique avec 2 ou 3 servomoteur


## Objectif du projet

Construire un petit bras robotique avec un Arduino et 3 servomoteurs, puis le programmer pour qu'il aille de lui-même d'une position à une autre. Le but est d'apprendre à contrôler un mécanisme avec du code et à comprendre ce qu'est un degré de liberté.

## Les composantes utilisés 

1 Arduino Uno  
3 servomoteurs  
1 condensateur 470 µF à 1000 µF, 10 V ou plus (stabilise l’alimentation)
1 breadboard et des fils dupont mâle-mâle


## Comment ça fonctionne

Le bras fonctionne comme un bras humain, avec trois mouvements :

- La base tourne le bras vers la gauche ou vers la droite.
- L'épaule monte ou baisse le bras.
- Le coude plie ou déplie le bras pour l'approcher ou l'éloigner.

Un servomoteur est un petit moteur qui sait aller à un angle précis, entre 0° et 180°. Chaque servo reçoit des instructions de l'Arduino par un fil de signal. L'Arduino est le cerveau : il exécute le programme et dit à chaque servo « va à tel angle ».

Le programme contient une liste de positions (repos, prise, dépôt, retour au repos). Il envoie les angles de chaque position aux servos, mais il les avance un degré à la fois, avec une petite pause. C'est ce qui rend le mouvement doux au lieu d'être brusque. Quand une position est atteinte, le bras fait une pause, puis passe à la suivante. Quand la liste est finie, tout recommence.

## Résultat obtenu

Le bras fait une séquence automatique, il part de sa position de repos, se tourne et s'abaisse vers la gauche (position de prise), se déplace vers la droite (position de dépôt), puis revient au repos. Il répète cela en boucle, sans que personne n'ait à le toucher.

Le projet montre donc qu'avec un peu de code, on peut faire bouger un mécanisme avec précision, et que le bras possède 3 degrés de liberté, un par servomoteur.

## Lien Tinkerkad

https://www.tinkercad.com/things/8b1tPWSaJs5-terrific-kasi
