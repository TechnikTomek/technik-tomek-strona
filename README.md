# Technik Tomek – strona-wizytówka kanału YouTube

Jednostronicowa wizytówka kanału **[Technik Tomek](https://www.youtube.com/@TechnikTomek)**: neonowe logo, animowany equalizer w tle, licznik subskrypcji, najnowszy film, siatka ostatnich filmów, linki i kontakt.

🌐 **Strona:** https://techniktomek.github.io/technik-tomek-strona/

## Jak to działa
- Wszystko jest w jednym pliku `index.html` (HTML + CSS + JS, bez frameworków). Działa też po otwarciu dwuklikiem z dysku.
- Teksty, linki, e-mail i dane zapasowe zmieniasz w obiekcie `CONFIG` na początku sekcji `<script>`.
- Kolory zmieniasz w zmiennych CSS w `:root` (np. `--cyan`).
- Szczegółowa instrukcja jest w komentarzu na górze `index.html`.

## Dane z YouTube (opcjonalnie)
Bez klucza API strona pokazuje dane zapasowe wpisane ręcznie w `CONFIG.fallback`.
Z kluczem **YouTube Data API v3** pobiera na żywo subskrypcje, wyświetlenia i najnowsze filmy (z pamięcią podręczną na 1 godzinę).

> ⚠️ **Bezpieczeństwo:** to repozytorium jest publiczne. Pole `YOUTUBE_API_KEY` jest domyślnie **puste**.
> Wpisz klucz dopiero wtedy, gdy w Google Cloud Console ograniczysz go:
> - **Ograniczenia aplikacji →** Strony internetowe: `https://techniktomek.github.io/*`
> - **Ograniczenia interfejsów API →** tylko **YouTube Data API v3**
>
> Nigdy nie wpisuj do plików haseł ani tokenów.

## Aktualizacja strony
```bash
git add .
git commit -m "Opis zmiany"
git push
```
GitHub Pages przebuduje stronę automatycznie po około minucie.
