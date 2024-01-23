.. 1NSI

Exercices
=========

Exercice 1
---------

On considère la liste de nombres suivante: ``L=[1,2,0,4,5]``.

#. Écrire une instruction python qui remplace la valeur 0 de la liste L par la valeur 3.
#. Écrire un script python qui ajoute le nombre 10 à toutes les valeurs de la liste L.
#. Écrire la fonction ``augmente`` qui prend en paramètre un tableau ``t`` de nombres et un nombre entier ``x``. Cette fonction renvoie le tableau ``t`` après avoir ajouté le nombre ``x`` à toutes les valeurs du tableau ``t``.

Exercice 2
----------

Soit L1 et L2 deux tuples tels que : ``L1 = (1,3,5,7,9)`` et ``L2 = (2,4,6,8)``.

#. Est-il possible d'ajouter les valeurs de L2 à la fin de L1 ? Justifier.
#. La fonction ``list(tuple)`` transforme un tuple en liste.
   Transformer les tuples L1 et L2 en listes.
#. Écrire un script python qui rassemble dans une même liste L3 les éléments de L1, en début de liste, puis les éléments
   de  L2 en fin de liste L. On doit obtenir ``L3 = [1,3,5,7,9,2,4,6,8]``.
#. Écrire un script python qui rassemble dans une même liste L4 les éléments de L1 avec les éléments de L2 rangés dans l'ordre
   croissant. On doit obtenir ``L4 = [1,2,3,4,5,6,7,8,9]``.


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
