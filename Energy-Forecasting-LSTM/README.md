# Prédiction de la Consommation Énergétique avec le Machine Learning  
## Prévision de Séries Temporelles (LSTM)


### Résumé

L’objectif de cette recherche était de prédire la consommation énergétique en utilisant les données de l’opérateur du système de transmission de la Finlande.  
Le but était de tester si un modèle de machine learning pouvait fournir des résultats suffisamment fiables pour un problème complexe de prévision, en explorant différentes techniques et en développant un modèle basé sur les données pour la prévision énergétique.  

Le jeu de données contenait 6 années de consommation horaire d’électricité en Finlande. Il s’agissait d’une série temporelle univariée, présentant une forte saisonnalité.  
Un modèle de **Long Short-Term Memory (LSTM)** a été utilisé pour entraîner les données.  
L’évaluation a été réalisée à l’aide de la métrique **RMSE (Root Mean Squared Error)**, permettant une comparaison directe avec les valeurs réelles de consommation.  

Les résultats montrent que la consommation électrique peut être prédite avec des algorithmes de machine learning. Ces prévisions peuvent être utilisées pour faciliter le déploiement d’énergies renouvelables, anticiper les jours de forte ou faible consommation, et réduire le gaspillage lié aux centrales polluantes de réserve.

### Implémentation du Modèle

Les données ont été importées depuis l’opérateur du système de transmission finlandais sous format **CSV**, puis déposées dans un dépôt GitHub.  
Le jeu de données contenait **52 965 observations** et **5 variables**, sans valeurs manquantes.  
- Consommation minimale : **5 341 MWh**  
- Consommation maximale : **15 105 MWh**  
- Consommation moyenne : **9 488,75 MWh**  

Il s’agit d’une série temporelle univariée, avec une colonne pour le temps et une autre pour la consommation énergétique.  
Pour prédire la consommation quotidienne, les données ont été **agrégées par jour** à l’aide de la fonction `resample`, convertissant les fréquences horaires en fréquences journalières.  

L’entraînement du modèle LSTM a été réalisé avec un ensemble d’apprentissage et un ensemble de validation, afin d’évaluer les performances pendant l’entraînement.  
L’algorithme a parcouru le jeu d’apprentissage **60 fois (epochs)**, avec une taille de lot (**batch size**) de 20, mettant à jour les poids du modèle après chaque lot.
