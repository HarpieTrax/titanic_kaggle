# 🛳️ Projet Titanic - Kaggle  
## Auteur : Paul Lachaise

Ce notebook contient ma solution pour le **défi Titanic** sur [Kaggle](https://www.kaggle.com/competitions/titanic), un cas d’étude classique utilisé pour introduire les fondamentaux de la data science et du machine learning supervisé.

## Contenu du dossier `Titanic_kaggle/`

Ce dossier contient l’ensemble du projet :

``` yaml
Titanic_kaggle/
├── data/
│ ├── train.csv # Données d'entraînement
│ ├── test.csv # Données de test
│ ├── gender_submission.csv # Fichier de base fourni par Kaggle
│ └── submission.csv # Fichier généré automatiquement par mon code pour soumission Kaggle
├── model.ipynb # Notebook principal avec tout mon code et les explications
└── random_forest_optimized.joblib # Modèle sauvegardé entraîné avec Random Forest
```

## Accès au code

Tout le code est contenu dans le fichier `model.ipynb`. Ce notebook est structuré en trois grandes parties :

### 1. Présentation du défi Titanic  
- Objectif du Kaggle  
- Explication des fichiers d’entrée  
- Description des variables 
- Analyse exploratoire des données

### 2. Data Preparation & Feature Engineering  
- Nettoyage des données  
- Traitement des valeurs manquantes  
- Transformation des variables avec **pandas**

### 3. Modélisation et prédiction  
- Entraînement de 3 modèles  
- Optimisation des hyperparamètres de **Random Forest**
- Génération automatique du fichier `submission.csv`


## Soumission Kaggle

À la fin de l’exécution du notebook `model.ipynb`, un fichier `submission.csv` est généré automatiquement.  
C’est ce fichier qu’il faut **soumettre sur Kaggle** pour obtenir votre **score de prédiction**.

## Setup

Le projet est configuré avec le gestionnaire de dépendances moderne [`uv`](https://docs.astral.sh/uv/), qui prend également en charge la création d'environnements virtuels. Les dépendances sont listées dans les fichiers `pyproject.toml` et `uv.lock`.  

Deux options s'offrent alors à vous pour exécuter ce projet :

### Option 1 — Installation locale (avec VS Code classique)

Si vous préférez travailler en local, il vous suffit de cloner ce dépôt et d’utiliser `uv` pour gérer l’environnement et installer les dépendances.

Installez `uv`

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

>Si l’installation de `uv` échoue ou si vous rencontrez des problèmes avec votre environnement virtuel, vous pouvez exécuter le projet dans le cloud via **GitHub Codespaces** (voir Option 2).

Installez ensuite toutes les dépendances définies dans `pyproject.toml`

```bash
uv sync
```

Activez enfin l’environnement virtuel

```bash
source .venv/bin/activate
```

### Option 2 — Exécution dans GitHub Codespaces (cloud, aucune installation requise)

Si vous ne souhaitez rien installer localement, vous pouvez tout exécuter dans le navigateur grâce à **GitHub Codespaces**.

1. Accédez au dépôt GitHub du projet.
3. Cliquez sur le bouton vert Code en haut à droite → "Create codespace" 
4. Une fois le Codespace lancé, ouvrez le terminal intégré et exécutez les mêmes commandes que pour l’installation locale expliqué juste au dessus.

---

Une fois l’environnement activé, vous êtes prêt à lancer le notebook `model.ipynb` et à explorer l’analyse ainsi que les prédictions du modèle.