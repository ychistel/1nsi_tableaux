.. 1NSI

.. toctree::
   :maxdepth: 1

Créer des listes par compréhension
=================================
#. Une liste L1 est créée à l’aide d’une boucle for. On donne le code en
   Python:

   .. code:: python

      # on crée une liste vide L1
      L1 = []
      for i in range(10):
          L1.append(i)

   a) Quel est le contenu de la liste L1 ?
   b) Écrire un code en Python pour créer la liste ``L2 = [1, 3, 5, 7, 9, 11, 13, 15]`` avec une boucle ``for``.

#. La méthode suivante permet de créer des listes qui ont la particularité d’avoir la même valeur à tous les indices.
   Soit par exemple la liste ``L3 = [0, 0, 0, 0, 0, 0, 0, 0]``.

   a) Écrire un code en Python qui crée la liste L3 avec une boucle ``for``.
   b) Écrire un code en Python qui crée la liste L3 en utilisant la concaténation de liste.
   
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

#. On présente une dernière méthode de création de liste appelée **méthode par compréhension**.

   Par exemple, pour créer la liste L1, on écrit en python:

   .. code:: python

      L1 = [i for i in range(10)]

   a) Créer les tableaux suivants avec la méthode par compréhension:

      - ``L8 = ['z','z','z','z']``
      - ``L9 = [1,2,3,4,5,6,7,8,9]``
      - ``L10 = [9,8,7,6,5,4,3,2,1]`` 
      - ``L11 = [1,4,9,16,25,36]``
      - ``L12 = [[1, 2, 3], [1, 2, 3], [1, 2, 3], [1, 2, 3]]``

   b) Recréer la liste ``L13 = [[0, 0, 0], [0, 0, 0], [0, 0, 0], [0, 0, 0]]`` avec la méthode par compréhension.
   c) Modifier la liste ``L13`` pour avoir ``L13 = [[0, 2, 0], [0, 0, 0], [0, 0, 0], [0, 0, 0]]``. Que remarque-t-on ?

#. Créer les listes suivantes en utilisant la méthode par compréhension.

   - ``L14 = [[0, 1, 2, 3, 4], [1, 2, 3, 4, 5], [2, 3, 4, 5, 6], [3, 4, 5, 6, 7], [4, 5, 6, 7, 8]]``
   - ``L15 = [[1], [1, 2], [1, 2, 3], [1, 2, 3, 4], [1, 2, 3, 4, 5]]``
   - ``L16 = [[1, 1, 1, 1, 1], [2, 2, 2, 2, 2], [3, 3, 0, 3, 3], [4, 4, 4, 4, 4], [5, 5, 5, 5, 5]]`` (on crée la liste
     puis on la modifie)
