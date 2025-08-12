# Airbnb NYC 2019 – Market Analysis (Python/Pandas)

## Obiettivo
Analizzare il mercato Airbnb a New York (2019): prezzi, disponibilità, differenze per quartiere e tipo di stanza; individuare pattern utili per host e pricing.

## Dataset
- Fonte: Airbnb NYC 2019 (Inside Airbnb / Kaggle)
- Campi principali: `neighbourhood_group`, `neighbourhood`, `room_type`, `price`, `minimum_nights`, `availability_365`, `number_of_reviews`, `reviews_per_month`
- Nota: In `data/` è presente `AB_NYC_2019.csv`. Vedi istruzioni sotto.

## Metodi / Stack
- Python (Pandas, Matplotlib/Seaborn)
- Passi: cleaning → feature engineering → EDA → segmentazioni (quartiere, room_type) → insight

## Risultati chiave (esempi)
- **Manhattan** ha il prezzo medio più alto; **Bronx**/ **Staten Island** i più bassi
- Le **Private room** mostrano un **rapporto prezzo/occupazione** interessante in quartieri periferici
- L’indice semplice `price × availability_365` evidenzia zone con potenziale di ricavo costante

## Struttura repo
- `notebooks/airbnb_nyc_2019.ipynb` – analisi completa con grafici
- `data/` – `README.md` + `AB_NYC_2019.csv`
- `graphs/` – immagini principali
- `requirements.txt` – dipendenze minime

## Riproduzione
```bash
python -m venv venv
# Windows: venv\Scripts\activate
# macOS/Linux: source venv/bin/activate
pip install -r requirements.txt
jupyter notebook notebooks/airbnb_nyc_2019.ipynb
