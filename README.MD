# Score Éditorial Anime
 PROJET FINAL — DATA SCIENCE
 # OBJECTIF Projet
 -Identifier rapidement des animés "à forte valeur éditoriale" à partir de données limitées pour une plateforme de streaming.
 ## vérifier le dataset
 On identifie les valeurs manquantes par colonne pour savoir où il faudra éventuellement les remplir ou supprimer des lignes.
On détecte les doublons pour nettoyer le dataset et éviter des biais.
On consulte les types de colonnes pour comprendre la nature des données et préparer leur traitement.

2) nettoyer le dataset avant analyse

-Supprimer les lignes avec des valeurs manquantes pour éviter les problèmes lors des calculs.

-Éliminer les doublons pour ne pas biaiser les résultats.

-Retirer les colonnes inutiles pour se concentrer sur les données pertinentes

3) calculer l'écart entre la meilleure et la pire note

-J’ai crée une nouvelle colonne Ecart_Note qui représente l’écart entre la meilleure et la pire note pour chaque produit.

calculer l'écart entre la meilleure et la pire note
df_clean['Ecart_Note'] = df_clean['Note_Meilleur_Ep'] - df_clean['Note_Pire_Ep']
display(df_clean.head(10))
 
 pourquoi la soustration et non la multiplication

Parce que je cherche un écart, c’est-à-dire une différence entre deux valeurs.

 -Cela permet d’identifier les séries ou produits dont la qualité varie beaucoup et ceux qui sont plus constants.

4) Analyse statistique de base

Min et Max montrent l’amplitude des écarts,
Moyenne et Médiane donnent une idée de la tendance générale

5) correlation entre variables numériques

- Cela montre si les notes hautes ou basses sont liées et si l’écart varie avec la note.

- La heatmap permet de repérer visuellement les relations fortes entre les variables
