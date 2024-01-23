Les tableaux
============

En programmation, un **tableau** est un type de données qui permet d'écrire plusieurs valeurs dans une même variable.

On définit le type tableau de la façon suivante:

- Le tableau est de **dimension fixe**. Cela signifie qu'il accepte un nombre fixe de valeurs;
- Les données d'un tableau sont du même type : des nombres ou des chaines de caractères ou etc;
- Le type tableau autorise la modification de ses valeurs;
- Le type tableau ne permet pas l'ajout de valeurs ou la suppression de valeurs.


Les tableaux en Python
----------------------

En python, la structure de données **tableau** n'existe pas. On construit des tableaux avec la structure de données ``list`` ou ``tuple``.

.. rubric:: Le type liste

Un tableau construit avec une **liste** est un **tableau dynamique**. Cela modifie le comportement d'un tableau :

-  La dimension d'une liste est variable, elle s'adapte au nombre de valeurs à écrire;
-  Les données peuvent avoir des types différents (nombres entiers et chaines de caractères dans une même liste) 
-  On peut ajouter, modifier, ou supprimer des valeurs ce qui change la dimension de la liste.

Une liste se note entre **crochets** et contient les valeurs séparées par des virgules.

.. code:: python

   # jours de la semaine dans une liste
   jours = ["lundi","mardi","mercredi","jeudi","vendredi","samedi","dimanche"]

.. rubric:: Le type tuple

Un tableau construit avec un **tuple** est un tableau **non mutable** ou **immuable**.

Cela siginie que sa dimension est fixe, qu'on ne peut pas modifier ses valeurs, ni en supprimer, ni en ajouter.

Un **tuple** se note entre **parenthèses** et contient les valeurs séparées par des virgules.

.. code:: python

   # jours de la semaine dans un tuple
   jours = ("lundi","mardi","mercredi","jeudi","vendredi","samedi","dimanche")

.. rubric:: Dimension d'une liste ou d'un tuple

La dimension d'un tableau créé avec une liste ou un tuple est donné avec la fonction ``len``.

.. code:: python

   # jours de la semaine dans un tuple
   jours = ("lundi","mardi","mercredi","jeudi","vendredi","samedi","dimanche")
   notes = [5,14,11,16]

   >>> len(jours)
   7
   >>> len(notes)
   4

.. rubric:: Accéder à une valeur du tableau

Pour accéder à un élément du tableau (tuple ou liste), on utilise son indice (index en anglais) placé entre crochets juste après le nom de la variable.

- Le premier élément d'un tableau est d'indice 0;
- Le deuxième élément d'un tableau a pour indice 1;
- Le dernier élément d'un tableau a pour indice la dimension du tableau - 1;
- On peut aussi accéder au dernier élément ave l'indice -1.

.. admonition:: Exemple
   
   On reprend le tuple sur les jours de la semaine:

   .. code:: python

      # jours de la semaine dans un tuple
      jours = ("lundi","mardi","mercredi","jeudi","vendredi","samedi","dimanche")

      >>> jours[0]
      "lundi"
      >>> jours[1]
      "mardi"
      >>> jours[6]
      "dimanche"
      >>> jours[-1]
      "dimanche"
      >>> jours[-2]
      "samedi"

Manipuler les éléments d'une liste
----------------------------------

.. rubric:: Un type itérable

On peut parcourir les éléments d'une liste et donc récupérer ses valeurs en **itérant** cette liste avec une boucle.

#. Avec une boucle ``for`` qui utilise les indices de chaque élément de la liste:

   .. code:: python

      # On définit une liste jours
      jours = ["lundi","mardi","mercredi","jeudi","vendredi","samedi","dimanche"]

      # boucle for qui itère sur les 7 indices, de 0 à 6, soit un range(7)
      for i in range(7):
          print(jours[i])
          
#. Avec une boucle ``for`` et le mot clé ``in``:

   .. code:: python

      # On définit une liste jours
      jours = ["lundi","mardi","mercredi","jeudi","vendredi","samedi","dimanche"]

      # boucle for qui itère sur sur chaque élément de la liste
      for jour in jours:
          print(jour)

