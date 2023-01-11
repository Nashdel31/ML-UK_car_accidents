# ML-UK_car_accidents

L'objectif de ce projet est de prédire la gravité des accidents de voiture. 
<br>
Les données proviennent des rapports de la police du Royaume Uni. 

<br>L'analyse des données a révélé nombre de valeurs manquantes, des données brutes à standardisées 
et un déséquilibre d'un rapport 10 entre les 3 classes d'intérêt. Et même après traitement de tous ces
aspects, il a fallu se placer dans l'hypothèse d'un besoin spécifique : 
<br>imaginons un chef d'entreprise qui souhaite connaitre la gravité en cas d'accident d'un de ces 
employés dans le but de savoir s'il doit gérer son absence ou non. Dans ce cas on peut regrouper les 
gravités 1 et 2 pour obtenir des modèles prédictifs exploitables.

Le modèle "Random Forest" donne les meilleurs résultats :
<code>
| gravité    | precision   | recall | f1-score  | support
|  2         |     0.78    |  0.70  |    0.73   |  79319
|  3         |     0.73    |  0.80  |    0.76   |  79913</code><br><code>
|accuracy avg|             |        |    0.75   | 159232
|   macro avg|    0.75     |  0.75  |    0.75   | 159232
|weighted avg|    0.75     |  0.75  |    0.75   | 159232
</code>
<br><br>

<br><br>
Source : [www.kaggle.com](www.kaggle.com/datasets/daveianhickey/2000-16-traffic-flow-england-scotland-wales?select=accidents_2012_to_2014.csv)

30nov : 01 => Analyse descriptive du dataset 1
<br>
03déc : 02 => Traitement Junction_Control
<br>
07déc : 03 => Dropna
<br>
09déc : 04 => Dataset nettoyé
<br>
10déc : 05 => Traitement données temporelles et mapping
<br>
14déc : 06 => 1er modèle prédictif KNN
<br>
19déc : 07 => modèles prédictifs KNN, DT, RF avec le dataset déséquilibré
<br>
05jan : 08 => modèles prédictifs DT et RF avec le dataset rééquilibré
<br>
06jan : 09 => modèles prédictifs DT, RF avec gravité 1 et 2 regroupées.
