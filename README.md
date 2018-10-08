# doc
créer un compte sur : 
https://community.cloud.databricks.com

download data :
* https://www.kaggle.com/zynicide/wine-reviews#winemag-data_first150k.csv
* https://www.kaggle.com/neuromusic/avocado-prices
* https://www.kaggle.com/census/total-construction-spending-data-collection#total-construction-spending-office_metadata.json

loader les données dans databricks

importe notebook :
 * http://cdn2.hubspot.net/hubfs/438089/notebooks/spark2.0/Structured%20Streaming%20using%20Scala%20DataFrames%20API.html


QCM : 
https://docs.google.com/forms/d/e/1FAIpQLSfan3cshpWVFgAtbXtxD-x-l6yve3GGK72_kIQZBVOg2RRwdw/viewform?usp=sf_link

# TD sur la base du fichier winemag_data_first150k-8c60b.csv

- 0 / créer un notebook:
la première cellule doit contenir : 
``import org.apache.spark.sql.functions._
import spark.implicits._```

- 1 / Loader le ficher csv
- 2 / Typer la dataframe, notament les points et les prix
- 2 Bis / sauvegarder la donnée en parquet, partitioner par état
- 2 Ter / Loader le fichier parquet de la France et de la Grèce. puis sauvegarder les données en avro partitionner par cépage.
/!\ l'objectif est d'avoir un seul fichier pas cépage
- 3 / Lister les cépages
- 4 / Lister les cépages par pays
- 5 / Afficher la courbe de distribution des points
- 6 / Afficher la courbe de distribution des prix
- 7 / Idem 5 & 6 mais par pays 
- 8 / Calculer la moyene des points & prix par cépage 
- 9 / Qu'est ce qui impacte le plus le prix de vente ?
- 9 bis / Comment pouvez-vous mesurez si le château ?
- 10 / Ajouter à votre analyse le revenu moyen des états producteurs comme pondérateurs des prix.
vous allez devoir trouver la donnée, puis trouver comment la relier à votre table existante
- 11 / créer un pipeline pour transformer à minima les colones variety country, et point en features et price en label.
- 11 / Entrainer le modèle de votre choix (régression logistique par exemple) sur ces données
- 12 / sauver votre modele et votre pipeline
- 13 / produire une prevision pour un vin français avec du Pinot Noir et une note de 92.

Bonus : extraire de nouvelles colonnes depuis la description


