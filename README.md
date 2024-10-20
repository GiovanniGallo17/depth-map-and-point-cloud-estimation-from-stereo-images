
# Depth Map and Point Cloud Estimation

Questo codice implementa un modello basato su rete neurale U-Net per stimare mappe di profondità da immagini stereoscopiche. Le mappe di profondità stimate vengono utilizzate per generare point cloud 3D.

## Requisiti

Prima di eseguire il codice, assicurati di avere:

1. Una GPU compatibile con CUDA per accelerare l'addestramento del modello.
2. **Jupyter Notebook** o **Jupyter Lab** per eseguire il notebook `.ipynb`.

## Struttura del Progetto

Assicurati di avere le seguenti cartelle e file organizzati correttamente:

```
├── depthMap_pointCloud_estimation.ipynb  # Notebook principale
├── immagini/                            # Cartella con le immagini di input
├── mappe_profondità/                    # Cartella con le mappe di profondità ground truth
└── requirements.txt                     # File delle dipendenze (opzionale)
```

- **immagini/**: cartella contenente le immagini di input.
- **mappe_profondità/**: cartella contenente le mappe di profondità ground truth corrispondenti alle immagini.

## Esecuzione del Codice

### 1. Preparazione del Dataset

Organizza il dataset nelle due cartelle:

- `immagini/`: conterrà le immagini RGB (o in scala di grigi) di input.
- `mappe_profondità/`: conterrà le mappe di profondità corrispondenti, che serviranno come ground truth durante l'addestramento.

### 2. Apertura del Notebook

Per avviare il processo:

1. Apri il terminale e lancia Jupyter Notebook o Jupyter Lab:

```bash
jupyter notebook
```

2. Apri il file `depthMap_pointCloud_estimation.ipynb` dal browser.

### 3. Esecuzione del Notebook

Una volta aperto il notebook, eseguire il codice una cella alla volta in ordine.

### 4. Salvataggio e Visualizzazione dei Risultati

- Le **mappe di profondità stimate** possono essere salvate come immagini.
- Le **point cloud** possono essere salvate in formato `.ply` o `.pcd` e visualizzate utilizzando Open3D o un visualizzatore 3D esterno.

### 5. Fine dell'Esecuzione

Al termine dell'addestramento e della valutazione, puoi salvare il modello addestrato per futuri utilizzi o testarlo su nuovi dati di input. 

---

### Note

- **GPU**: È altamente consigliato eseguire il codice su una GPU per migliorare le prestazioni, specialmente durante l'addestramento.
