
# 📊 Analyse de Sentiments Multilingue (FR/EN) et Emojis

Ce projet compare trois approches de Traitement du Langage Naturel (NLP) pour classifier les sentiments de critiques issues des réseaux sociaux. Le dataset est particulier car il mélange le **français**, l'**anglais** et les **emojis** au sein des mêmes phrases.

## 🚀 Objectif du Projet

L'objectif est de déterminer quelle méthode est la plus robuste pour traiter des données "bruitées" (social media) et bilingues parmi :

1. **L'Approche Lexicale** : Utilisation de **VADER** (Valence Aware Dictionary and sEntiment Reasoner).
2. **Le Machine Learning Classique** : Modèle **Naive Bayes** avec vectorisation **TF-IDF**.
3. **Le Deep Learning** : Réseau de neurones récurrents de type **LSTM** (Long Short-Term Memory).

## 🛠️ Installation et Prérequis

Le projet est développé en Python 3. Les bibliothèques suivantes sont nécessaires :

```bash
pip install pandas numpy scikit-learn tensorflow vaderSentiment matplotlib seaborn

```

## 📂 Structure du Dataset

Le fichier `social_media_reviews_dataset.csv` contient :

* `text` : Le contenu de la critique (mélange FR/EN + Emojis).
* `sentiment` : La classe cible (positive, negative, neutral).

## 🧠 Méthodologie et Modèles

### 1. Préparation des données

Nettoyage du texte via Regex pour supprimer les URLs, les mentions (@) et normaliser les espaces, tout en conservant les emojis pour l'analyse.

### 2. Modèles testés

* **VADER** : Analyse basée sur un lexique prédéfini de mots et d'emojis. Très efficace pour les expressions anglaises et les smileys.
* **Naive Bayes** : Modèle probabiliste qui apprend l'importance des mots (TF-IDF). Rapide et efficace sur les mots-clés bilingues.
* **LSTM** : Modèle de Deep Learning capable de comprendre l'ordre des mots et le contexte global de la phrase.

## 📈 Résultats et Comparaison

Les performances sont évaluées à l'aide d'une matrice de confusion et d'un rapport de classification (Précision, Recall, F1-Score).

*Exemple de visualisation des résultats :*

## 💻 Utilisation

Pour tester une prédiction personnalisée, lancez la cellule d'interaction à la fin du notebook :

```python
saisie = input("Entrez votre commentaire : ")
faire_une_prediction(saisie)

```

---

