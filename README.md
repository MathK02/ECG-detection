# ECG Anomaly Detection using CNN & LSTM

Ce projet implémente un pipeline complet de détection d’anomalies dans des signaux ECG en utilisant deux types de réseaux de neurones profonds : un CNN 1D et un LSTM 1D.

## Description

- Chargement et fusion des fichiers `ECG5000_TRAIN.txt` et `ECG5000_TEST.txt`
- Normalisation des signaux ECG et préparation des tenseurs
- Entraînement de deux modèles (CNN et LSTM)
- Suivi des performances avec les courbes de loss et d'AUC
- Évaluation complète avec :
  - Matrice de confusion
  - Courbe ROC
  - Courbe précision-rappel
  - Histogramme des scores de probabilité

## Données

Les données ECG utilisées proviennent du dataset ECG5000 du UCR Time Series Classification Archive :  
http://www.timeseriesclassification.com/description.php?Dataset=ECG5000

Les fichiers doivent être nommés :
- `ECG5000_TRAIN.txt`
- `ECG5000_TEST.txt`

Ils peuvent être chargés via `files.upload()` dans un environnement Google Colab.

## Modèles

Deux modèles sont entraînés et comparés :
- **CNN 1D** : deux couches de convolution + max pooling adaptatif + dropout + couche fully connected
- **LSTM 1D** : une couche LSTM suivie d’un dropout et d’un classifieur linéaire

##  Résultats

Les performances des deux modèles sont présentées ci-dessous.

###  CNN 1D

- **Courbe du loss d’entraînement**  
  ![Loss CNN](images/loss_cnn.jpg)

- **Courbe ROC**  
  ![ROC CNN](images/roc_cnn.jpg)

- **Courbe précision-rappel**  
  ![PR CNN](images/pr_cnn.jpg)

- **Matrice de confusion**  
  ![Confusion CNN](images/confusion_cnn.jpg)

- **Histogramme des scores de probabilité par classe**  
  ![Histogramme CNN](images/histogram_cnn.jpg)

---

###  LSTM 1D

- **Courbe du loss d’entraînement**  
  ![Loss LSTM](images/loss_lstm.jpg)

- **Courbe ROC**  
  ![ROC LSTM](images/roc_lstm.jpg)

- **Courbe précision-rappel**  
  ![PR LSTM](images/pr_lstm.jpg)

- **Matrice de confusion**  
  ![Confusion LSTM](images/confusion_lstm.jpg)

- **Histogramme des scores de probabilité par classe**  
  ![Histogramme LSTM](images/histogram_lstm.jpg)


