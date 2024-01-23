.. 1NSI

.. toctree::
   :maxdepth: 1

Carré magique
=============

Présentation mathématique
-------------------------

Un carré d'ordre :math:`n` est un tableau carré contenant :math:`n^2` nombres entiers strictement positifs.

On dit qu'un carré d'ordre :math:`n` est **magique** si:

-  il contient tous les nombres entiers de :math:`1` à :math:`n^2`;
-  les sommes des nombres de chaque ligne, les sommes des nombres de chaque colonne et les sommes des nombres des 2
   diagonales sont égales.

.. admonition:: Exemple
   :name: exemple

   Voici un carré magique d'ordre 3

   .. image:: ../img/ex4.png
      :alt: ex4.png
      :align: center
      :width: 200
      :class: mg-b

   On donne un second carré de nombres d'ordre 4:

   .. image:: ../img/carre_2.png
      :alt: carre_2.png
      :align: center
      :width: 160

Le carré de nombres d'ordre 4 est-il un carré magique ? Justifier.

Des carrés de nombres en Python
-------------------------------

On modélise, en python, un carré par une liste contenant les listes des nombres de chaque ligne.

En python, le carré magique d'ordre 3 est représenté par une liste de 3 listes de longueur 3 chacune.

.. code:: python

   carre1=[
       [2,7,6],
       [9,5,1],
       [4,3,8]
   ]

#. Représenter le carré d'ordre 4 en python stocké dans la variable ``carre2``.

#. a) Quelle est la valeur de ``len(carre2)`` ?

   b) Quelle est la valeur de ``carre2[1]`` ?

   c) Quelle est la valeur de ``carre2[0][2]`` ?

   d) Quelle instruction permet de récupérer la valeur 10 du carré 2 ?

#. On donne le code de la fonction **calcul_ligne**.

   .. code:: python

      def calcul_ligne(carre,n):
          somme=0
          for nombre in carre[n]:
              somme=somme+nombre
          return somme

   a) Quelle valeur renvoie l'appel de la fonction ``calcul_ligne(carre1,2)`` ?

   b) Quels calculs peut-on effectuer sur un carré de nombres avec la fonction calcul_ligne ? Comment ?

#. Écrire la fonction ``calcul_colonne`` qui prend en paramètre un carré de nombres et le numéro d'une colonne du carré
   de nombres. La fonction ``calcul_colonne`` renvoie la somme des nombres de cette colonne.

   Par exemple, l'appel ``calcul_colonne(carre1,0)`` renvoie la valeur 15.

#. On donne le code de la fonction **calcul_diagonale** qui prend en paramètre un carré de nombres. Cette fonction
   calcule la somme des nombres d'une diagonale.

   .. code:: python

      def calcul_mystere(carre):
          somme=0
          for i in range(len(carre)):
              somme=somme+carre[i][i]
          return somme

   Quel calcul effectue l'appel ``calcul_mystere(carre2)`` ?

#. Pour calculer la somme des nombres de l'autre diagonale, on écrit la fonction ``calcul_diagonale_2`` qui prend en
   paramètre le carré de nombres et renvoie la somme des nombres positionnés sur la seconde diagonale du carré.
   
   Écrire cette fonction en python.

#. On donne le code de la fonction ``intrus`` qui a pour paramètre ``liste`` de type liste.

   .. code:: python

      def intrus(liste):
          valeur=liste[0]
          for nombre in liste:
              if nombre!=valeur:
                  return False
          return True

   a) Quelle valeur est renvoyée par l'appel ``intrus([7,7,5,7])`` ?
   b) Quelle valeur est renvoyée par l'appel ``intrus([15,15,15,15,15,15,15,15])`` ?
   
#. La fonction ``est_magique`` prend en paramètre un carré de nombres et renvoie ``True`` si le carré est magique,
   ``False`` sinon.

   L'algorithme proposé ci-dessous consiste à placer dans une même liste les sommes de toutes les lignes, les sommes de
   toutes les colonnes et les sommes de chaque diagonale.

   Lorsque cette liste est complète, on vérifie qu'elle contient la même valeur de somme.

   On donne cette fonction en pseudo-code :

   .. code:: python
   
      def est_magique(carré):
          créer une liste vide S
          ajouter dans S la somme des nombres en ligne de carré
          ajouter dans S la somme des nombres en colonne de carré
          ajouter dans S la somme de la première diagonale de carré
          ajouter dans S la somme de la deuxième diagonale de carré
          Si les tous les nombres de S sont égaux:
              renvoyer "le carré est magique"
          sinon:
              renvoyer "le carré n'est pas magique"

   Écrire le code de la fonction ``est_magique`` en Python.

#. Utiliser votre programme pour vérifier si le carré d'ordre 4 est magique.
