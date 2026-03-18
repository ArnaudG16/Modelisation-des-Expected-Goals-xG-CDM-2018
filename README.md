# Projet XG (Expected Goals)

Ce projet vise à construire et analyser un modèle d'Expected Goals (xG) basé sur des données réelles de la Coupe du Monde 2018. L'objectif est d'estimer la probabilité qu'un tir se transforme en but en fonction de diverses caractéristiques spatiales et contextuelles.

## Description

Les *Expected Goals* sont une métrique statistique utilisée pour évaluer la qualité d'une occasion de but. 

Dans ce notebook, nous modélisons une variable binaire $Y$ :
- 1 : But
- 0 : Pas de but

Nous utilisons les données Open Data fournies par StatsBomb.

## imaux Méthodologie

### Modèle
Nous utilisons une Régression Logistique pour estimer la probabilité $P(Y=1|X)$ via la fonction sigmoïde :

$$P(Y=1|X) = \frac{1}{1 + e^{-(\beta_0 + \beta_1 X_1 + ... + \beta_n X_n)}}$$

### Features (Caractéristiques)
Les principales variables explicatives utilisées pour l'entraînement du modèle incluent :
- Distance au but
- Angle de tir
- Type de tir (ex: tête, pied)

## Installation et Prérequis

Pour exécuter ce notebook, vous aurez besoin des librairies Python suivantes :

```python
pip install statsbombpy mplsoccer scikit-learn pandas numpy matplotlib xgboost
