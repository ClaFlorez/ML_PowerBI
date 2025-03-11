# 🚀 Configuration d'un environnement de travail local avec Anaconda et PyCaret

## 🛠️ Prérequis
Avant de commencer, assurez-vous d'avoir **Anaconda** installé sur votre machine. Si ce n'est pas le cas, suivez les étapes ci-dessous.

---

## 📌 Étape 1 : Télécharger et installer Anaconda

🔗 [Téléchargez Anaconda](https://www.anaconda.com/products/individual) et suivez les instructions d'installation adaptées à votre système d'exploitation (Windows, macOS, Linux).  
Une fois l'installation terminée, ouvrez **Anaconda Prompt** (et non CMD classique) pour exécuter les commandes suivantes.

---

## 📌 Étape 2 : Créer un environnement Conda

Dans **Anaconda Prompt**, exécutez la commande suivante pour créer un environnement appelé `myenv` avec Python 3.7 :

```bash
conda create --name myenv python=3.7
```
✅ Une fois l'installation terminée, Conda vous demandera de confirmer. Tapez `y` puis **Entrée**.

---

## 📌 Étape 3 : Activer l’environnement

Activez l’environnement `myenv` avec la commande :

```bash
conda activate myenv
```
⚠️ Si cette commande ne fonctionne pas, essayez :
```bash
source activate myenv  # Pour certains systèmes
```

---

## 📌 Étape 4 : Installer PyCaret

Avec l’environnement `myenv` activé, installez PyCaret en exécutant :

```bash
pip install pycaret==2.0
```
🔄 Si l’installation échoue, essayez d’abord de mettre à jour `pip` :

```bash
pip install --upgrade pip
```
Puis réessayez d’installer PyCaret.

---

## 📌 Étape 5 : Configurer Python pour Power BI

Dans **Power BI**, allez dans :
1. **Fichier** > **Options et paramètres** > **Options**
2. Sélectionnez **Scripts Python**
3. Choisissez le chemin Python de votre environnement `myenv` (généralement situé dans `C:\Users\VotreNom\anaconda3\envs\myenv\python.exe`)

---

## 🎯 Résumé des commandes

```bash
# 1️⃣ Installer Anaconda (si ce n’est pas déjà fait)
# 2️⃣ Créer un environnement Conda
conda create --name myenv python=3.7

# 3️⃣ Activer l’environnement
conda activate myenv

# 4️⃣ Installer PyCaret
pip install pycaret==2.0
```

💡 **Astuce** : Si vous rencontrez des erreurs, copiez-les ici pour obtenir de l'aide ! 🚀

