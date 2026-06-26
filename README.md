# Domek w Rusinowie — strona

Statyczna strona-wizytówka domku letniskowego w Rusinowie. Czysty HTML — bez frameworków, bez build-u, bez zależności od zewnętrznych CDN poza czcionkami Google Fonts (jedyny zewnętrzny zasób ładowany przy wejściu). Ładuje się błyskawicznie i jest w pełni widoczna dla wyszukiwarek.

## Pliki

- `index.html` — cała strona (jedyny plik wejściowy, treść wpisana na stałe)
- `img/` — zoptymalizowane zdjęcia (hero, galeria wnętrza, plac zabaw, podgląd OG)
- `vercel.json` — nagłówki cache (zdjęcia zapamiętywane przez przeglądarkę na rok)
- `.gitignore` — wyklucza materiały robocze (`screenshots/`, `uploads/`) z publikacji

## Wdrożenie

### Vercel
1. Wrzuć projekt na GitHub.
2. W Vercel: **Add New… → Project → Import** repozytorium.
3. Framework Preset: **Other** · Build Command: *puste* · Output Directory: *puste* (root).
4. Deploy. Następnie w **Settings → Domains** dodaj `domekwrusinowie.pl`.

### Lokalnie
Otwórz `index.html` w przeglądarce — działa też bez serwera. Ewentualnie `npx serve`.

## Wydajność

- Treść wpisana na stałe w HTML — strona widoczna natychmiast i indeksowana przez Google.
- Zdjęcia przeskalowane i skompresowane (z ~10,8 MB do ~3,2 MB), galeria ładowana leniwie.
- Film (YouTube) i mapa Google ładują się dopiero po kliknięciu — zero zewnętrznych skryptów przy wejściu.
- Czcionki Google z `display=swap` (jedyny zewnętrzny zasób ładowany od razu).

## Uwagi

- Domena docelowa w meta/OG: `https://domekwrusinowie.pl`. Po zmianie domeny zaktualizuj adresy w `<head>` `index.html`.
