# **Hackathon Airbus : Détection et Lecture des Matricules des Hélicoptères**

## **Description du projet**
Ce projet, réalisé dans le cadre d’un hackathon organisé par Airbus, vise à détecter et lire les matricules d’hélicoptères à partir d’images. Ces informations sont cruciales pour le suivi, l’identification et la gestion des appareils dans diverses situations opérationnelles.

La solution combine des techniques de vision par ordinateur et de reconnaissance de caractères pour offrir un pipeline complet et automatisé :

1. **Détection des matricules** : Utilisation du réseau de neurones YOLOv4 pour localiser avec précision les zones contenant les matricules dans les images.
2. **Lecture des matricules** : Extraction des zones détectées et reconnaissance des caractères à l’aide de la bibliothèque EasyOCR.

---

## **Technologies utilisées**
- **YOLOv4** : Modèle de détection d’objets performant, adapté à la localisation des zones contenant des matricules.
- **EasyOCR** : Bibliothèque pour la reconnaissance de caractères dans les images.
- **Python** : Langage principal utilisé pour développer le pipeline.
- **OpenCV** : Utilisé pour le prétraitement des images et la manipulation des zones détectées.

---

## **Étapes du pipeline**
1. **Prétraitement des images** :
   - Chargement des images brutes.
   - Redimensionnement et ajustement des contrastes pour optimiser la détection.

2. **Détection des matricules avec YOLOv4** :
   - Entraînement du modèle YOLOv4 avec un jeu de données annoté spécifique.
   - Détection des zones contenant les matricules.
  ![image](https://user-images.githubusercontent.com/91097262/168992165-5625077c-f2b7-4220-9232-e3793ea36026.png)

3. **Extraction des zones d’intérêt** :
   - Découpage des zones détectées pour les préparer à la reconnaissance optique.
  ![image](https://user-images.githubusercontent.com/91097262/168992387-7c0f971b-8a86-4e23-a4fe-a17b7e5d4063.png)
  ![image](https://user-images.githubusercontent.com/91097262/168992514-89ce498e-38f8-4e58-8aea-eb2c202f9528.png)

4. **Lecture des matricules avec EasyOCR** :
   - Application d’OCR sur les zones extraites pour obtenir les matricules sous forme de texte.
  ![image](https://user-images.githubusercontent.com/91097262/168992606-073f9224-b4e0-445d-9d6e-603bd44dae06.png)


5. **Validation des résultats** :
   - Comparaison des sorties avec les annotations pour évaluer les performances.
   - Amélioration continue via l’ajustement des hyperparamètres.

---

## **Améliorations possibles**
- Intégration de YOLOv8 pour une meilleure précision et rapidité.
- Enrichissement des données d’entraînement (divers éclairages, angles variés).
- Système de correction automatique des erreurs pour la lecture OCR.
- Déploiement d’une interface utilisateur interactive.
