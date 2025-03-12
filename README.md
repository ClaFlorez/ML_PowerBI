# ML_PowerBI

# Problèmes de Versions de Python et Dépendances 

## Résumé

Ce document résume les problèmes rencontrés lors de la tentative d'installation de certaines dépendances Python, en particulier `numpy`, en raison d'incompatibilités de versions. Il détaille également le processus de recherche et de téléchargement de versions spécifiques de Python. 

## Problèmes Détectés

1.  **Incompatibilité de `numpy` avec Python 3.7 :** * Tentative d'installation de `numpy` version 2.2.3 dans un environnement avec Python 3.7.
    * `numpy` 2.2.3 requiert Python 3.10 ou supérieur, ce qui a entraîné des erreurs de "version introuvable". ❌
2.  **Conflits de dépendances après avoir forcé l'installation de numpy 2.2.3 dans l'environnement de base :** * Après avoir forcé l'installation de numpy 2.2.3 dans l'environnement de base, des conflits ont été générés avec des bibliothèques telles que contourpy, gensim et numba. 
    * Ces bibliothèques requièrent des versions antérieures de numpy. 
3.  **Problèmes avec le Lanceur Python (py.exe) :** ⚠️
    * Le lanceur Python (py.exe) n'a pas pu trouver d'installations spécifiques de Python (3.10), même lorsque d'autres versions (3.12) étaient présentes. ❓
    * Cela a empêché la création d'environnements virtuels spécifiques avec python 3.10. ⛔
4.  **Nécessité de Recherche et Téléchargement de Versions Spécifiques de Python :** ⬇️
    * Il a fallu rechercher et télécharger des versions spécifiques de Python (3.10) depuis le site Web officiel de Python ([python.org](https://www.python.org/downloads/)) pour assurer la compatibilité avec les dépendances requises. 

## Solutions Mises en Œuvre

1.  **Création d'Environnements Virtuels avec des Versions Compatibles :** ✨
    * L'importance de créer des environnements virtuels avec des versions de Python compatibles avec les dépendances requises a été soulignée.
    * Un environnement virtuel a été créé avec python 3.12, pour pouvoir installer numpy 2.2.3 sans conflits. ✅
2.  **Mise à Jour de Python :** 🆙
    * Il a été recommandé de mettre à jour vers la version la plus récente de Python (3.12) pour assurer la compatibilité avec les dernières versions des dépendances. 
3.  **Isolation des Dépendances :** ️
    * La nécessité d'isoler les dépendances de chaque projet dans des environnements virtuels distincts pour éviter les conflits a été mise en évidence. 

## Leçons Apprises

* Toujours vérifier la compatibilité des versions entre Python et les dépendances. 
* Utiliser des environnements virtuels pour isoler les projets et éviter les conflits de dépendances. 
* Maintenir Python et `pip` à jour. 
* Lorsque des conflits de dépendances surviennent, il est préférable de créer des environnements virtuels isolés, plutôt que de résoudre ces conflits dans l'environnement de base. 
* Le site Web officiel de Python est la source fiable pour télécharger des versions spécifiques de Python.


(myenv) C:\Users\H0PPR202\anaconda3\envs\myenv>conda list pycaret
# packages in environment at C:\Users\H0PPR202\anaconda3\envs\myenv:
#
# Name                    Version                   Build  Channel
pycaret                   2.0                      pypi_0    pypi

(myenv) C:\Users\H0PPR202\anaconda3\envs\myenv>






travail final en PowerBI
