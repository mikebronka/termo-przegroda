# Kalkulator termiczny stropu

Kalkulator przegrody dla domu jednorodzinnego: stropu pod nieogrzewanym strychem albo skosu poddasza użytkowego. Działa w przeglądarce, bez instalacji i bez serwera.

**[Otwórz kalkulator](https://mikebronka.github.io/termo-przegroda/)**

## Dwa tryby

- **Strop pod strychem:** pasy dolne wiązarów, strefa instalacyjna, ruszt CD (pusty lub wypełniony wełną), paroizolacja, płyty GK.
- **Poddasze użytkowe:** krokwie, membrana MWK, skos i ścianka kolankowa.

## Co liczy

- współczynnik U z korektą na szczeliny (PN-EN ISO 6946, metoda uproszczona),
- rozkład temperatury w przegrodzie, punkt rosy i temperaturę na paroizolacji,
- kondensację metodą Glasera dla warunków chwilowych (PN-EN ISO 13788),
- temperaturę przy kanałach rekuperacji i peszlach umieszczonych w izolacji,
- wysokość pomieszczenia w świetle albo wysokość skosu przy ściance i odległość do 1,4 m i 2,2 m (PN-ISO 9836),
- obciążenie pasa dolnego i straty ciepła.

## Widoki

- przekrój w skali z profilami temperatury i ciśnienia pary,
- model 3D (three.js) z płaszczyzną punktu rosy,
- porównanie wariantów i eksport raportu PDF na A4.

Warianty zapisują się w pamięci przeglądarki (localStorage). Każdy użytkownik ma swoje i nic nie trafia na serwer.

Wyniki są pomocnicze. Decyzje wykonawcze warto skonsultować z projektantem.

## Uruchomienie

Wystarczy otworzyć `index.html` w przeglądarce. Wersja online działa przez GitHub Pages (Settings → Pages → Deploy from a branch → `main` / root).
