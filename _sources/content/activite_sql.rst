.. TNSI

.. toctree::
   :maxdepth: 1

Langage SQL
===========

Le langage SQL "Stuctured Query Language" permet d’effectuer des requêtes sur des bases de données.

Les mots clés du langage SQL qui réalisent ces requêtes sont appelées des **clauses**.

On donne ci-dessous quelques exemples de requêtes en langage SQL.

.. note::

   #. Chaque requête écrite en SQL se termine par un point virgule. 
   #. Les clauses sont écrites en MAJUSCULE pour être plus lisibles mais le SQL est insensible à la casse.

On reprend notre modèle relationnel sur les romans de science-fiction pour effectuer quelques requêtes en SQL.

.. figure:: ../img/schema_relationnel_romans.png
   :class: b-8
   :align: center
   :width: 480

   Schéma relationnel de la base **romans**

Requête d'interrogation d'une table
-----------------------------------

#. Interroger une table pour en extraire toutes les valeurs des attributs.

   La clause ``SELECT ... FROM ---`` où les trois points sont remplacés par les attributs souhaités séparés par des
   virgules et les trois tirets sont remplacés par la relation interrogée.

   .. admonition:: Exemple

      .. code-block:: sql

         SELECT attribut1, attribut2 FROM Table

   a) Écrire une requête permettant d’obtenir les titres des romans de la base.
   b) Écrire une requête permettant d’obtenir les noms et prénoms des auteurs de la base.

#. Lors d’une requête d’interrogation, il est possible d’y ajouter une **condition** ou un **sélecteur**.

   La clause ``WHERE ...`` placée en fin de requête réalise cette opération où les trois points sont remplacés par une
   condition ou sélecteur écrit avec les opérateurs habituels (=, <, >, etc.).

   .. admonition:: Exemple

      .. code-block:: sql

         SELECT attributs FROM Table WHERE Selecteur
         
   a) Écrire une requête permettant d’obtenir les titres des romans écrits après 1900.
   b) Écrire une requête permettant d’obtenir les noms et prénoms des auteurs nés en 1920.
   
#. Le résultat d’une requête d’interrogation peut être triée.

   Pour ce faire, on ajoute en fin de requête la clause ``ORDER BY ...`` ordre en remplaçant les trois points par
   l’attribut souhaité et en indiquant l’ordre souhaité par ``DESC`` (décroissant) ou ``ASC`` (croissant).

   .. admonition:: Exemple

      .. code-block:: sql

         SELECT attributs FROM Table WHERE Selecteur ORDER BY attribut ASC

   a) Écrire une requête permettant d’obtenir les titres des romans rangés par ordre croissant.
   b) Écrire une requête permettant d’obtenir les noms et prénoms des auteurs rangés par année de naissance.

Les fonctions d'agrégation
--------------------------

Il est parfois utile d’obtenir des informations numériques (statistiques) sur les valeurs d’un attribut : nombre d’enregistrements dans une relation, valeur moyenne, valeur maximale ou minimale ou bien la somme des valeurs.

Pour ce faire, on utilise les **fonctions d’agrégation**. Ces fonctions prennent en paramètre les attributs sur
lesquels ils s’appliquent. Cette fonction est placée juste derrière la clause ``SELECT``.

.. admonition:: Exemple

   .. code-block:: sql

      SELECT Fonction agrégation(attribut) FROM Table
      
a) La fonction COUNT() donne le nombre d’enregistrements d’une relation.

   Écrire une requête donnant le nombre total de romans de la base.

b) Les fonctions MAX() et MIN() donnent la valeur maximale et minimale d’un attribut.

   Écrire une requête donnant l’année de naissance du plus jeune auteur.

Insérer un nouvel enregistrement
--------------------------------

La clause ``INSERT INTO --- VALUES ...`` **ajoute** un enregistrement dans une relation. Les trois tirets sont remplacés par le nom de la relation et les noms des attributs et les trois points par les valeurs à insérer dans le même ordre que les attributs.

.. admonition:: Exemple

   .. code-block:: sql

      INSERT INTO Table (attribut1, attribut2) VALUES (valeur1, valeur2)

a) Écrire une requête qui ajoute l’écrivaine J.K. Rowling née en 1965.

b) Écrire une requête qui ajoute le roman "Harry Potter à l’école des sorciers" écrit en 2001.

Modifier, supprimer un enregistrement
--------------------------

#. La clause ``UPDATE --- SET ... WHERE condition`` **modifie** la valeur d’un attribut d’une relation. Les trois tirets sont remplacés par le nom de la relation et les trois points par l’affection à l’attribut de la nouvelle valeur.

   .. admonition:: Exemple

      .. code-block:: sql

         UPDATE Table SET attribut1 = valeur1, attribut2 = valeur2 WHERE Selecteur

   a) Écrire une requête qui modifie le titre du roman "Blade runner" par son titre original.

   b) Écrire une requête qui modifie le prénom de l’écrivaine J.K. Rowling par "Joanne" Rowling.

#. La clause ``DELETE FROM --- WHERE ...`` **supprime** un enregistrement d’une relation. Les trois tirets sont remplacés par le nom de la relation et les trois points par une condition qui précise la valeur de l’attribut à supprimer.

   .. admonition:: Exemple

      .. code-block:: sql

         DELETE FROM Table WHERE Selecteur

   a) Écrire une requête qui supprime le roman Harry Potter.

   b) Écrire une requête qui supprime l’écrivaine Joanne Rowling.



Requêtes SQL sur la base de données ``romans.db``
-------------------------------------------------

La base de données contenant nos 5 relations a déjà été créée et peut être utilisée dans CAPYTALE. Il suffit de
récupérer le fichier sur l'ENT et de l'ajouter en fichier annexe de votre feuille de travail SQL.

#. Lorsque votre environnement est prêt, saisir toutes les requêtes précédentes dans différentes cellules de votre feuille de travail et contrôler les résultats.

#. Écrire et exécuter les requêtes supplémentaires suivantes:

   a) Obtenir les genres de romans;
   b) Obtenir les titres de romans écrits en 1950;
   c) Obtenir les romans écrits après 1960;
   d) Obtenir les romans écrits entre 1900 et 1920;
   e) Obtenir les auteurs nés avant 1900;
   f) Obtenir les genres de romans commençant par la lettre s;
   g) Ajouter une nouvelle langue;
   h) Ajouter à nouveau l’écrivaine Joanne Rowling;
   i) Ajouter deux romans Harry Potter;
   j) Ajouter les genres fantaisie et sorcellerie;
   k) Ajouter dans la relation livre_par_genre les romans d’Harry Potter et leur genre.
