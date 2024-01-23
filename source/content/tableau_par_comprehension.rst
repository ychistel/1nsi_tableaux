.. 1NSI

Tableaux par compréhension
==========================

   .. rubric:: Méthodes de construction de tableaux
      :name: méthodes-de-construction-de-tableaux

   .. rubric:: Construire un tableau initialisé avec une valeur
      :name: construire-un-tableau-initialisé-avec-une-valeur

   Si on souhaite construire un tableau de très grande taille avec une
   valeur initiale unique, python permet une construction rapide:
   ``tableau = [valeur initiale] * dimension du tableau``

   .. rubric:: Exemple
      :name: exemple

   Construire une liste L de 100 nombres tous égaux à 0.

   .. code:: python

      L = [0] * 100 # --> crée la liste L=[0,0,0,.....,0,0,0] avec 100 zéros

   .. rubric:: Créer un tableau par compréhension
      :name: créer-un-tableau-par-compréhension

   La construction d'un tableau par compréhension introduit la boucle
   for à l'intérieur des crochets du tableau à construire.

   La syntaxe est de la forme:
   ``[valeur for i in range(dimension du tableau)]``

   .. rubric:: Exemple
      :name: exemple-1

   #. Construire par compréhension une liste ordonnée de nombres:

      -  ``[i for i in range(5)]`` construit le tableau
         ``[0, 1, 2, 3, 4]``
      -  ``[i**2 for i in range(5)]`` construit le tableau
         ``[0, 1, 4, 9, 16]``
      -  ``[2*i+1 for i in range(5)]`` construit le tableau
         ``[1, 3, 5, 7, 9]``

   #. Construire un tableau à partir des valeurs d'un autre tableau :

   .. code:: python

      t=[2,3,5,7,11,13]
      p=[x**2 for x in t]
      print(p) # --> affiche le tableau p de valeur [4, 9, 25, 49, 121, 169] 

   #. Initialiser un tableau de tableaux par compréhension :

   .. code:: python

      t=[ [0]*3 for i in range(3) ]
      print(t) # --> affiche le tableau t de valeur [[0,0,0],[0,0,0],[0,0,0]]
