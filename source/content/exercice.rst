.. TNSI

.. toctree::
   :maxdepth: 1

Requêtes en langage SQL
=======================

Exercice 1
----------

Un hôtel gère ses chambres avec une base de données. Les chambres disposent de 1 à quatre lits. La relation **Chambre**
permet d’enregistrer le numéro de la chambre, la date (le jour réservé), l’heure d’arrivée, le nombre de lits et la
prise du petit-déjeuner pour le lendemain matin.

L’attribut ``date`` est une chaine de caractères, les attributs ``numéro``, ``heure`` et ``lits`` sont des nombres
entiers et l’attribut ``petitdej`` est un booléen.

Voici un extrait de la relation **Chambre**:

.. table::
   :align: center

   ====== ======== ===== ==== ========
   numéro date     heure lits petitdej
   ====== ======== ===== ==== ========
   45     21/11/22 17    2    True
   46     21/11/22 18    1    False
   ====== ======== ===== ==== ========
   
Écrire les requêtes SQL pour obtenir les informations suivantes:

#. Les numéros des chambres réservées à la date du "23/11/22".
#. Les numéros des chambres réservés à la date du "23/11/22" avec petit-déjeuner.
#. Le nombre de chambres sans petit-déjeuner réservés à la date du "24/11/22".
#. Le nombre de chambres réservés à la date du "24/11/22" avec 2 ou 3 lits.
#. Les enregistrements des clients arrivés le "20/11/22" après 18 heures.
#. L’heure d’arrivée du premier client le "19/11/22".

.. _exercice-1:

Exercice 2
----------

Une librairie est gérée à l’aide d’une base de données. Le modèle relationnel contient 5 relations décrites ci-dessous
avec leur schéma:

-  **Livres** (id_livre, titre, prixHT, année, id_genre, id_editeur)
-  **Auteurs** (id_auteur, nom, prénom)
-  **Écrits** (id_auteur, id_titre)
-  **Genre** (id_genre, genre)
-  **Éditeurs** (id_editeur, nom)

Les attributs ``id_livre``, ``id_auteur``, ``id_genre``, ``id_editeur`` et le couple ``(id_auteur, id_titre)`` sont des
clés primaires.

-  L'attribut ``id_editeur`` de la relation **Livres** est une clé étrangère en référence à la clé primaire ``id_editeur``
   de la relation **Éditeurs**.
-  L'attribut ``id_genre`` de la relation **Livres** est une clé étrangère en référence à la clé primaire ``id_genre``
   de la relation **Genre**.
-  L'attribut ``id_auteur`` de la relation **Ecrits** est une clé étrangère en référence à la clé primaire
   ``id_auteur`` de la relation Auteurs.
-  L'attribut ``id_titre`` de la relation **Ecrits** est une clé étrangère en référence à la clé primaire
   ``id_livre`` de la relation Livres.
   

Toutes les clés primaires et l'attribut ``année`` sont de type entier.

L'attribut ``prixHT`` est de type flottant. Les autres attributs sont des chaines de caractères.


#. Représenter le schéma relationnel de la base de données par un diagramme. On fera précéder les clés primaires du
   symbole \#, les clés étrangères seront soulignées. On reliera par une flèche les différentes relations.
   
#. Écrire en langage SQL les requêtes permettant d’obtenir les informations suivantes:

   a) Les titres des livres de la base.

   b) Les titres et années de parution des livres.

   c) Les titres des livres qui commencent par la lettre "A".

   d) Le prix HT maximal d’un livre de la base.

   e) Tous les champs de la table Auteurs.

   f) Le nombre d’auteurs contenus dans la base.

   g) Le nombre de livres référencés dans la base et le prix moyen.

   h) Les noms et prénoms de tous les auteurs par ordre alphabétique de nom.

   i) Les noms des auteurs dont le prénom est "Pierre".

   j) Les titres des livres coûtant plus de 15 euros HT avec leur prix HT.

   k) Les titres de livres coûtant moins de 15 euros avec leur prix TTC. La TVA est de 5,5%.

   l) Les titres et années de parution des livres parus de 2010 à 2015 ordonnés suivant l’année de parution de manière décroissante.

   m) Les titres des livres avec le nom de leur éditeur.

   n) Les titres des livres avec le genre "science".

   o) Les titres et les prix HT des livres du genre "policier" coûtant moins de 20 euros HT.

   p) Les années de parution de livres dans le genre "science" sans doublons.

   q) Le prix total de tous les livres parus en 2019 dans le genre "science".

   r) Les identifiants des livres dont l’auteure a pour prénom "Marie".

   s) Les titres des livres du genre "science" parus en 2019 contenant la chaine "nsi" dans le titre.

   t) Le titre du livre (ou les titres des livres) dont le prix est maximal.

   u) Le titre du livre (ou les titres des livres) dont le prix est maximal en 2015.

   v) Les titres des livres dont le prix est plus petit que le prix moyen avec leur prix.

   w) Les titres du livre le plus cher et du livre le moins cher avec leur prix. Il peut y en avoir plusieurs.

   x) Les titres des livres coûtant le plus cher avec le nom de leurs éditeurs.

   y) Les genres pour lesquels il n’y a aucun livre.

   z) Les titres des livres avec les noms des auteurs respectifs.