.. rubric:: Modifier une valeur de la liste

La modification d'une valeur d'une liste est possible. Pour cela, on procède à une nouvelle affectation sur l'élément
de la liste en précisant son indice et la nouvelle valeur.

.. code:: python

   # on définit la variable jours de type liste:
   jours = ["lundi","mardi","mercredi","jedi","vendredi","samedi","dimanche"]

   # zut il manque un "u" à jeudi qui a pour indice 3 ! On modifie :
   jours[3] = "jeudi"

.. rubric:: Ajouter une valeur à une liste

Si les tuples sont des tableaux non modifiables, les listes sont des tableaux que l'on peut agrandir en ajoutant des éléments.

Plusieurs méthodes sont possibles :

-  Par concaténation de deux listes existantes avec l'opérateur + ;
-  En utilisant la méthode **append** qui permet d'ajouter une valeur en fin de liste.

.. code:: python

   # Soit 2 tableaux de nombres
   >>> t=[0,1,2]
   >>> u=[3,4,5]
   
   # Concaténation des tableaux
   >>> t + u
   [0,1,2,3,4,5]

   # Avec la méthode **append** :
   >>> t=[0,1,2]
   >>> t.append(3)
   >>> t
   [0,1,2,3]

.. rubric:: Supprimer une valeur dans la liste

La suppression d'une valeur d'un tableau, en Python, ne se fait que sur les listes. La fonction ``del`` et les
méthodes ``remove`` et ``pop`` permettent de supprimer un élément du tableau. Elles s'utilisent très différemment:

.. code:: python

   # liste de mots
   >>> mots = ["na","ne","ni","no","nu"]
   
   # on supprime le dernier élément et on récupère sa valeur
   >>> mots.pop()
   'nu' #  -->  la liste mots = ["na","ne","ni","no"]

   # on supprime le second élément et on récupère sa valeur
   >>>mots.pop(1)
   'ne' #  --> la liste mots = ["na","ni","no"]

   # on supprime le premier élément avec del
   >>> del mots[0] #  --> la liste mots = ["ni","no"]

   # on supprime le mot "no"
   mots.remove("no") # --> la liste mots = ["ni"]

Tableau de tableaux
-------------------

Un tableau peut contenir des tableaux ! On parle alors de tableaux à 2 dimensions.

.. admonition:: Exemple

   Une grille de jeu peut se représenter par un tableau à 2 dimensions:

   .. code::

      grille = [
         [0,0,0],    # première ligne
         [0,0,0],    # seconde ligne
         [0,1,0]     # troisième ligne
      ]

Pour accéder à une valeur de ce tableau, on utilise un premier indice pour sélectionner le tableau où se trouve la
valeur puis un second indice pour obtenir la valeur dans le tableau sélectionné. Les indices sont notés entre crochets.

.. admonition:: Exemple

   Soit un tableau T contenant les tableaux [4,5],[6,7] et [8,9].

   En python, avec les listes, on a ``T=[[4,5],[6,7],[8,9]]``. On peut remarquer:

   -  que le tableau T contient 3 tableaux de dimension 2 ; T est un tableau de longueur 3;
   -  que le tableau [4,5] a pour indice 0, le tableau [6,7] a pour indice 1 et le tableau [8,9] a pour indice 2 ;
   -  que les valeurs ont pour indice 0 et 1 pour chacun des trois tableaux de longueur 2.

.. code:: python

   # Liste contenant 3 listes
   >>> T=[[1,2,3,4],[5,6,7],[8,9]]

   >>> len(T)
   3 # --> renvoie la valeur 3 car T contient 3 listes
   
   >>> len(T[0])
   4 # --> renvoie 4 car la première liste a pour longueur 4  T[0]=[1,2,3,4]

   >>> T[-1]
   [8,9] # renvoie la liste [8,9] qui est le dernier élément du tableau T

   >>> T[0][2]
   3 # renvoie le nombre 3 car T[0] est la liste [1,2,3,4] et que l'élément d'indice 2 est 3.
