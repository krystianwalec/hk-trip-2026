# Hongkong 2026 — Planer podróży

Samowystarczalna strona HTML (po polsku) dla Krystiana i żony: Hongkong, wspinaczka outdoor **26–27 X**, potwierdzony wyjazd z rodziną do **Guilin–Yangshuo 29–31 X**, wesele w Sha Tin 1 XI.

## Pliki

- `index.html` — cała aplikacja (CSS + JS inline, Leaflet/OSM z CDN)
- `images/` — lokalne zdjęcia (ścieżki `images/*.jpg` — nie zamieniać na zdalne URL)
- `README.md` — ta instrukcja
- `.nojekyll` — pusty plik pomocniczy dla GitHub Pages

## Otwieranie lokalnie

1. Sklonuj lub skopiuj folder `hk-trip-planner`.
2. Otwórz `index.html` w przeglądarce:
   - dwuklik w Finderze / Eksploratorze, **albo**
   - z terminala: `open index.html` (macOS) / `xdg-open index.html` (Linux)
3. Mapa wymaga sieci (kafelki OpenStreetMap + Leaflet z unpkg). Zdjęcia ładują się **lokalnie** z `images/`.

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
git add index.html README.md .nojekyll images
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

Sztywny kręgosłup (wszędzie ten sam):

- 25 X przylot HKG
- **26–27 X wspinaczka** (plan osobno)
- **28 X wolny dzień** zwiedzania HK
- **29–31 X Guilin z rodziną — potwierdzone**
- 1 XI wesele · Regal Riverside, Sha Tin
- 2 XI wylot

Trzy opcje (A/B/C) różnią tylko **wieczór 25 X + pełny 28 X** (i lekki poranek 1 XI):

- A — klasyczne HK (Peak, Star Ferry, dim sum, rynki)
- B — Lantau / Big Buddha na 28 X
- C — baza bliżej Sha Tin / New Territories

Kalendarz, mapa Leaflet, jet lag (SEA→HKG), teaser zdjęć z `images/`.
