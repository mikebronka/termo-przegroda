# Jak liczy kalkulator

Ta strona opisuje wzory i założenia. Wszystkie obliczenia są jednowymiarowe (prostopadle do przegrody) i dotyczą stanu ustalonego przy warunkach wpisanych w panelu.

## Opór cieplny i współczynnik U

Opór warstwy jednorodnej: **R = d / λ** (d w metrach, λ w W/mK).

**Warstwy niejednorodne** (belki, krokwie, legary z wypełnieniem) są uśredniane powierzchniowo:

- udział drewna f = szerokość drewna / rozstaw osiowy,
- λ_zast = f · 0,13 + (1 − f) · λ_wypełnienia,
- R = d / λ_zast.

To uproszczenie, które nieco zaniża wpływ mostków liniowych przez drewno.

**Pustka powietrzna** ma opór wg PN-EN ISO 6946: 0,11 m²K/W przy 5 mm, 0,13 przy 7 mm, 0,15 przy 10 mm i 0,16 przy 15 mm i więcej.

**Ruszt CD** pusty ma stały opór (0,15 dla pojedynczego, 0,16 dla podwójnego). Wypełniony wełną liczony jest jako wełna z pasmami powietrza w miejscu profili.

**Opory przejmowania:** Rsi = 0,10 i Rse = 0,10 m²K/W. Oba można zmienić w ustawieniach zaawansowanych.

**Opór całkowity:** R_T = Rsi + ΣR + Rse, a **U₀ = 1 / R_T**.

### Korekta na szczeliny ΔUg

Spoiny między matami w jednej warstwie albo w kilku warstwach ułożonych dokładnie jedna na drugiej przechodzą na wylot. Wg załącznika F normy PN-EN ISO 6946 dodawana jest wtedy korekta:

**ΔUg = 0,01 · (R_izolacji / R_T)²**

Korekta znika, gdy górna warstwa jest ułożona na mijankę lub pod kątem 90°, albo gdy wełna między belkami jest przykryta warstwą ciągłą.

**U = U₀ + ΔUg.** Wymaganie Warunków Technicznych 2021 dla stropu pod nieogrzewanym poddaszem i dla dachu: U ≤ 0,15 W/m²K.

## Rozkład temperatury

Temperatura w punkcie, do którego od strony pokoju zebrał się opór R(x):

**θ(x) = θi − (θi − θe) · R(x) / R_T**

Spadek temperatury w warstwie jest więc proporcjonalny do jej oporu: wełna przejmuje prawie całą różnicę, płyty i folia prawie nic.

## Punkt rosy

Ciśnienie nasycenia pary (PN-EN ISO 13788):

- dla θ ≥ 0 °C: p_sat = 610,5 · exp(17,269 · θ / (237,3 + θ)),
- dla θ < 0 °C: p_sat = 610,5 · exp(21,875 · θ / (265,5 + θ)).

Ciśnienie pary w pokoju: p_i = φ_i · p_sat(θi). Punkt rosy to temperatura, przy której p_sat = p_i (wzór odwrócony). Przy 20 °C i 50 % wynosi ok. 9,3 °C.

**Płaszczyzna punktu rosy** to wysokość w przegrodzie, na której θ(x) = punkt rosy.

## Paroizolacja

Za paroizolację uznawana jest warstwa o największym oporze dyfuzyjnym, jeśli ma sd ≥ 2 m. Ocena:

| Zapas: temperatura folii − punkt rosy | Status |
|---|---|
| ≥ 2 K | w normie |
| 0–2 K | uwaga |
| < 0 K | problem: para skropli się pod folią |

Kalkulator podaje też udział izolacji pod folią. Bezpieczna zasada praktyczna: najwyżej ok. 1/3.

## Kondensacja: metoda Glasera

Ciśnienie pary rozkłada się liniowo względem sumy oporu dyfuzyjnego sd (od p_i w pokoju do p_e na strychu). Opór dyfuzyjny warstwy: sd = μ · d. Jeśli w którymkolwiek miejscu p > p_sat, występuje kondensacja.

Ilość kondensatu w płaszczyźnie kondensacji c:

**g_c = δ₀ · [ (p_i − p_sat,c) / sd_1 − (p_sat,c − p_e) / sd_2 ]**

gdzie δ₀ = 2 · 10⁻¹⁰ kg/(m·s·Pa), a sd_1 i sd_2 to opory dyfuzyjne po obu stronach płaszczyzny. Wynik podawany jest w g/m² na dobę.

To obliczenie dla jednego stanu (np. mrozu projektowego), bez rocznego bilansu wilgoci. Pokazuje najgorszy dzień, a nie roczną ilość wody.

## Kanały i instalacje

