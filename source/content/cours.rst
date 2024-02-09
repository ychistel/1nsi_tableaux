Les tableaux
============

En programmation, un **tableau** est un type de données qui permet d'écrire plusieurs valeurs dans une même variable.

On définit le type tableau de la façon suivante:

- Le tableau est de **dimension fixe**. Cela signifie qu'il accepte un nombre fixe de valeurs;
- Les données d'un tableau sont du **même type** : des nombres ou des chaines de caractères ou etc;
- Le type tableau autorise la **modification** de ses valeurs;
- Le type tableau **ne permet pas l'ajout ou la suppression** de valeurs.

Les tableaux en Python
----------------------

En python, la structure de données **tableau** n'existe pas. On construit des tableaux avec la structure de données ``list`` ou ``tuple``.

.. rubric:: Le type liste

.. admonition:: Définition
   :class: definition

   Un tableau construit avec une **liste** est un **tableau dynamique**.

   -  La dimension d'une liste est variable, elle s'adapte au nombre de valeurs à écrire;
   -  Les données peuvent avoir des types différents (nombres entiers et chaines de caractères dans une même liste) 
   -  On peut ajouter, modifier, ou supprimer des valeurs ce qui change la dimension de la liste.

   Une liste se note entre **crochets** et contient les valeurs séparées par des virgules.

.. code:: python

   # jours de la semaine dans une liste
   jours = ["lundi","mardi","mercredi","jeudi","vendredi","samedi","dimanche"]

.. rubric:: Le type tuple

.. admonition:: Définition
   :class: definition

   Un tableau construit avec un **tuple** est un tableau **non mutable** ou **immuable**.
   Cela siginie que sa dimension est fixe, qu'on ne peut pas modifier ses valeurs, ni en supprimer, ni en ajouter.
   Un **tuple** se note entre **parenthèses** et contient les valeurs séparées par des virgules.

On définit la variable ``jours`` qui contient les jours de la semaine dans un tuple

>>> jours = ("lundi","mardi","mercredi","jeudi","vendredi","samedi","dimanche")

.. rubric:: Dimension d'une liste ou d'un tuple

.. admonition:: Définition
   :class: definition

   La **dimension** d'un tableau est le nombre d'éléments qu'il contient.

En python, la dimension d'un tableau créé avec une liste ou un tuple est donné avec la fonction ``len``.

On reprend la variable ``jours`` de type **tuple** qui contient les 7 jours de la semaine

>>> jours = ("lundi","mardi","mercredi","jeudi","vendredi","samedi","dimanche")
>>> len(jours)
7

Dans un autre exemple, on définit la variable ``notes`` qui contient des valeurs entières

>>> notes = [5,14,11,16]
>>> len(notes)
4

.. rubric:: Accéder à une valeur du tableau

.. admonition:: Propriétés
   :class: propriete
      
   Chaque élément d'un tableau (tuple ou liste) est accessible par son **indice** (index en anglais), c'est à dire par la position qu'il occupe dans le tableau.
   
   - Le premier élément d'un tableau est d'indice ``0``;
   - Le deuxième élément d'un tableau a pour indice ``1``;
   - Le dernier élément d'un tableau a pour indice la ``dimension du tableau - 1``;
   - On peut aussi accéder au dernier élément avec l'indice ``-1``.

En python, on accède à un élément du tableau en notant son indice entre crochets juste après le nom de la variable tableau.

On reprend le tuple ``jours`` qui contient les jours de la semaine. On peut accéder à chaque jour de la semaine avec les indices:

>>> jours = ("lundi","mardi","mercredi","jeudi","vendredi","samedi","dimanche")
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

.. rubric:: Un type itérable

.. admonition:: Définition
   :class: definition

   Un type est itérable lorsqu'on peu accéder à chacune de ses valeurs. 
   
   Les **listes** et les **tuples** python sont itérables.

On peut parcourir les éléments d'une liste et donc récupérer ses valeurs en **itérant** cette liste avec une **boucle**. Par exemple, avec une boucle qui utilise les **indices** de chaque élément de la liste:

On reprend le tuple ``jours``:

>>> jours = ["lundi","mardi","mercredi","jeudi","vendredi","samedi","dimanche"]

On crée une boucle ``for`` qui itère sur les 7 indices, de 0 à 6, c'est à dire avec un range(7)
   
>>> for i in range(7):
        print(jours[i])
"lundi"
"mardi"
"mercredi"
"jeudi"
"vendredi"
"samedi"
"dimanche"
         
Donnons un autre exemple, avec une boucle qui **accède directement** à chaque valeur du tableau

>>> for jour in jours:
        print(jour)
"lundi"
"mardi"
"mercredi"
"jeudi"
"vendredi"
"samedi"
"dimanche"

.. rubric:: Modifier une valeur de la liste

La modification d'une valeur d'une liste est possible. Pour cela, on procède à une nouvelle affectation sur l'élément de la liste en précisant son indice et la nouvelle valeur.

On définit la variable ``jours`` de type liste

>>> jours = ["lundi","mardi","mercredi","jedi","vendredi","samedi","dimanche"]

On remarque une erreur, il manque un "u" à jeudi qui a pour indice 3 ! On corrige l'erreur :
   
>>> jours[3] = "jeudi"
>>> jours
["lundi","mardi","mercredi","jeudi","vendredi","samedi","dimanche"]

Tableau de tableaux
-------------------

.. admonition:: Définition
   :class: definition

   Un tableau dont chaque élément est un tableau est appelé **tableau à 2 dimensions**. 
   
   La dimension (longueur) du tableau est donnée par le nombre de tableaux qu'il contient.

Par exemple, une grille de jeu peut se représenter par un tableau à 2 dimensions:

.. code::

   grille = [
      [0,0,0],    # première ligne
      [0,0,0],    # seconde ligne
      [0,1,0]     # troisième ligne
   ]

.. admonition:: Propriété
   :class: propriete

   L'accès à une valeur d'un tableau de tableaux se fait avec 2 indices:
   
   -  un premier indice pour accéder au tableau où se trouve la valeur;
   -  un second indice pour obtenir la valeur dans le tableau sélectionné. 
   
   Les indices sont notés entre crochets.

Soit un tableau T contenant les tableaux [4,5],[6,7] et [8,9].

En python, avec les listes, on a ``T=[[4,5],[6,7],[8,9]]``. On peut remarquer:

-  que le tableau T contient 3 tableaux de dimension 2 ; T est un tableau de longueur 3;
-  que le tableau [4,5] a pour indice 0, le tableau [6,7] a pour indice 1 et le tableau [8,9] a pour indice 2 ;
-  que les valeurs ont pour indice 0 et 1 pour chacun des trois tableaux de longueur 2.

On crée une liste ``T`` qui contient 3 listes. La liste ``T`` est de longueur 3.

>>> T=[[4,5],[6,7],[8,9]]
>>> len(T)
3

On peut aussi récupérer la longueur de la première liste de la variable ``T``

>>> len(T[0])
2

On peut accéder à la dernière liste contenue dans la variable ``T`` avec l'indice ``-1``
   
>>> T[-1]
[8,9]

On accède via les indices à la première valeur du tableau situé au milieu de ``T``
   
>>> T[1][0]
6
