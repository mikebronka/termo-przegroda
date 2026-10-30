# Kalkulator termiczny stropu

Kalkulator przegrody dla domu jednorodzinnego: stropu pod nieogrzewanym strychem albo skosu poddasza użytkowego. Działa w przeglądarce, bez instalacji i bez serwera.

**[Otwórz kalkulator](https://mikebronka.github.io/termo-przegroda/)**

![Widok ogólny kalkulatora](docs/widok-ogolny.png)

## Trzy tryby

- **Strop pod strychem:** belki stropu (pasy dolne wiązarów, jętki albo belki stropu drewnianego), strefa instalacyjna, ruszt CD (pusty lub wypełniony wełną), paroizolacja, płyty GK.
- **Poddasze użytkowe:** krokwie, membrana MWK, skos i ścianka kolankowa.
- **Sufit podwieszany:** ruszt CD (pojedynczy lub podwójny krzyżowy) pod wiązarami, jętkami, belkami albo stropem betonowym, rozkład płyt GK w jednej lub dwóch warstwach.

## Co liczy

- współczynnik U z korektą na szczeliny (PN-EN ISO 6946, metoda uproszczona),
- rozkład temperatury w przegrodzie, punkt rosy i temperaturę na paroizolacji,
- kondensację metodą Glasera dla warunków chwilowych (PN-EN ISO 13788),
- temperaturę przy kanałach rekuperacji i peszlach umieszczonych w izolacji,
- wysokość pomieszczenia w świetle albo wysokość skosu przy ściance i odległość do 1,4 m i 2,2 m (PN-ISO 9836),
- obciążenie belek i straty ciepła,
- opłacalność dodatkowej warstwy wełny: oszczędność na rachunkach dla wybranego źródła ciepła (pompa ciepła, gaz, prąd, pellet), koszt i czas zwrotu, także przy rosnących cenach energii.

## Widoki

**Model 3D** z rozsuniętymi warstwami i prześwietloną wełną: pasy wiązarów, kanały rekuperacji, peszle, ruszt z wieszakami, folia i płyty. Fioletowa płaszczyzna to miejsce, w którym przegroda ma temperaturę punktu rosy.

![Widok 3D przegrody](docs/widok-3d.png)

**Przekrój w skali** z profilem temperatury i ciśnienia pary. Tutaj wariant z folią w połowie izolacji: folia ma 0,4 °C przy punkcie rosy 9,3 °C, więc pod nią pojawia się kondensacja (czerwony odcinek).

![Przekrój z profilem temperatury i pary](docs/przekroj.png)

**Tryb poddasza użytkowego:** połać pod kątem, krokwie, membrana MWK, wełna pod krokwiami, ruszt i płyta GK.

![Poddasze użytkowe w 3D](docs/poddasze-3d.png)

**Wersja na telefon:** najważniejsze wyniki na górze, pod nimi widok 3D i warstwy.

<img src="docs/telefon.png" alt="Kalkulator na telefonie" width="320">

**Sufit podwieszany:** model 3D z belkami, wieszakami, profilami głównymi i nośnymi, folią i dwiema warstwami płyt (tu rozsunięte). Kalkulator sprawdza obciążenie wieszaka, rozstawy profili, to, czy krótkie krawędzie płyt wypadają na profilach, i mijanie styków w warstwie oraz między warstwami.

![Sufit podwieszany w 3D](docs/sufit-3d.png)

**Plan płyt** z długością każdego kawałka, profilami nośnymi i stykami drugiej warstwy. Do tego zestawienie materiałów: płyty, profile CD i UD, łączniki, wieszaki, wkręty, folia, taśmy i masa.

![Plan rozkładu płyt](docs/sufit-plan.png)

Pozostałe funkcje:

- przekrój w skali z profilami temperatury i ciśnienia pary,
- model 3D (three.js) z płaszczyzną punktu rosy,
- porównanie wariantów i eksport raportu PDF na A4.

Warianty zapisują się w pamięci przeglądarki (localStorage). Każdy użytkownik ma swoje i nic nie trafia na serwer.

Wyniki są pomocnicze. Decyzje wykonawcze warto skonsultować z projektantem.

## Uruchomienie

Wystarczy otworzyć `index.html` w przeglądarce. Wersja online działa przez GitHub Pages (Settings → Pages → Deploy from a branch → `main` / root).
