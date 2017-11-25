# <center><u>Spark</u></center>

##### Introduction Spark
Super jointure entre Data Scientist et Data Engineer.<br>
Spark est une librairie, un jar naturellement utilisable avec Scale et Java. Aujourd'hui on peut aussi coder avec Python via Jython.

##### L'arrivée de Spark 2.0

Dans les nouvelles API de spark 2.0 on a la notion de dataframe et autres, rendant spark plus performant.
<br>
Spark cherche à réduire le nombre de passages entre les noeuds (étape shuffle) et donc les transitions réseaux qui sont couteuses.
<br>
Les RDDs c'est la finallement la notion de dataset.<br>
On écrit de manière déclarative. L'évaluation passe par le terminal. Quand c'est *laizy*, les parties du graphique déjà exectuées ne sont pas à refaire.

##### Comment Spark est né (financierement) - Databricks
C'est DataBricks qui a financé Spark.

##### Spark en lui-même
L'idée c'est de coder du distribué comme si c'était du sequentiel. <br>
RDD est resilient. Le RDD se divise sur 4 noeuds par exemple. Si le noeud 3 plante, la partie 3 du RDD sera dupliquée ailleurs.<br>
Spark a été écrit en Scala donc plus performant avec ce langage. Autre avantage de scala, c'est un langage compatible pour les différents métiers de la donnée.

##### Un peu de code
```
sc.parallellize(...)
# Permet de créer un RDD et parallelliser du code.
```

##### Notion de Spark-SQL
L'idée est simple, pouvoir requeter en langage SQL.

##### Architecture Spark
- Driver Program: **SparkContext**
- Cluster Manager: **Master**
- Worker Node(s): **Executor(s)**

Avec Cassandra, pour optimiser l'initialisation de notre cluster, on cherche à mettre un slave par noeud.
