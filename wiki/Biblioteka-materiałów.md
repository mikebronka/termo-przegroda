# Biblioteka materiałów

Wartości domyślne używane przez kalkulator. Pola oznaczone jako edytowalne zmienisz w rozwiniętej karcie warstwy.

## Warstwy przegrody

| Materiał | Grupa | Grubość domyślna | λ [W/mK] | μ / sd | Gęstość | Uwagi |
|---|---|---|---|---|---|---|
| Wełna mineralna – maty | izolacja | 15 cm (1–60) | 0,035, edytowalna | μ = 1 | 20 kg/m³ | układ: prosto / na mijankę / pod kątem 90° |
| Wełna wdmuchiwana | izolacja | 20 cm (1–60) | 0,040, edytowalna | μ = 1 | 30 kg/m³ | |
| Belki stropu + wypełnienie | konstrukcja | 15 cm (8–30) | drewno 0,13 + wypełnienie | jak wypełnienie | wypełnienie | rodzaj: pasy dolne wiązarów / jętki / belki stropu drewnianego; domyślnie 4,5 cm co 95 cm |
| Krokwie + wypełnienie | konstrukcja (poddasze) | 20 cm (10–30) | drewno 0,13 + wypełnienie | jak wypełnienie | wypełnienie | domyślnie 8 cm co 90 cm |
| Legary na belkach + wypełnienie | konstrukcja (strop) | 20 cm (5–40) | drewno 0,13 + wypełnienie | jak wypełnienie | wypełnienie + drewno 450 kg/m³ | domyślnie 5 cm co 60 cm, w poprzek belek |
| Pustka powietrzna | konstrukcja | 5 cm (1–40) | R wg PN-EN ISO 6946 | | | |
| Ruszt pojedynczy CD 60 | konstrukcja | 2,7 cm | R = 0,15 (pusty) | | 2,6 kg/m² | może być wypełniony wełną |
| Ruszt podwójny krzyżowy CD 60 | konstrukcja | 5,4 cm | R = 0,16 (pusty) | | 4,2 kg/m² | może być wypełniony wełną |
| Folia PE 0,2 mm | szczelność | 0,2 mm | | sd = 75 m | 0,19 kg/m² | paroizolacja |
| Membrana o zmiennym sd (Vario) | szczelność | 0,3 mm | | sd = 20 m (zimowe), edytowalne | 0,1 kg/m² | paroizolacja |
| Membrana wiatroizolacyjna / MWK | szczelność | 0,5 mm | | sd = 0,02 m | 0,14 kg/m² | |
| Płyta gipsowo-kartonowa | okładziny | 12,5 / 15 / 18 mm | 0,25 | μ = 10 | 680 kg/m³ | |
| Płyta OSB | okładziny | 12–25 mm | 0,13 | μ = 200 | 600 kg/m³ | |
| Deski z przerwami (kładka) | okładziny | 25 / 32 mm | 0,13 | μ = 5 | 450 kg/m³ | liczone z ok. 15 % przerw |

Wypełnienie belek i krokwi: wełna – maty (λ 0,035, 20 kg/m³), wełna wdmuchiwana (λ 0,040, 30 kg/m³) albo pustka.

## Instalacje w izolacji

| Element | Średnica domyślna |
|---|---|
| Kanał wywiewny rekuperacji | 75 mm |
| Kanał nawiewny rekuperacji | 75 mm |
| Kanał czerpni / wyrzutni | 160 mm |
| Peszel z przewodami | 20 mm |
| Przewód | 10 mm |

## Sufit podwieszany

### Płyty

| Płyta | Grubość | Ciężar | Do pomieszczeń mokrych |
|---|---|---|---|
| GKB 12,5 – zwykła | 12,5 mm | 9,0 kg/m² | nie |
| GKBI 12,5 – impregnowana | 12,5 mm | 9,5 kg/m² | tak |
| GKF 12,5 – ogniochronna | 12,5 mm | 10,0 kg/m² | nie |
| GKFI 12,5 – ogniochronna impregnowana | 12,5 mm | 10,5 kg/m² | tak |
| Utwardzona 12,5 (np. Diamant) | 12,5 mm | 12,5 kg/m² | tak |
| GKB 15 – zwykła | 15 mm | 11,5 kg/m² | nie |

Formaty: 120 × 200, 120 × 250, 120 × 260, 120 × 280, 120 × 300 cm.

### Wieszaki

| Wieszak | Nośność domyślna | Budowa w modelu 3D |
|---|---|---|
| Wieszak bezpośredni ES | 25 kg | strzemię w kształcie odwróconego U pod belką, ramiona przykręcone do boków profilu |
| Wieszak noniuszowy | 40 kg | górna i dolna część perforowana, spięte zawleczkami, strzemię na profilu |
| Wieszak obrotowy z prętem | 25 kg | pręt z oczkiem, wieszak sprężynowy, zawiesie na profilu |

Nośności są ustawione ostrożnie. Rzeczywiste wartości zależą od producenta i sposobu mocowania, więc sprawdź kartę techniczną i wpisz swoją wartość.

### Ruszt i limity domyślne

| Parametr | Wartość domyślna |
|---|---|
| Profil CD 60 | 0,6 kg/m, długość 3 m (lub 4 m) |
| Rozstaw profili nośnych | 40 cm (limit 50 cm, w pomieszczeniu mokrym 40 cm) |
| Rozstaw profili głównych | 100 cm (limit 100 cm) |
| Rozstaw wieszaków przy stropie betonowym | 90 cm (limit 100 cm) |
| Rozstaw wkrętów | warstwa 1: 50 cm, warstwa 2 (lub jedyna): 17 cm |
| Najkrótszy kawałek płyty | 25 cm |

## Źródła ciepła (opłacalność docieplenia)

| Źródło | Sprawność / SCOP | Cena energii (przykładowa) |
|---|---|---|
| Pompa ciepła | 3,5 | 1,05 zł/kWh (prąd) |
| Kocioł gazowy | 0,95 | 0,35 zł/kWh |
| Ogrzewanie elektryczne | 1,0 | 1,05 zł/kWh |
| Kocioł na pellet | 0,85 | 0,30 zł/kWh |

Ceny są przykładowe. Wpisz własne z rachunku.

---

[← Spis treści](README.md) · [Otwórz kalkulator](https://mikebronka.github.io/termo-przegroda/)