- **Temperatura nad kanałem:** θ na wysokości wierzchu rury.
- **Punkt rosy wywiewu:** liczony z temperatury pokoju i wilgotności wywiewu (domyślnie 60 %, łazienki).
- **Kanał wywiewny:**
  - temperatura nad kanałem ≥ punkt rosy wywiewu: w normie,
  - między 0 °C a punktem rosy: uwaga, bo przy postoju rekuperatora powietrze w kanale może się wykraplać,
  - poniżej 0 °C: problem.

  Zalecane jest też co najmniej ok. 20 cm izolacji nad kanałem.
- **Kanał nawiewny:** ostrzeżenie, gdy otoczenie jest o więcej niż 10 K chłodniejsze od nawiewu.
- **Zimny kanał (czerpnia, wyrzutnia)** po ciepłej stronie folii wymaga otuliny paroszczelnej.
- **Peszle i przewody:** kalkulator sprawdza, czy leżą pod folią (dostęp bez przebijania), czy nad nią.

## Wysokości

- Posadzka gotowa → spód belek = (wylewka → spód belek) − podłoga docelowa.
- Pokój w świetle = posadzka → spód belek − grubość wszystkiego pod belkami.
- **Poddasze:**
  - skos przy ściance = (wylewka → spód krokwi przy ściance) − podłoga − d_pod_krokwią / cos α,
  - odległość od ścianki do wysokości h = (h − skos przy ściance) / tg α.

## Obciążenie belek

Ciężar warstw = Σ ρ · d dla wełny, płyt i wypełnień oraz stałe ciężary rusztu i membran. Drewna belek nie wlicza się do sumy, wlicza się drewno legarów. Wynik porównywany jest z dopuszczalnym obciążeniem (domyślnie 50 kg/m², typowe dla pasa dolnego wiązara).

## Straty ciepła i opłacalność docieplenia

- Strumień ciepła: q = U · (θi − θe) [W/m²].
- Strata przez całą przegrodę: P = q · A [W].
- Zużycie na sezon: E = U · A · Sd · 24 / 1000 [kWh], gdzie Sd to stopniodni (domyślnie 3600 K·d, typowo dla Polski przy 20 °C).

Dla dokładki o grubości t:

- mniej strat: ΔE = (U_przed − U_po) · A · Sd · 24 / 1000,
- mniej energii do kupienia: ΔE / sprawność (dla pompy ciepła: / SCOP),
- oszczędność: ΔE / sprawność · cena energii [zł/rok],
- koszt: A · t · cena wełny za m³ + A · robocizna za m²,
- zwrot prosty: koszt / oszczędność,
- zwrot przy wzroście cen o g rocznie: n = ln(1 + koszt · g / oszczędność) / ln(1 + g),
- bilans po 30 latach: suma oszczędności przez 30 lat (z wzrostem cen) − koszt.

## Sufit podwieszany

### Geometria

- Profile nośne biegną równolegle do belek w ruszcie podwójnym i prostopadle do belek w ruszcie pojedynczym. Płyty montuje się poprzecznie do profili nośnych.
- Rzędy płyt mają szerokość płyty. Warstwa 2 jest przesunięta o „długie krawędzie”.
- W każdym rzędzie pierwszy styk = (numer rzędu · przesunięcie styków + przesunięcie warstwy) modulo długość płyty. Kolejne styki leżą co długość płyty.

### Obciążenie wieszaka

**Q = q · pole na wieszak**, gdzie:

- q = płyty + ruszt + folia + wełna leżąca na suficie + dodatkowe [kg/m²],
- ruszt = 0,6 kg/m profilu / rozstaw profili nośnych (+ to samo dla profili głównych) + 0,3 kg/m² na wieszaki i łączniki,
- wełna = 0,2 kg/m² na każdy centymetr (ok. 20 kg/m³),
- pole na wieszak = rozstaw profili głównych × rozstaw wieszaków (w ruszcie pojedynczym: rozstaw profili nośnych × rozstaw wieszaków).

Obliczenie jest ostrożne: wieszaki przy ścianach mają w rzeczywistości mniejsze pole.

### Ciężary płyt

GKB 12,5: 9,0 kg/m² · GKBI 12,5: 9,5 · GKF 12,5: 10,0 · GKFI 12,5: 10,5 · utwardzona 12,5: 12,5 · GKB 15: 11,5.

### Ilość płyt

Kawałki z rozkładu są przydzielane do płyt metodą „pierwszy pasujący, od największego”, z wykorzystaniem odcinków. Paski węższe niż pół płyty mogą być cięte po dwa z jednej płyty. Odpad = (powierzchnia kupionych płyt − powierzchnia sufitu × warstwy) / powierzchnia kupionych płyt.

### Wkręty

- Długość: grubość płyt + 10 mm, zaokrąglona w górę do 25, 35, 45, 55 albo 70 mm.
- Liczba: liczba profili nośnych × (rozpiętość / rozstaw wkrętów + 1) · 1,1, w zaokrągleniu do 50 szt.

---

[← Spis treści](README.md) · [Otwórz kalkulator](https://mikebronka.github.io/termo-przegroda/)
