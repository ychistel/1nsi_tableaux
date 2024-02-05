.. 1NSI

.. toctree::
   :maxdepth: 1

Créer des listes en Python
==========================

Une liste python est le type qui permet de représenter des tableaux. Les listes Python sont des tableaux dynamiques car ils peuvent être agrandis ou réduits. Cela signifie que l'on peut ajouter ou supprimer des valeurs dans une liste.

Il existe plusieurs pour créer des listes:

-  On crée une liste vide et ensuite on ajoute des valeurs avec la méthode ``append``;
-  On crée des listes par concaténation;
-  On crée des listes par compréhension.

Construction avec la méthode ``append``
---------------------------------------

On donne le code en Python:

.. code:: python

   # on crée une liste vide L1
   L1 = []
   for i in range(10):
         L1.append(i)

#. Quel est le contenu de la liste L1 ?
#. Écrire un code en Python pour créer la liste ``L2 = [1, 3, 5, 7, 9, 11, 13, 15]`` avec une boucle ``for``.
#. Écrire une fonction ``liste_nulle`` qui prend en paramètre la taille ``n`` de la liste et renvoie une liste contenant ``n`` fois la valeur ``0``. Par exemple, l'appel ``L3 = liste_nulle(8)`` crée la liste ``L3 = [0, 0, 0, 0, 0, 0, 0, 0]``.

Construction avec la concaténation
----------------------------------

On peut concaténer des listes Python comme on le fait avec des chaines de caractères.

Par exemple, la concaténation des listes ``[1,2]`` et ``[3,4]`` donne la liste ``[1,2,3,4]``.

#. Écrire en Python la concaténation des listes ``[1,2]`` et ``[3,4]``.
#. Écrire un code en Python qui crée la liste ``L3 = [0, 0, 0, 0, 0, 0, 0, 0]`` en utilisant la concaténation de liste.  
#. On donne la fonction suivante écrite en Python:

   .. code:: python

      # on crée une liste vide L1
      def init_tab(v,n):
          return [v]*n
          
      L4 = init_tab(1,5)

   a) Est-il possible de créer la liste L3 avec cette fonction ? Si oui, comment ?
   b) Créer avec cette fonction les listes :

      -  ``L5 = [’a’, ’a’, ’a’, ’a’, ’a’]``
      -  ``L6 = [L4, L4, L4]``
      -  ``L7 = [[0, 0, 0], [0, 0, 0], [0, 0, 0], [0, 0, 0]]``

   c) Modifier la liste L5 avec l'instruction ``L5[0] = 'b'``. Quel est le contenu de L5 ?
   d) Modifier la liste L7 pour avoir ``L7 = [[0, 2, 0], [0, 0, 0], [0, 0, 0], [0, 0, 0]]``. Que remarque-t-on ?

Construction par compréhension
-------------------------------

On présente une dernière méthode de création de liste appelée **méthode par compréhension**.
Par exemple, pour créer la liste L1, on écrit en python:

.. code:: python

   L1 = [i for i in range(10)]

#. Créer les tableaux suivants avec la méthode par compréhension:

   - ``L8 = ['z','z','z','z']``
   - ``L9 = [1,2,3,4,5,6,7,8,9]`` 
   - ``L10 = [[1, 2, 3], [1, 2, 3], [1, 2, 3], [1, 2, 3]]``

#. Recréer la liste ``L11 = [[0, 0, 0], [0, 0, 0], [0, 0, 0], [0, 0, 0]]`` avec la méthode par compréhension.
#. Modifier la liste ``L11`` pour avoir ``L13 = [[0, 2, 0], [0, 0, 0], [0, 0, 0], [0, 0, 0]]``. Que remarque-t-on ?
#. Créer les listes suivantes en utilisant la méthode par compréhension.

- ``L12 = [[0, 1, 2, 3, 4], [1, 2, 3, 4, 5], [2, 3, 4, 5, 6], [3, 4, 5, 6, 7], [4, 5, 6, 7, 8]]``
- ``L13 = [[1], [1, 2], [1, 2, 3], [1, 2, 3, 4], [1, 2, 3, 4, 5]]``
- ``L14 = [[1, 1, 1, 1, 1], [2, 2, 2, 2, 2], [3, 3, 0, 3, 3], [4, 4, 4, 4, 4], [5, 5, 5, 5, 5]]`` (on crée la liste puis on la modifie)
