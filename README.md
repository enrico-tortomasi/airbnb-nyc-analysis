# Airbnb NYC 2019 – Market Analysis (Python/Pandas)
![Completed](https://img.shields.io/badge/Completed-✓-3CB371)


Analisi dei dati delle inserzioni Airbnb a New York City
con focus su prezzi, disponibilità e differenze tra quartieri.

---

## Dataset
- Fonte: [Airbnb NYC 2019 (Inside Airbnb / Kaggle](https://www.kaggle.com/datasets/dgomonov/new-york-city-airbnb-open-data)
- Campi principali: `neighbourhood_group`, `neighbourhood`, `room_type`, `price`, `minimum_nights`, `availability_365`, `number_of_reviews`, `reviews_per_month`
- Nota: In `data/` è presente `AB_NYC_2019.csv`. Vedi istruzioni sotto.

---

## Obiettivi dell’analisi

- Analizzare la distribuzione degli annunci per borough (Manhattan, Brooklyn, ecc.).
- Confrontare i prezzi medi tra quartieri.
- Valutare la relazione tra prezzo, tipo di alloggio e zona.
- Esplorare eventuali pattern tra disponibilità e prezzo.

---

## Strumenti utilizzati

- Python 3.x
- Librerie: `pandas`, `numpy`, `matplotlib`, `seaborn`
- Jupyter Notebook

---

## Workflow

1. Caricamento del dataset.
2. Pulizia:
   - rimozione outlier estremi di prezzo (es. > 500$ o valori incoerenti)
   - gestione valori nulli per quartiere / prezzo
   - eventuale filtraggio su categorie rilevanti.
3. Analisi:
   - conteggio annunci per borough e neighbourhood
   - analisi della distribuzione dei prezzi
   - confronto dei prezzi medi per borough e tipo di stanza.
4. Visualizzazioni:
   - istogrammi / boxplot dei prezzi
   - bar chart per numero annunci per borough
   - grafici combinati prezzo vs room_type / borough.

---

## Struttura repo

```
airbnb-nyc-analysis/
│
├─ data/
│   └─ airbnb_nyc.csv
│
├─ graphs/
│   ├─ (Barplot)Popolarità_media_per_prezzo_e_stanza.png
│   ├─ (Barplot)Quartieri_più_redditizi.png
│   ├─ (Barplot)Stanze_più_redditizie_per_zona.png
│   ├─ (Heatmap)Popolarità_media_per_prezzo_e_stanza.png
│   └─ (Heatmap)Stanze_più_redditizie_per_zona.png
│
├─ notebooks/
│   └─ airbnb_nyc_analysis.ipynb
│
└─ README.md

```
---

## Riproduzione

```
bash
python -m venv venv
# Windows: venv\Scripts\activate
# macOS/Linux: source venv/bin/activate
pip install -r requirements.txt
jupyter notebook notebooks/airbnb_nyc_2019.ipynb
```

---

## Insight principali

### **Manhattan** è il quartiere più redditizio, **Bronx**/ **Staten Island** i minori invece.

![Quartieri_più_redditizi](graphs/(Barplot)Quartieri_più_redditizi.png)

---

### Le **Entire Home/Apt** sono le piu' redditizie a **Manhattan** e **Brooklyn** con netto distacco, rispetto alle **Private room** che hanno un reddito inferiore ma ben distribuito in tutti i quartieri.

![Stanze_più_redditizie_per_zona](graphs/(Heatmap)Stanze_più_redditizie_per_zona.png)

---

### Le fasce di prezzo più popolari sono quelle che vanno da **51-150**, con un discreto aumento di popolarità per le **Private room** nella fascia **101-150**.

![Popolarità_media_per_prezzo_e_stanza](graphs/(Barplot)Popolarità_media_per_prezzo_e_stanza.png)

---

### Altri Insights:

- Le **Private room** mostrano un **rapporto prezzo/occupazione** interessante in quartieri periferici.
  
- L’indice semplice `price × availability_365` evidenzia zone con potenziale di ricavo costante.


---

## Come eseguire il notebook

Clonare il repository.

Installare le dipendenze (pandas, numpy, matplotlib, seaborn).

Aprire il notebook in Jupyter / VS Code.

Eseguire tutte le celle in ordine.
