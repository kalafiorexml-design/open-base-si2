# Katalog raportów (reports/)

Ten folder trzyma katalog i stronę listującą raporty **Open Base + SI²**.

## Pliki
- `catalog.json` — lista raportów (tytuł, ścieżka, okładka, tagi, opis).
- `index.html` — strona, która czyta `catalog.json` i renderuje karty.
- `riemann/` — przykładowy dział z raportami (Riemann, Λ, mollifier).

## Jak dodać nowy raport
1. Wrzuć raport HTML i zasoby (PNG/CSV) do odpowiedniego podfolderu (np. `reports/nowy_dzial/`).
2. Dopisz wpis w `catalog.json`, np.:
```json
{ "id":"id-unikalny", "title":"Mój raport", "path":"reports/nowy_dzial/moj.html",
  "cover":"reports/nowy_dzial/okladka.png", "data":["reports/nowy_dzial/dane.csv"],
  "tags":["tag1","tag2"], "summary":"Krótki opis", "updated":"2025-01-01T00:00:00Z" }
```
3. Commit & push. Strona `reports/index.html` pokaże nową kartę.
