# 📊 Analyse en Composantes Principales (PCA) avec méthode des puissances et déflation

Ce projet implémente une version personnalisée de l'**Analyse en Composantes Principales (PCA)** à partir de zéro, sans utiliser `scikit-learn`, en combinant :

- Centrage et calcul de la **matrice de covariance**
- **Méthode des puissances** pour obtenir le vecteur propre principal
- **Déflation** pour extraire les vecteurs propres suivants
- Projection des données sur les composantes principales
- Visualisation des résultats avec `matplotlib` et `seaborn`
📁 Contenu du projet
data

├── iris.txt

functions

├── deflation.py

notebook

├──principle_component_analysis_iris.ipynb

README.MD

[![Exécuter sur Binder](https://mybinder.org/badge_logo.svg)](https://hub.gesis.mybinder.org/user/zoubirchatti-01__linear-algebra-ws2un37q/doc/tree/03_principle_component_analysis_deflation/notebook/PCA_deflation%20.ipynb)
