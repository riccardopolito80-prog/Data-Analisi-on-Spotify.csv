# Data-Analisi-on-Spotify
🎵 Analisi dei Trend Musicali su Spotify
Questo progetto consiste in un'analisi esplorativa dei dati (EDA - Exploratory Data Analysis) su un dataset di brani musicali di Spotify. L'obiettivo è comprendere quali fattori influenzano la popolarità delle canzoni, analizzare l'evoluzione delle caratteristiche musicali nel tempo e identificare correlazioni tra le varie metriche audio.

📋 Indice
Descrizione del Progetto

Requisiti e Installazione

Struttura del Dataset

Workflow dell'Analisi

1. Pulizia dei Dati

2. Analisi dei Top Brani

3. Analisi Temporale

4. Correlazioni e Caratteristiche

Visualizzazioni Chiave

Come Eseguire

📖 Descrizione del Progetto
Il notebook analizza un file CSV (spoty_v.csv) contenente informazioni dettagliate sulle tracce più popolari su Spotify. Attraverso l'uso di librerie Python per la data science, il progetto esplora:

Quali sono le canzoni più ascoltate in assoluto.

Come è cambiata la "ballabilità" (danceability) della musica dal 2000 ad oggi.

La relazione tra velocità (BPM) ed energia dei brani.

Le correlazioni tra le diverse caratteristiche audio (es. acustica vs energia).

🛠 Requisiti e Installazione
Per eseguire questo notebook, è necessario avere installato Python e le seguenti librerie:

Bash

pip install pandas numpy matplotlib seaborn
Le librerie principali utilizzate sono:

Pandas: Per la manipolazione e pulizia dei dati.

NumPy: Per operazioni numeriche.

Matplotlib & Seaborn: Per la visualizzazione grafica dei dati.

Json & Datetime: Per la gestione di formati specifici.

📊 Struttura del Dataset
Il dataset include colonne quali:

track_name, artist(s)_name: Metadati del brano.

streams: Numero totale di ascolti (target principale dell'analisi).

released_year: Anno di pubblicazione.

bpm, key, mode: Caratteristiche tecniche musicali.

danceability_%, energy_%, acousticness_%, etc.: Metriche audio fornite da Spotify.

in_spotify_playlists, in_apple_charts: Presenza nelle classifiche delle piattaforme.

⚙️ Workflow dell'Analisi
1. Pulizia dei Dati (Data Cleaning)
Prima dell'analisi, il dataset viene sottoposto a un rigoroso processo di pulizia:

Gestione Encoding: Lettura del file con encoding latin-1 per gestire caratteri speciali.

Valori Nulli: Rimozione delle righe contenenti valori mancanti (NaN) nelle colonne chiave.

Duplicati: Eliminazione delle tracce duplicate per garantire l'unicità dei dati.

Correzione Tipi di Dato: Conversione della colonna streams da oggetto a numerico, gestendo errori di conversione.

Rimozione Outlier/Errori: Identificazione e rimozione manuale di righe con dati anomali o corrotti (es. indici 374, 574) che potrebbero falsare le statistiche.

2. Analisi dei Top Brani
Ordinamento del dataset per numero di streams per identificare la Top 10 delle canzoni più ascoltate.

3. Analisi Temporale
Raggruppamento dei dati per released_year per osservare come la media della Danceability è cambiata negli anni, con un focus specifico dal 2000 in poi.

4. Correlazioni e Caratteristiche
Utilizzo di Boxplot per analizzare la distribuzione della danceability e individuare outlier statistici.

Analisi bivariata tramite Scatterplot per vedere la relazione tra BPM ed Energia, distinguendo tra tonalità maggiori e minori.

Creazione di una Heatmap (matrice di correlazione) per visualizzare i legami tra tutte le variabili numeriche.

📈 Visualizzazioni Chiave
Il notebook genera i seguenti grafici:

Barplot: Top 10 canzoni per numero di Streams.

Lineplot: Evoluzione della "Ballabilità" nella musica dal 2000 ad oggi.

Boxplot: Distribuzione della Danceability (analisi degli outlier).

Scatterplot: Relazione tra Velocità (BPM) ed Energia (Energy %), con distinzione per tonalità (Mode).

Heatmap: Mappa di correlazione tra le variabili audio (es. acousticness vs energy).

🚀 Come Eseguire
Clona il repository o scarica i file.

Assicurati che il file spoty_v.csv sia nella stessa directory del notebook.

Apri il terminale o Anaconda Prompt.

Avvia Jupyter Notebook:

Bash

jupyter notebook
Apri il file Analisi file spotify trend.ipynb ed esegui le celle in sequenza.
