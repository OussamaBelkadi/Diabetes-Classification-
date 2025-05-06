Projet de Classification du Diabète

Ce projet implémente des modèles de classification pour prédire le diabète à partir de données médicales, en utilisant à la fois un réseau de neurones avec TensorFlow et une régression logistique implémentée à partir de zéro.
Table des matières

    Introduction
    Structure du projet
    Dataset
    Fonctionnalités
    Installation
    Utilisation
    Résultats
    Comparaison des modèles
    Conclusion

Introduction

Ce projet vise à prédire si un patient est diabétique ou non en se basant sur diverses mesures médicales. Deux approches sont implémentées et comparées :

    Un réseau de neurones utilisant TensorFlow/Keras
    Une régression logistique implémentée à partir de zéro avec des opérations matricielles

Structure du projet

├── devoir_classification.ipynb   # Notebook principal
├── diabetes.csv                  # Dataset
└── README.md                     # Documentation

Dataset

Le dataset utilisé est diabetes.csv, qui contient les attributs suivants :

    Pregnancies: Nombre de grossesses
    Glucose: Concentration de glucose plasmatique
    BloodPressure: Pression artérielle diastolique (mm Hg)
    SkinThickness: Épaisseur du pli cutané triceps (mm)
    Insulin: Insuline sérique à 2 heures (mu U/ml)
    BMI: Indice de masse corporelle
    DiabetesPedigreeFunction: Fonction de pedigree du diabète
    Age: Âge en années
    Outcome: Variable cible (0 = absence de diabète, 1 = présence de diabète)

Fonctionnalités
Préparation des données

    Importation des données depuis le fichier CSV
    Division des données en ensembles d'entraînement (80%) et de test (20%)

Réseau de neurones avec TensorFlow

    Architecture simple avec une couche de sortie à activation sigmoid
    Compilation avec optimiseur Adam et fonction de coût binary_crossentropy
    Entraînement sur plusieurs époques
    Visualisation de l'architecture du réseau
    Évaluation des performances (précision, rappel, F1-score)

Régression logistique à partir de zéro

    Implémentation manuelle avec des opérations matricielles
    Fonction sigmoid et descente de gradient
    Calcul des gradients et mise à jour des paramètres
    Évaluation des performances et comparaison avec le réseau de neurones

Installation

Pour exécuter ce projet, vous aurez besoin des bibliothèques Python suivantes :

bash

pip install numpy matplotlib pandas scikit-learn tensorflow

Utilisation

    Clonez ce dépôt
    Assurez-vous que le fichier diabetes.csv est dans le même répertoire que le notebook
    Ouvrez et exécutez le notebook devoir_classification.ipynb

bash

jupyter notebook devoir_classification.ipynb

Résultats

Les deux modèles atteignent des performances similaires, avec une précision d'environ 75-80% sur l'ensemble de test. Des métriques détaillées sont calculées, notamment :

    Matrice de confusion
    Rapport de classification (précision, rappel, F1-score)
    Graphiques d'évolution de la perte et de la précision

Comparaison des modèles

    Réseau de neurones : Facile à implémenter grâce à TensorFlow, très flexible pour des architectures plus complexes
    Régression logistique à partir de zéro : Permet une compréhension profonde de l'algorithme, contrôle total sur chaque étape du processus d'apprentissage

Pour ce problème simple de classification binaire, les deux approches donnent des résultats comparables car un réseau de neurones avec une seule couche (sans couches cachées) est mathématiquement équivalent à une régression logistique.
Conclusion

Ce projet montre l'implémentation et la comparaison de deux approches différentes pour la classification du diabète. Les résultats similaires entre les deux modèles confirment que pour des problèmes linéairement séparables, des modèles simples peuvent être aussi efficaces que des approches plus complexes.

Le développement de modèles à partir de zéro offre une compréhension approfondie des algorithmes sous-jacents, tandis que l'utilisation de bibliothèques comme TensorFlow permet un prototypage rapide et une scalabilité pour des problèmes plus complexes.

Projet réalisé dans le cadre d'un cours sur l'apprentissage automatique et la classification
