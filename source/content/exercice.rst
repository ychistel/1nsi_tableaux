.. 1NSI

Exercices
=========

Exercice 1
---------

On considère le tableau ``T=[[1,2],[4,5],[7,8]]``.

#. Quelle est la dimension du tableau T ?
#. Écrire un code python qui remplace la valeur 4 du tableau ``T`` par la valeur 6.
#. Écrire un code python qui remplace la valeur 2 du tableau ``T`` par la valeur 4.
#. Écrire un script python qui ajoute le nombre 1 à toutes les valeurs du tableau T.

Exercice 2
----------

On représente une grille carrée de dimension 5 par un tableau. Chaque ligne de la grille est un tableau contenant 5 valeurs. Au début, la grille est vide et elle est représentée par un tableau ne contenant que des zéros.

.. figure:: ../img/dames_1.svg
   :align: center
   :width: 200

#. La variable ``damier``contient le tableau représentant la grille de dimension 5. Quel est est le contenu de cette variable.

#. On ajoute des pions sur cette grille. On dispose de 5 pions blancs sur la ligne du haut et 5 pions noirs sur la ligne du bas.

   .. figure:: ../img/dames_2.svg
      :align: center
      :width: 200

   Un pion blanc est représenté par la valeur 1 dans la grille et un pion noir est représenté par la valeur 2 dans la grille. Modifier la variable ``damier`` en y ajoutant les pions.

#. Les pions se déplacent verticalement. Les pions blancs vers le bas et les pions noirs vers le haut. Écrire une fonction ``deplace`` qui permet de déplacer un pion (blanc ou noir) d'une case. Un pion ne peut pas se déplacer s'il est bloqué par un autre pion ou s'il est sur le bord.

   .. figure:: ../img/dames_3.svg
      :align: center
      :width: 200

#. Lorsqu'un pion blanc est bloqué par un pion noir, il peut avancer uniquement en diagonale. Pour cela, il faut qu'un pion noir soit présent et alors il passe par dessus à condition de retomber dans la grille et sur une case vide. Le pion sauté n'est pas supprimé.

   .. figure:: ../img/dames_4.svg
      :align: center
      :width: 200

   Sur la figure, un pion blanc peut avancer car la case est libre en diagonale et l'autre est bloqué car la case est occupée par un pion noir.

   Écrire une fonction ``sauter`` qui fait sauter un pion en diagonale. Il faut :

   - vérifier que le pion est bien bloqué;
   - vérifier que le pion reste dans la grille;
   - vérifier que la case est libre.

   Si c'est bien le cas, le pion est déplacé dans la grille.

#. Le jeu s'arête lorsqu'un des joueurs a réussi à placer tous ses pions sur la ligne adverse. Si la partie est bloquée, le vainqueur est celui qui a le plus grand nombre de pions sur la ligne adverse.. En cas d'égalité, il y a match nul.



Exercice 3
----------

La suite de **Fibonacci** est une suite dont chaque valeur s’obtient en ajoutant les deux valeurs qui la précèdent,
avec les nombres :math:`0` et :math:`1` comme valeurs initiales.

Soit **fib** le tableau contenant les premiers nombres de la suite de Fibonacci: ``fib=[0,1,1,2,3,5,8,13]``

#. On saisit l’instruction ``len(t)``. Quelle est la valeur renvoyée ?
#. Comment peut-on afficher la dernière valeur du tableau ? Proposer plusieurs façons d’y parvenir.
#. Quelle sont les valeurs ``fib[4]`` et ``fib[8]`` ? Justifier.
#. Ajouter à la fin du tableau ``fib`` une nouvelle valeur de la suite de Fibonacci.

#. On souhaite compléter le tableau des nombres de la suite de Fibonacci.

   La fonction ``suivant`` prend en paramètre le
   tableau des nombres de la suite de Fibonacci et ajoute le terme suivant en fin de tableau. La fonction renvoie le
   tableau avec le nouveau terme ajouté.

   a) Ecrire le code de la fonction ``suivant``.
   b) Vérifier votre fonction en ajoutant plusieurs termes à la suite de Fibonacci.


Exercice 4
----------

#. Créer, en Python, un tableau ``panier`` contenant les fruits : pomme, poire, prune et orange. Chaque fruit est une
   chaine de caractères.

#. Écrire une fonction ``est_present`` qui prend en paramètre le tableau de fruits et un fruit. La fonction renvoie un
   booléen ``True`` ou ``False`` qui affirme si le fruit est dans le panier ou non.

   .. rubric:: Par exemple:

   >>> est_present(panier,'pomme')
   True
   >>> est_present(panier,'kiwi')
   False
   
#. Écrire une fonction ``ajoute`` qui prend en paramètre le tableau de fruits et un fruit pour l’ajouter au tableau de
   fruits si celui-ci n’y est pas encore.

   .. rubric:: Par exemple:

   >>> ajoute(panier,'kiwi')
   ['pomme','poire','prune','orange','kiwi']
   >>> ajoute(panier,'poire')
   ['pomme','poire','prune','orange','kiwi']

#. Écrire une fonction ``supprime`` qui prend en paramètre le tableau de fruits et un fruit pour le supprimer du tableau.

   La méthode ``remove(valeur)`` supprime dans un tableau la première occurence ``valeur``.

   .. rubric:: Par exemple:
   
   >>> supprime(panier,'kiwi')
   ['pomme','poire','prune','orange']
   >>> supprime(panier,'poire')
   ['pomme','prune','orange']

.. _exercice-2:

Exercice 5
----------

Soit ``t`` une variable de type tableau contenant telle que ``t=[7,1,3,9,7,6,2,7,5,9]``.

#. Écrire la fonction ``occurence`` qui prend en paramètres un tableau ``tab`` et une valeur ``x``. Cette fonction
   renvoie le nombre d'occurences de la valeur ``x`` que contient le tableau ``tab``. Si la valeur n'est pas présente
   dans le tableau, la fonction renvoie ``0``.

   .. rubric:: Par exemple:
   
   >>> occurence(t,7)
   3
   >>> occurence(t,4)
   0
   
#. Écrire la fonction ``decale`` qui prend en paramètre le tableau ``tab`` et le modifie en décalant toutes les nombres
   qu'il contient de 1 rang vers la droite. La première position, laissée libre, sera occupée par la dernière
   valeur décalée du tableau.

   >>> decale(t)
   [9,7,1,3,9,7,6,2,7,5]
   >>> decale(t)
   [5,9,7,1,3,9,7,6,2,7]


Exercice 6
----------

Lors d'un examen, un candidat a eu les notes suivantes:

- français: 12, coefficient : 4
- mathématiques: 13, coefficient : 5
- anglais: 9, coefficient : 2
- histoire: 14, coefficient : 2
- sciences: 11, coefficient : 3

On crée une liste dont chaque valeur est une liste constituée de la note et du coefficient.

La liste dans la variable ``notes`` telle que : ``notes = [[12,4],[13,5],[9,2],[14,2],[11,3]]``

#. Quelle est la valeur de ``notes[1]`` ?
#. Comment obtient-on la valeur et le coefficient de la troisième note de valeur 9 ? ?
#. Écrire une boucle qui affiche seulement les notes. Puis seulement les coefficients.
#. Écrire la fonction ``moyenne`` qui prend en paramètre la liste de notes et renvoie la moye nne des notes affectées de
   leurs coefficients.
