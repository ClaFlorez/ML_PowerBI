## 🧠 Expériences avec PyCaret + Power BI (notes personnelles)

### 🔍 Problème courant : erreur `target_variable`
**Erreur complète :**
```
AttributeError: 'Simple_Imputer' object has no attribute 'target_variable'
```

### ✅ Solution : utiliser versions compatibles
Dans Anaconda Prompt :
```bash
conda activate xgboost_bank
pip install pycaret==2.3.10 scikit-learn==1.0.2
```
Puis vérifier que Power BI pointe vers le bon environnement :
- **Fichier > Options > Scripts Python**
- Répertoire Python = `C:\Users\TON_UTILISATEUR\anaconda3\envs\xgboost_bank`

### ✅ Script Power BI corrigé
```python
from pycaret.classification import *
import pandas as pd

# dataset = fourni automatiquement par Power BI
dataset.columns = dataset.columns.str.strip()  # Nettoyage des noms de colonnes

setup(data=dataset, target='deposit', silent=True, html=False)

xgb = create_model('xgboost', verbose=False)
final_xgb = finalize_model(xgb)
predict_model(final_xgb)

dataset = pull()  # Résultat envoyé à Power BI
```

### ✅ Éviter erreurs de nom de colonne
Avant `setup()`, il est conseillé d'afficher les colonnes :
```python
print(dataset.columns.tolist())
```

### 🔍 Vérifier les versions dans Power BI
```python
import sklearn
import pycaret
print("Scikit-learn version:", sklearn.__version__)
print("PyCaret version:", pycaret.__version__)
```

---

## 🧯 Dépannage Power BI (quand il se bloque)

### 🧪 Tester un script minimal
```python
import pandas as pd

dataset.columns = dataset.columns.str.strip()
print("Colonnes disponibles :", dataset.columns.tolist())
dataset['TEST'] = 'ok'
```

### 🔁 Vider le cache de Power BI
Supprimer les dossiers temporaires :
```
C:\Users\TON_UTILISATEUR\AppData\Local\Microsoft\Power BI Desktop\AnalysisServicesWorkspaces\
```

### ⚙️ S'assurer que Python utilisé est correct
Dans **Fichier > Options > Scripts Python**, pointer vers :
```
C:\Users\TON_UTILISATEUR\anaconda3\envs\xgboost_bank\python.exe
```

---

Made with ❤️ pour apprendre à mon rythme.

