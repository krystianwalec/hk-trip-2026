# Hongkong 2026 — Planer podróży

Samowystarczalna strona HTML (po polsku) do porównania planu podróży Krystiana i żony: Hongkong, wspinaczka outdoor, wesele w Sha Tin oraz opcjonalny **plan rodziny** Guilin–Yangshuo.

## Pliki

- `index.html` — cała aplikacja (CSS + JS inline, Leaflet/OSM z CDN)
- `README.md` — ta instrukcja
- `.nojekyll` — pusty plik pomocniczy dla GitHub Pages

## Otwieranie lokalnie

1. Sklonuj lub skopiuj folder `hk-trip-planner`.
2. Otwórz `index.html` w przeglądarce:
   - dwuklik w Finderze / Eksploratorze, **albo**
   - z terminala: `open index.html` (macOS) / `xdg-open index.html` (Linux)
3. Mapa wymaga sieci (kafelki OpenStreetMap + Leaflet z unpkg). Zdjęcia ładują się z Wikimedia Commons / Unsplash.

Opcjonalnie lokalny serwer (przydatne, gdy przeglądarka blokuje część zasobów z `file://`):

```bash
cd hk-trip-planner
python3 -m http.server 8080
# potem http://localhost:8080
```

## GitHub Pages

1. Utwórz nowe repozytorium na GitHubie (np. `hk-trip-planner`).
2. Wgraj zawartość tego folderu do gałęzi `main` (root repo albo podfolder — patrz krok 4).

```bash
cd hk-trip-planner
git init
git add index.html README.md .nojekyll
git commit -m "Add Hong Kong 2026 trip planner"
git branch -M main
git remote add origin https://github.com/<USER>/<REPO>.git
git push -u origin main
```

3. W repo: **Settings → Pages → Build and deployment → Source: Deploy from a branch**.
4. Branch: `main`, folder: `/ (root)` — jeśli `index.html` leży w root repo.  
   Jeśli trzymasz pliki w podfolderze `docs/`, wybierz `/docs`.
5. Po 1–2 minutach strona będzie pod:
   `https://<USER>.github.io/<REPO>/`

Nie trzeba builda ani Node — wystarczy statyczny HTML.

## Zawartość strony

- Kalendarz 24 X – 2 XI 2026
- Trzy opcje itinerariów (zakładki) z 2–3 dniami wspinaczki
- Sekcja wspinaczki HK (Lion Rock, Kowloon Peak, Cape Collinson, Shek O, Clearwater Bay, Tung Lung Chau)
- Wesele 1 XI · Regal Riverside Hotel, Sha Tin
- Opcjonalny plan rodziny Guilin–Yangshuo (koszty, zdjęcia, dni)
- Mapa Leaflet z markerami Guilin + HK

To narzędzie decyzyjne — nie rezerwacja i nie sztywny rozkład jazdy.
