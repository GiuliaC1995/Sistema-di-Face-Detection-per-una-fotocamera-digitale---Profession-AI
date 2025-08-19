# Sistema-di-Face-Detection-per-una-fotocamera-digitale---Profession-AI
Progetto di Computer Vision: Sistema di Face Detection per fotocamera digitale sviluppato in Python.

## Descrizione

Sistema di Computer Vision per rilevare volti in immagini acquisite da una fotocamera digitale. Il modello distingue tra immagini contenenti volti e immagini senza volti, ed è stato addestrato su un dataset personalizzato.

## Pipeline del Progetto

### Raccolta e Preprocessing dei Dati

- Dataset di volti: FaceScrub
- Dataset di non volti: STL-10
- Ridimensionamento, conversione in scala di grigi e normalizzazione delle immagini.
- Suddivisione in set di training e test con bilanciamento delle classi.

### Estrazione delle Feature

- Calcolo delle Histogram of Oriented Gradients (HOG) per ogni immagine.
- Standardizzazione dei dati con `StandardScaler`.

### Addestramento del Modello

- Support Vector Machine (SVM) con kernel RBF.
- Ricerca dei migliori iperparametri tramite `RandomizedSearchCV`.
- Salvataggio del modello con `joblib`.

### Rilevamento dei Volti

- Applicazione del modello addestrato su nuove immagini.
- Visualizzazione dei volti rilevati con bounding boxes.

## Librerie principali

- `OpenCV` – elaborazione e visualizzazione delle immagini.
- `scikit-image` – estrazione di feature HOG.
- `scikit-learn` – modello SVM, preprocessing, ricerca iperparametri.
- `NumPy` – gestione degli array.
- `Matplotlib` – visualizzazione dei risultati.
- `Joblib` – salvataggio del modello.

## Come usare il progetto

1. Aprire `Sistema_di_Face_Detection_per_una_fotocamera_digitale.ipynb` in Google Colab.
2. Eseguire le celle in ordine.
3. Caricare immagini di prova o collegare la fotocamera per testare il sistema.

## Autore

Giulia Calvino – Master in Data Science

