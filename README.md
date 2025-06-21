# rechauffement-climatique-powerbi
# Projet Power BI : Analyse du Réchauffement Climatique

## 1) Dataset utilisé

Le dataset provient de Kaggle, intitulé **« Climate Change : Earth Surface Temperature Data »**.  
J’ai utilisé deux fichiers CSV sur les cinq disponibles :  
- Températures des villes  
- Températures des pays  

## 2) Objectifs

- Comparer les températures entre les villes et les pays.  
- Vérifier si les températures des villes sont plus élevées que celles des pays dans leur ensemble (hypothèse liée à l’urbanisation et effet d’îlot de chaleur).  
- Ou au contraire, si les températures sont plus élevées au niveau des pays (notamment en raison de zones de désertification).  
- Évaluer si cette différence de température est significative.  
- Analyser comment ces différences se manifestent tout au long de l’année.  
- Étudier l’évolution des températures et du réchauffement climatique depuis les années 1920.  
- Mesurer l’impact de la longitude et de la latitude sur ces températures.  

## 3) Enjeux et difficultés rencontrés

- Les tables « températures villes » et « températures pays » sont les données initiales téléchargées.  
- Création d’une table « Date » dans Power BI Desktop à l’aide de DAX, générée avec l’aide de ChatGPT.  
- Filtrage des données pour ne retenir que la période depuis 1920, pour limiter la volumétrie.  
- Création des tables « Pays » et « Villes » afin d’avoir un exemplaire unique des données, avec génération du code par ChatGPT.  
- Transformation des données latitude/longitude (format nombre + lettre) en valeurs numériques : les valeurs Nord (N) restent positives, Sud (S) deviennent négatives ; idem pour Est (E) positif et Ouest (W) négatif. Code Power Query généré par ChatGPT.  
- Création des tables « Longitude » et « Latitude » pour gérer les doublons de valeurs uniques, avec du code DAX généré par ChatGPT.  

## 4) Résultats

- Confirmation de l’augmentation des températures à l’échelle mondiale depuis 1920.  
- Les températures moyennes sont plus élevées à l’échelle des pays que des villes, avec une différence d’environ 1 degré.  
- En été, les températures des villes sont légèrement plus élevées que celles des pays.  
- Les températures augmentent jusqu’à une certaine latitude puis diminuent, avec un maximum proche de l’équateur.  
- Forte corrélation entre latitude et température, la latitude influence grandement les températures.  
- La longitude présente une dispersion des points, formant des groupes distincts, indiquant que la température dépend plus de facteurs géographiques (océans, continents, altitude) que de la longitude.  

## 5) Installation et Prérequis

- Power BI Desktop (version recommandée : [2.144.878.0 64-bit (juin 2025)])  
- Télécharger les fichiers CSV depuis Kaggle ici : [https://www.kaggle.com/datasets/berkeleyearth/climate-change-earth-surface-temperature-data]  
- Ouvrir le fichier `.pbix` avec Power BI Desktop pour accéder au dashboard  

## 6) Utilisation

- Ouvrir le fichier `RechauffementClimatique.pbix` avec Power BI Desktop  
- Naviguer entre les différentes pages du rapport pour explorer les analyses  
- Les filtres de dates et de localisation sont activables pour affiner les résultats  

## 7) Captures d’écran

!(Temporalité des températures.png)  
!(Géographie des températures.png)  

## 8) Licence

Ce projet est sous licence Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0).  
Voir le fichier LICENSE pour plus de détails.

## 9) Contact

Pour toute question ou collaboration, vous pouvez me contacter via : 
- LinkedIn : [ton profil LinkedIn](https://www.linkedin.com/in/louise-de-baglion-8074605a/)  

---

Merci de votre intérêt pour ce projet !

