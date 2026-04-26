# Analyse de Sentiment sur les Avis de Films

## Pipeline complet de Text Mining et Classification

## 1. Contexte du projet

Les plateformes de streaming et les sites de e-commerce génèrent chaque jour des millions d'avis de clients.  
L'analyse automatique de ces avis permet aux entreprises de mieux comprendre les retours des utilisateurs, d'identifier les avis positifs et négatifs, et d'améliorer leurs services.

Dans ce mini-projet, nous construisons un pipeline complet de traitement du langage naturel, appelé aussi NLP, appliqué à la classification d'avis de films.

Le but est de prédire si un avis est **positif** ou **négatif** à partir de son contenu textuel.

---

## 2. Objectif du projet

L'objectif principal de ce projet est de construire un pipeline complet de Text Mining comprenant les étapes suivantes :

1. Exploration des données
2. Prétraitement du texte
3. Vectorisation des avis
4. Réduction de dimension avec LSI
5. Classification des avis
6. Évaluation des performances
7. Comparaison entre Bag-of-Words et TF-IDF

---

## 3. Dataset utilisé

Le dataset utilisé dans ce projet est :

Dataset_IMDB_Avis_Films.csv

Ce fichier contient des avis de films annotés selon deux classes :

- positive : avis positif
- 
egative : avis négatif

Le dataset permet donc d'entraîner un modèle de classification supervisée pour prédire automatiquement le sentiment d'un avis.

---

## 4. Structure du projet

Le projet contient les fichiers suivants :

- Analyse_Sentiment_Avis_Films.ipynb : notebook Jupyter contenant tout le pipeline du projet
- Dataset_IMDB_Avis_Films.csv : dataset utilisé pour l'analyse de sentiment
- README.md : présentation générale du projet

---

## 5. Étapes réalisées dans le notebook

### 5.1 Exploration des données

Dans cette partie, nous analysons le dataset afin de mieux comprendre sa structure.

Les analyses réalisées sont :

- Chargement du dataset
- Affichage des premières lignes
- Vérification des colonnes disponibles
- Analyse de la distribution des classes positives et négatives
- Étude de la longueur des avis
- Visualisation des données avec des graphiques
- Analyse des mots les plus fréquents

---

### 5.2 Prétraitement du texte

Le prétraitement permet de nettoyer les avis avant de les utiliser dans les modèles de machine learning.

Les traitements appliqués sont :

- Suppression des balises HTML
- Suppression de la ponctuation
- Suppression des chiffres
- Mise en minuscules
- Suppression des espaces inutiles
- Tokenisation
- Suppression des stopwords
- Stemming et/ou lemmatisation

---

### 5.3 Vectorisation des textes

Les modèles de machine learning ne comprennent pas directement le texte.  
Il faut donc transformer les avis en représentations numériques.

Deux méthodes de vectorisation sont utilisées :

#### Bag-of-Words

La méthode Bag-of-Words représente les textes selon la fréquence d'apparition des mots.

#### TF-IDF

La méthode TF-IDF donne plus d'importance aux mots qui sont fréquents dans un document mais moins fréquents dans l'ensemble du corpus.

---

### 5.4 Réduction de dimension avec LSI

Après la vectorisation, les matrices obtenues peuvent être très grandes.  
Nous appliquons donc une réduction de dimension avec LSI, Latent Semantic Indexing.

Cette étape permet de :

- Réduire la taille de l'espace vectoriel
- Réduire le bruit
- Améliorer l'efficacité du modèle
- Garder les informations les plus importantes

---

### 5.5 Modélisation

Un modèle de classification est entraîné pour prédire le sentiment des avis.

Le modèle utilisé dans ce projet est :

- Régression logistique

Le modèle est appliqué séparément sur :

- Les données vectorisées avec Bag-of-Words
- Les données vectorisées avec TF-IDF

---

### 5.6 Évaluation des performances

Les performances du modèle sont évaluées avec les métriques suivantes :

- Accuracy
- Precision
- Recall
- F1-score

Un tableau récapitulatif permet de comparer les résultats obtenus avec Bag-of-Words et TF-IDF.

---

## 6. Question d'analyse

La question principale traitée dans le notebook est :

**Quelle vectorisation donne de meilleurs résultats entre Bag-of-Words et TF-IDF ? Pourquoi ?**

La réponse est donnée directement dans le notebook à partir des résultats obtenus.

En général, TF-IDF peut donner de meilleurs résultats car il prend en compte l'importance réelle des mots dans les documents.  
Contrairement au Bag-of-Words, il ne se limite pas uniquement au nombre d'apparitions des mots.

---

## 7. Bibliothèques utilisées

Les principales bibliothèques utilisées dans ce projet sont :

- pandas
- numpy
- matplotlib
- seaborn
- nltk
- scikit-learn
- wordcloud

---

## 8. Comment exécuter le projet

Pour exécuter ce projet :

1. Ouvrir le fichier Analyse_Sentiment_Avis_Films.ipynb avec Jupyter Notebook
2. Vérifier que le fichier Dataset_IMDB_Avis_Films.csv est dans le même dossier que le notebook
3. Exécuter les cellules du notebook dans l'ordre

---

## 9. Auteur

Projet réalisé par : **Rania Oulmidi**

---

## 10. Conclusion

Ce projet présente un pipeline complet de Text Mining appliqué à l'analyse de sentiment des avis de films.  
Il permet de comprendre les étapes essentielles d'un projet NLP, depuis l'exploration des données jusqu'à l'évaluation d'un modèle de classification.
