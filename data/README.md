# Données du projet

Les fichiers de données volumineux (`.csv`, `.parquet`, `.json`) placés dans ce dossier sont automatiquement ignorés par Git via `.gitignore`.

## Sources et instructions

* *À compléter : indiquer ici les liens de téléchargement des datasets utilisés et les commandes pour les placer dans `data/`.*

### 2. Configurer le kernel Jupyter et tester PySpark dans `lab01.ipynb`

1. **Enregistrer votre `.venv` comme kernel Jupyter** pour que VS Code le détecte automatiquement dans vos notebooks :
```bash
   python -m ipykernel install --user --name=projet-m2-bigdata --display-name "Python 3.11 (BigData .venv)"
```
2. **Ouvrir `notebooks/lab01.ipynb` dans VS Code** :
* En haut à droite du notebook, cliquez sur **Select Kernel** > **Jupyter Kernel...** > choisissez **Python 3.11 (BigData .venv)**.
* Créez une première cellule de code et exécutez ce test pour valider que Spark démarre bien sur votre Mac :


```python
from pyspark.sql import SparkSession

spark = (
    SparkSession.builder
    .appName("Lab01-Test")
    .master("local[*]")
    .getOrCreate()
)

print("Version Spark :", spark.version)

# Test rapide avec un DataFrame
data = [("Alice", 34), ("Bob", 45), ("Charlie", 29)]
df = spark.createDataFrame(data, ["nom", "age"])
df.show()

```


3. **Pousser la mise à jour de votre documentation sur GitHub** :
```bash
git add README.md data/README.md
git commit -m "docs: ajout de la documentation dans README.md et data/README.md"
git push

```