# 🛒 Mini-Projet : Analyse de Paniers et Recommandations Produits

Ce projet a pour objectif d'analyser les données de ventes d'une enseigne de e-commerce afin d'identifier des associations d'articles (Market Basket Analysis). En utilisant les algorithmes **Apriori** et **FP-Growth**, nous extrayons des règles d'association pour formuler des recommandations métier concrètes (cross-selling, création de bundles, agencement des rayons).

## 🎯 Objectifs du Projet

- **Préparer et nettoyer** un jeu de données transactionnel.
- **Extraire des itemsets fréquents** et des règles d'association.
- **Interpréter les métriques clés** : Support, Confiance, et Lift.
- **Comparer les algorithmes** Apriori et FP-Growth (temps de calcul, efficacité).
- **Proposer des actions marketing** basées sur les données.

## 📂 Arborescence du Projet

```text
Mini-Projet_Analyse_Paniers/
│
├── data/                       # Dossier contenant les jeux de données bruts
│   ├── order_data.csv          # Petit dataset pour la phase de test (Partie 0)
│   └── Online_Retail.xlsx      # Dataset principal de transactions e-commerce
│
├── notebooks/                  # Scripts et Notebooks Jupyter
│   └── Mini-Projet_Apriori_FPGrowth.ipynb  # Code complet et documenté
│
├── livrables/                  # Livrables finaux
│   └── Rapport_Synthetique.pdf # Rapport d'analyse et recommandations métier
│
└── README.md                   # Description du projet
```

## 🛠️ Prérequis et Installation

Pour exécuter le code de ce projet, vous devez avoir Python installé ainsi que Jupyter Notebook ou utiliser Google Colab. 

Voici les bibliothèques requises :
- `pandas`
- `numpy`
- `matplotlib` / `seaborn`
- `apyori`
- `mlxtend`

Pour installer les dépendances via `pip`, exécutez la commande suivante dans votre terminal :

```bash
pip install pandas numpy matplotlib seaborn apyori mlxtend
```

## 🚀 Comment utiliser ce projet ?

1. **Cloner le dépôt** :
   ```bash
   git clone https://github.com/VOTRE_UTILISATEUR/Mini-Projet_Analyse_Paniers.git
   cd Mini-Projet_Analyse_Paniers
   ```
2. **Ajouter les données** :
   Placez vos fichiers `order_data.csv` et `Online Retail.xlsx` (ou `transaction_dataset.csv`) dans le dossier `data/`.
3. **Lancer le Notebook** :
   Ouvrez votre terminal, naviguez vers le dossier du projet et lancez Jupyter :
   ```bash
   jupyter notebook notebooks/Mini-Projet_Apriori_FPGrowth.ipynb
   ```
4. **Exécuter les cellules** de haut en bas pour voir la préparation des données, l'application d'Apriori, l'application de FP-Growth, et l'affichage des règles.

## 📊 Principales Conclusions

- **FP-Growth** s'est révélé beaucoup plus rapide et efficace qu'Apriori pour traiter notre dataset volumineux grâce à sa structure en arbre (FP-Tree) qui évite la génération de candidats multiples.
- Les règles filtrées (avec un **Lift > 1** et une **confiance élevée**) ont permis de proposer des stratégies de recommandations comme l'affichage "Les clients qui ont acheté ceci ont également acheté cela" sur la plateforme e-commerce.

## ✍️ Auteur
- EZ-ZAHRAOUI El-Mehdi      5 DDSI G:2
