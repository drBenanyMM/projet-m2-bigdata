# Projet M2 Big Data

Ce dépôt contient les travaux pratiques (`lab01` à `lab06`), les modules de traitement distribué, les tests et le rapport final du projet de Master 2 Big Data.

## Structure du projet

```text
projet-m2-bigdata/
├── data/               # Jeux de données bruts et traités (ignorés par Git)
│   └── README.md       # Instructions de téléchargement et description des schémas
├── notebooks/          # Notebooks Jupyter des travaux pratiques (lab01 à lab06)
├── reports/            # Rapport final (rapport.pdf) et graphiques générés (figures/)
├── results/            # Métriques d'évaluation et sorties expérimentales (metrics.csv)
├── src/                # Code source Python réutilisable (pipelines Spark, transformations)
├── tests/              # Tests unitaires et validation des pipelines
├── .gitignore          # Fichiers et dossiers exclus du suivi Git
├── requirements.txt    # Dépendances principales du projet
└── requirements-lock.txt # Versions exactes des paquets pour reproductibilité

```

## Prérequis système

* **Python :** `3.11`
* **Java (JDK) :** `17` (requis pour l'exécution du moteur Apache Spark)
* **Apache Spark :** `3.5.9`

## Installation et configuration

1. **Cloner le dépôt :**
```bash
git clone [https://github.com/drBenanyMM/projet-m2-bigdata.git](https://github.com/drBenanyMM/projet-m2-bigdata.git)
cd projet-m2-bigdata

```


2. **Créer et activer l'environnement virtuel :**
```bash
python3.11 -m venv .venv
source .venv/bin/activate

```


3. **Installer les dépendances :**
```bash
python -m pip install --upgrade pip
python -m pip install -r requirements-lock.txt

```
