Les jointures en SQL
====================

On redonne le modèle relationnel utilisé pour notre base de données ``livres.db``.

.. figure:: ../img/schema_relationnel_romans.png
   :alt: image
   :class: b-8
   :align: center
   :width: 480

Dans la première partie, nous avons réalisé des requêtes SQL sur une relation à chaque fois.

On poursuit notre travail sur le notebook commencé dans l'activité précédente.

Comment obtenir les données issues de plusieurs relations ? Pour ce faire, on réalise des jointures en utilisant les
clés étrangères.

La clause ``JOIN --- ON ...`` réalise cette jointure en remplaçant les trois tirets par la relation à joindre et les
trois points par une égalité entre les clefs étrangères liant les deux relations.

.. admonition:: Exemple

   .. code-block:: sql

      SELECT attributs FROM TableA Join TableB ON TableA.cle1 = TableB.cle2 WHERE Selecteur

#. On va interroger notre base pour recueillir les titres de romans et les noms de leur auteur.

   a) Écrire une requête SQL qui recueille les attributs ``titre`` et ``id_auteur`` de la relation livre, ordonnés
      selon la clé étrangère ``id_auteur par ordre croissant``.

   b) Écrire une requête SQL qui recueille les auteurs ordonnés par ordre croissant.
   
      Si vos requêtes sont correctes, vous obtenez les résultats suivants :

      .. figure:: ../img/jointure_livre_auteur.png
            :alt: image
            :align: center
            :width: 480

      On peut donc relier ces informations avec la clé étrangère ``id_auteur``.

   c) Recopier dans une cellule de votre feuille de travail sql la requête suivante pour effectuer la jointure en SQL:

      .. image:: ../img/requete_sql_1.png
         :alt: image
         :align: center

#. Écrire les requêtes SQL suivantes en effectuant une jointure:

   a) Recueillir le titre du roman, le nom de l’auteur et sa date de naissance.

   b) Recueillir le titre du roman, le nom de l’auteur et sa date de naissance pour les auteurs nés après 1918.

   c) Recueillir le nombre d’enregistrements de la requête précédente.

   d) Recueillir le titre et la langue d’écriture du roman.

   e) Recueillir les titres de romans écrits en français.

   f) Recueillir les titres de romans écrits en anglais publiés avant 1950.

#. Donner un exemple qui nécessite de joindre plusieurs relations entre elles.

#. On veut recueillir le nom et la langue d’écriture de l’auteur.

   a) Compléter la requête SQL suivante:

      .. image:: ../img/requete_sql_2.png
         :alt: image
         :align: center

   b) Exécuter cette requête dans votre feuille de travail sql. Que remarquez-vous ?

   c) La clause DISTINCT placée juste après la clause SELECT évite les doublons. Corriger votre requête SQL.

#. On veut recueillir les genres de chaque roman.

   a) Compléter la requête SQL suivante:

      .. image:: ../img/requete_sql_3.png
         :alt: image
         :align: center

   b) Exécuter cette requête dans votre feuille de travail sql.

   c) Que se passe-t-il si les relations sont écrites dans un ordre différent?

#. Écrire les requêtes SQL suivantes:

   a) Recueillir les auteurs qui ont écrit leurs romans en français.

   b) Recueillir les titres de romans anglais, les noms et les prénoms de leur auteur.

   c) Recueillir les titres de romans anglais, l’année de publication, les noms et les prénoms de leur auteur publiés
      entre 1960 et 1970 rangés du plus récent au plus ancien.

   d) Recueillir les titres de roman d’anticipation.

   e) Recueillir les titres et les genres des romans de Philip K.Dick.

   f) Recueillir les noms et prénoms des auteurs et les titres de romans dystopiques anglais.
