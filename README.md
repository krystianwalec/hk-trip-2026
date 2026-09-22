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

- 25 X przylot HKG · check-in **Dorsett Kai Tak**
- **26–27 X wspinaczka** — Beacon Hill (26) + Monkey Buttress / Central Crags / Devil’s Peak (27); Tung Lung weekend-only · baza Dorsett
- **28 X wolny dzień** zwiedzania HK
- **29–31 X Guilin z rodziną — potwierdzone** (12 os. · ~1366 HKD/os. ≈ 750 PLN · od rodziny / organizatorów)
- **31 X–2 XI Alva Hotel By Royal** (Sha Tin; check-out Krystiana 2 XI rano)
- 1 XI wesele · Regal Riverside, Sha Tin
- 2 XI wylot

Trzy opcje (A/B/C) różnią tylko **wieczór 25 X + pełny 28 X** (i lekki poranek 1 XI):

- A — klasyczne HK (Peak, Star Ferry, dim sum, rynki)
- B — Lantau / Big Buddha na 28 X
- C — baza bliżej Sha Tin / New Territories

Kalendarz, mapa Leaflet, jet lag (SEA→HKG), teaser zdjęć z `images/`.

Sekcja **Do załatwienia przed wyjazdem** (`#przed-wyjazdem`): otwarte checklisty — Global Entry, płatności HK+Chiny, roaming/eSIM; pobocznie pociągi HK↔Guilin (TBD).

Sekcja **Plan wspinania 26–27 X** (baza Dorsett Kai Tak):
- Pon 26 X: Beacon Hill Main Wall (taxi Lung Yan Rd)
- Wt 27 X: Monkey Buttress **lub** Central Crags; backup Devil’s Peak
- Tung Lung Chau: idealne, ale kaito zwykle tylko sob/niedz/święta — nie primary Mon–Tue
- Markery mapy: Beacon Hill, Monkey Buttress, Central Crags, Devil’s Peak, Tung Lung, Sam Ka Tsuen pier
- Źródło: [Grok share climbing](https://grok.com/share/bGVnYWN5_c5985378-7d77-401e-8a2d-12fa2d8e5252)

Sekcja **Hotele (my + rodzina)** (wspólne, potwierdzone rezerwacje):
- Dorsett Kai Tak (Kowloon City / 43 Shing Kai Road) · 25–29 X 2026 · mapa ≈ 22.3268, 114.1955 · baza wspinania
- Alva Hotel By Royal (1 Yuen Hong St, Sha Tin) · Krystian i żona 31 X – 2 XI 2026 (rodzina może zostać do 11 XI) · mapa ≈ 22.3865, 114.2088
- Przepływ: Dorsett → Guilin 29–31 X → Alva po powrocie; Alva blisko wesela (Regal Riverside, Sha Tin).

Sekcja **Guilin – Yangshuo 29–31 X** (plan i koszty **od rodziny / organizatorów**):
- Grupa: **12 osób** · 3 dni / 2 noce
- **Dzień 1 (29 X, Guilin):** przylot → Wzgórze Trąby Słonia (Elephant Trunk, wstęp wolny) → Guihai Qinglan / Czyste Niebo nad Jeziorem Guilin (50) → wieczór wolny: Pagody Słońca i Księżyca + Aleja Wschód-Zachód (Dongxi) → noc **Guilin Atour Hotel** (Superior twin + śniadanie)
- **Dzień 2 (30 X):** rejs Li Jiang **4★ ~4 h** (główne atrakcje rzeki) → stary Xingping → pejzaż z banknotu 20 ¥ → Impression Liu Sanjie B2 → noc **Yangshuo Atour Hotel** (Superior twin + śniadanie; okolica Ten-Mile Gallery)
- **Dzień 3 (31 X):** tratwy bambusowe Yulong (4-os.) → Ten-Mile Gallery → Moon Hill (jedyna skała w oknie Guilin) → Xiangong / Xianggong → transfer na dworzec i powrót
- Koszty pakietu (HKD, 12 os.): bilety 8820 (m.in. Guihai 50×12=600, rejs 360×12=4320, Liu Sanjie B2 195×12=2340, Yulong 280×3 tratwy=840, Xianggong 60×12=720) + hotele 4680 (Guilin Atour 350×6=2100, Yangshuo Atour 430×6=2580) + van 15 miejsc 2700 + obsługa 200 → **16 400** razem · **~1366 HKD/os. ≈ ~750 PLN** / 3 dni
- **Nie wliczone:** pociągi HK ↔ Guilin, posiłki poza śniadaniem. Pociągi do ustalenia w tym tygodniu (pamiętane ~£80 w obie strony).
- Hotele w Guilin: **Guilin Atour Hotel** (29 X) i **Yangshuo Atour Hotel** (30 X, okolica Ten-Mile Gallery) · Superior twin + śniadanie · 6 pokoi
