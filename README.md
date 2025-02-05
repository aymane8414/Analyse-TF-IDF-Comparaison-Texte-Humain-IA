# Analyse de la Différence entre Textes Humains et Générés par l'IA avec TF-IDF

## Description

Ce projet utilise la méthode TF-IDF pour analyser la différence entre les textes écrits par des humains et ceux générés par l'IA. L'objectif est d'identifier et de comparer les caractéristiques linguistiques de ces deux types de texte.


## Données

Les données utilisées proviennent du **DAIGT Proper Train Dataset**, un jeu de données disponible sur [Kaggle](https://www.kaggle.com/datasets/thedrcat/daigt-proper-train-dataset). Ce jeu de données contient plus de 300 000 échantillons de texte classifiés comme générés par l'IA ou écrits par des humains.


## Méthodologie

1. **Prétraitement des Données :**
   Le nettoyage des données a consisté à enlever les caractères spéciaux, les chiffres et à normaliser le texte en minuscules. Ensuite, un stemming a été appliqué pour réduire les mots à leur racine, ce qui est particulièrement utile pour la vectorisation TF-IDF.

2. **Utilisation de TF-IDF :**
   Pour vectoriser les textes, le modèle TF-IDF a été utilisé. Ce modèle prend en compte la fréquence des termes dans un texte et leur rareté dans l'ensemble du corpus. Cependant, il est important de noter que TF-IDF ne capture pas le contexte des mots dans une phrase, ce qui limite sa capacité à distinguer les nuances du langage humain par rapport à l'IA.

3. **Analyse Statistique :**
   Une première analyse a permis de comparer la lisibilité des textes humains et générés par IA, en utilisant des indices comme le **Flesch Score** et le **Grade Level**. Il a été observé que les textes générés par l'IA sont généralement plus difficiles à lire que ceux rédigés par les humains. De plus, les textes IA présentent moins de variabilité, ce qui suggère que l'IA tend à générer des phrases d'une complexité similaire.

4. **Visualisation des Résultats :**
   La réduction de dimensionnalité a été utilisée pour visualiser les différences entre les textes à l'aide de PCA et de t-SNE. Ces visualisations ont montré que les textes IA ont tendance à être plus concentrés, tandis que les textes humains sont plus dispersés. Ce phénomène pourrait être lié à l'approche plus homogène adoptée par l'IA dans la génération de texte.
   
## Outils :
- Python (pandas, numpy, scikit-learn)
- TF-IDF
- Jupyter Notebook
  
## Résultats
1. **Lisibilité :**
   - Les textes IA sont moins lisibles, avec des scores de lisibilité plus faibles.

2. **Variabilité :**
   - Les textes humains présentent une plus grande variabilité en complexité et style.

3. **Visualisation des Données :**
   - Les textes IA apparaissent plus regroupés, indiquant une similarité accrue.
   - Les textes humains sont plus dispersés, reflétant une plus grande diversité.

## Discussion

L'utilisation de l'algorithme TF-IDF pour vectoriser les textes a permis de réaliser une première analyse, mais il aurait été plus pertinent d'explorer des modèles comme BERT. Contrairement à TF-IDF, qui ne prend en compte que la fréquence des mots, BERT capture le contexte des mots et leur relation dans une phrase, ce qui permettrait une meilleure distinction entre les textes humains et ceux générés par l'IA.

BERT est plus coûteux en termes de calcul, mais aurait offert des résultats plus précis, notamment en saisissant les nuances du langage. L'analyse du contexte des mots aurait donc enrichi les résultats et permis de mieux capturer les caractéristiques stylistiques des textes générés par l'IA et ceux écrits par des humains.

## Conclusion

L'utilisation de TF-IDF a permis de faire une première analyse, mais un modèle comme BERT serait plus adapté. BERT comprend le contexte des mots, ce qui aiderait à mieux distinguer les textes humains de ceux générés par l'IA, contrairement à TF-IDF qui ne se base que sur la fréquence des mots.

Ce projet a montré que les textes humains et IA diffèrent en termes de lisibilité et de variabilité stylistique. Toutefois, l'utilisation de modèles comme BERT offrirait des résultats plus précis.

Pour aller plus loin, il serait intéressant d'explorer des méthodes d'apprentissage supervisé ou non supervisé, surtout avec les IA qui commencent à imiter le style humain.
