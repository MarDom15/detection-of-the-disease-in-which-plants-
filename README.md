
# 🌱 SmartPlantVision

SmartPlantVision est une application Android innovante qui aide les agriculteurs et les amateurs de jardinage à identifier rapidement les maladies des plantes. Basée sur l'apprentissage automatique et optimisée pour les environnements hors ligne, cette solution apporte des gains de temps et de productivité considérables en agriculture.

---

## 📚 Table des matières
- [🌟 Introduction](#-introduction)
- [🎯 Objectifs](#-objectifs)
- [✨ Caractéristiques principales](#-caractéristiques-principales)
- [🛠️ Technologies utilisées](#%EF%B8%8F-technologies-utilisées)
- [⚙️ Conditions préalables](#%EF%B8%8F-conditions-préalables)
- [🧪 Méthodologie](#-méthodologie)
- [📊 Résultats](#-résultats)
- [🚧 Limitations et défis](#-limitations-et-défis)
- [🔮 Améliorations futures](#-améliorations-futures)
- [👥 Équipe](#-équipe)
- [📖 Références](#-références)

---

## 🌟 Introduction

Les pertes agricoles dues aux maladies des plantes représentent un problème majeur, impactant les rendements et les revenus. 🌾 SmartPlantVision vise à réduire ces pertes en fournissant une méthode rapide, abordable et fiable pour détecter les maladies des plantes à partir d'images de feuilles.

L'application est spécifiquement conçue pour fonctionner hors ligne, rendant son utilisation possible même dans des zones rurales où l'accès à Internet est limité.

---

## 🎯 Objectifs

1. 🧬 Détecter les maladies des feuilles pour des cultures majeures :
   - **Pommes** : Black Rot, Cedar Apple Rust, Apple Scab.
   - **Pommes de terre** : Early Blight, Late Blight.
   - **Tomates** : Bacterial Spot, Leaf Mold, Tomato Mosaic Virus.
   - **Maïs** : Northern Corn Leaf Blight, Gray Leaf Spot, Rust.

2. 📱 Fournir une interface utilisateur simple et intuitive.
3. 🚜 Garantir une précision acceptable pour une détection fiable sur le terrain.
4. 🌐 Permettre une utilisation hors ligne.

---

## ✨ Caractéristiques principales

- **🤖 Reconnaissance des maladies via TensorFlow Lite** : Analyse d'images avec un réseau neuronal pour identifier les maladies des feuilles.
- **⚡ Modèle optimisé** : Basé sur `my_ssd_mobilenet50_v2_fpnlite`, offrant un compromis idéal entre vitesse et précision.
- **📱 Interface mobile ergonomique** : Application conçue avec Android Studio, compatible avec les smartphones modernes.
- **🎯 Précision et efficacité** :
  - Précision variant entre 66 % et 94 % pour différents scénarios.
  - Temps de traitement rapide grâce à TensorFlow Lite.
- **🔍 Analyse multi-maladies** : Identification simultanée de plusieurs maladies pour une seule culture.

---

## 🛠️ Technologies utilisées

### Frameworks et bibliothèques
- **TensorFlow 2.7** : Framework principal pour l'entraînement et l'optimisation du modèle de détection d'objets.
- **TensorFlow Lite** : Version légère de TensorFlow, intégrée dans l'application Android pour des performances optimales.
- **Object Detection API** : Utilisée pour configurer et entraîner les modèles de détection d'objets.

### Outils de développement
- **🖼️ LabelImg** : Utilisé pour labelliser les images d'entraînement avec précision.
- **💻 Android Studio** : Environnement de développement pour créer l'application Android.
- **📈 TensorBoard** : Pour évaluer et visualiser les performances du modèle pendant l'entraînement.

### Modèle d'apprentissage automatique
- **my_ssd_mobilenet50_v2_fpnlite** :
  - Résolution des images : 320x320 px.
  - Optimisé pour une balance entre la précision et la vitesse d'exécution.

### Données
- **📊 Dataset Kaggle** : Collection d'images avec des maladies variées, adaptées pour l'entraînement et les tests.
- **🎨 Techniques d'augmentation** :
  - Rotation.
  - Miroir horizontal.
  - Éclairage variable.

---

## ⚙️ Conditions préalables

### Pour utiliser l'application
- Un smartphone Android (minimum Android 8.0).
- 📸 Images des feuilles prises avec un fond neutre (idéalement blanc).
  
### Pour les développeurs
- Python 3.9 ou supérieur.
- TensorFlow et les dépendances associées.
- Android Studio pour le développement.

---

## 🧪 Méthodologie

1. **📂 Collecte et préparation des données** :
   - Sélection des images d'un dataset Kaggle contenant des maladies courantes.
   - Annotation manuelle des images avec des outils comme LabelImg.
   - Utilisation de 600 images par classe pour équilibrer le dataset.

2. **🏋️ Entraînement du modèle** :
   - Modèle basé sur `my_ssd_mobilenet50_v2_fpnlite`.
   - Configurations clés : résolution 320x320 px, batch size de 4, 50 000 itérations d'entraînement.
   - Évaluation régulière avec TensorBoard pour ajuster les hyperparamètres.

3. **📱 Développement de l'application Android** :
   - Intégration du modèle TensorFlow Lite exporté dans une application Android.
   - Optimisation pour un traitement rapide et une interface utilisateur intuitive.

4. **🧪 Tests et validation** :
   - Scénarios de tests variés pour évaluer les performances dans des conditions réelles.
   - Analyse des résultats pour identifier les forces et les limites.

---

## 📊 Résultats

### Précision par culture et scénario
- **🍎 Pommes** : 66-94 % selon la maladie.
- **🥔 Pommes de terre** : 67-88 %.
- **🍅 Tomates** : 75-92 %.
- **🌽 Maïs** : Non évalué en raison de problèmes techniques.

### ✅ Avantages observés
- Bonne performance pour des feuilles individuelles dans un fond neutre.
- Rapidité d'exécution grâce à TensorFlow Lite.

---

## 🚧 Limitations et défis

- **📉 Précision réduite pour les feuilles multiples dans une même image.**
- **🎨 Impact du fond** : Les performances diminuent lorsque le fond des images n'est pas neutre.
- **🗂️ Volume limité du dataset** : Seulement 600 images par maladie, ce qui limite la généralisation.

---

## 🔮 Améliorations futures

- **📈 Extension du dataset** : Ajouter plus d'images et diversifier les conditions de prise.
- **🖼️ Reconnaissance multi-feuilles** : Améliorer l'algorithme pour détecter plusieurs feuilles dans une seule image.
- **🌱 Ajout d'autres cultures** : Étendre l'application à d'autres types de plantes.
- **🤖 Automatisation agricole** : Intégration avec des robots agricoles pour surveiller automatiquement les champs.

---

## 👥 Équipe

- **👨‍💻 Darius Bonk**  
- **👨‍💻 Vipul Durgade**  
- **👨‍💻 Matial Domche**  
- **👨‍💻 Kiran Krishnakumar**  

**Encadrant** : Vitali Czymmek, Fachhochschule Westküste  
**📅 Date de soumission** : 30 janvier 2022

---

## 📖 Références

- Dataset utilisé : [New Plant Diseases Dataset](https://www.kaggle.com/datasets/vipoooool/new-plant-diseases-dataset)
- Tutoriel TensorFlow : [TensorFlow Object Detection API](https://tensorflow-object-detection-api-tutorial.readthedocs.io/)
- Documentation GitHub : [TensorFlow Models Repository](https://github.com/tensorflow/models)
