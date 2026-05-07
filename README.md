
## Instalacja

### Wymagania
- Python 3.9+
- pip

### Instalacja zależności

```bash
pip install -r requirements.txt
```

### Uruchomienie

Notebooki uruchamiać **w kolejności** — każdy korzysta z artefaktów poprzedniego:

Kolejność: `01` → `02` → `03` → `04`

---

## Źródła danych

| Źródło | Co zawiera | Jak wczytywane |
|---|---|---|
| Pliki CSV (`dane/`) | Sklepy, POI, obszar, dzielnice | `pd.read_csv()` |
| AWS S3 (`dataplace-recruitment`) | Budynki (955k), populacja (450k) | `boto3` → pobierz raz do `data/raw/` |
| Snowflake (`RECRUITMENT_TRACES`) | ~414M sygnałów mobilnych (lipiec 2020) | SQL z agregacją na serwerze — nie pobierać całej tabeli |
.

---