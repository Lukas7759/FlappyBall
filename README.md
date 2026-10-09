**Język:** Polski · [English](README.en.md) · [中文](README.zh.md)

# Flappy Ball – aktualizacja

Gra przeglądarkowa w jednym pliku: `flapy.html`. Wystarczy otworzyć plik w przeglądarce, nie trzeba nic instalować.

## Co nowego

### 🌍 Pięć języków interfejsu
Polski, angielski, rosyjski, chiński i japoński.

- Przyciski wyboru języka (`PL`, `EN`, `RU`, `中文`, `日本語`) są na górze menu głównego.
- Przy pierwszym uruchomieniu gra wybiera język przeglądarki. Jeśli go nie obsługuje, ustawia angielski.
- Wybór języka jest zapamiętywany.
- Przetłumaczone: menu, poziomy trudności i ich opisy, sklep ze skórkami (razem z nazwami skórek), ekran końca gry, pauza, komunikat o zapisie danych i tekst sekretnego zakończenia.
- Komunikaty kontrolera/pada i panel admina nadal są tylko po angielsku.

### ⏸️ Pauza
- Klawisze **Esc** lub **P**, przycisk **⏸** w lewym górnym rogu albo przełączenie karty przeglądarki.
- W pauzie zatrzymują się muzyka, ruch rur oraz czasomierze tarczy i autopilota (wcześniej mogły się skończyć w trakcie pauzy).
- Z pauzy można wznowić grę albo wyjść do menu.

### 🏆 Baner „NOWY REKORD!”
Pojawia się na ekranie końca gry, gdy pobijesz swój najlepszy wynik.

### 🐛 Poprawki błędów
- **Menu admina nie otwiera się już w trakcie gry.** Wcześniej szybkie klikanie myszą (3 kliknięcia w 0,6 s) mogło je przypadkowo otworzyć.
- **Zapis w `localStorage` zamiast w ciasteczkach.** Chrome nie zapisuje ciasteczek dla plików otwieranych lokalnie (`file://`), więc postęp mógł się gubić. Stare zapisy z ciasteczek są nadal odczytywane, więc nic nie przepadnie.
- Tekst zgody na zapis danych dopasowano do nowego sposobu zapisu.
- Dodano czcionki zapasowe dla znaków chińskich i japońskich.

## Sterowanie

| Akcja | PC | Telefon | Pad |
|---|---|---|---|
| Machnięcie skrzydłami | Spacja / klik myszą | dotyk ekranu | przycisk A |
| Pauza | Esc / P / przycisk ⏸ | przycisk ⏸ | – |

## Klucze zapisu

Dane są w `localStorage` przeglądarki:

`flappyBestScore`, `flappyTotalScore`, `flappySkin`, `flappyDifficulty`, `flappyCookieConsent`, `flappyMuted`, `flappyLang`

Resetuje je opcja „Reset saved progress” w menu admina (potrójne kliknięcie w menu lub dotknięcie czterema palcami).

## Co sprawdzić po aktualizacji

Kod przeszedł kontrolę składni, ale nie był jeszcze testowany w przeglądarce. Warto sprawdzić:

- [ ] Każdy z 5 języków w menu, sklepie i na ekranie końca gry
- [ ] Pauza: Esc, P, przycisk ⏸ i zmiana karty
- [ ] Tarcza i autopilot po wznowieniu z pauzy
- [ ] Wyjście do menu z pauzy, a potem nowa gra
- [ ] Baner „NOWY REKORD!”
- [ ] Zapis wyniku i skórki po odświeżeniu strony
- [ ] Szybkie klikanie w trakcie gry (menu admina nie powinno się otworzyć)

## Znane braki i plany

- Odliczanie przed startem i ikony power-upów na ekranie (HUD)
- Nowe power-upy: magnes, spowolnienie, mnożnik punktów
- Tłumaczenie komunikatów kontrolera/pada
- Przycisk „Exit” nadal nie zamyka karty (przeglądarki blokują `window.close()`)

## Wersja 2 – poziomy i nowe skórki

### 🎚️ 5 poziomów (liczone z wyniku w jednym biegu)

| Poziom | Od punktów | Motyw |
|---|---|---|
| 1 | 0 | Dzień – niebieskie niebo, zielone rury |
| 2 | 200 | Zachód słońca – pomarańczowe niebo, piaskowa ziemia, miedziane rury |
| 3 | 500 | Noc – gwiazdy, księżyc, turkusowe rury |
| 4 | 800 | Kosmos – fioletowa mgławica, planeta, neonowe rury |
| 5 | 1100 | Koniec gry – sekretne zakończenie (wcześniej było przy 200 pkt) |

Przy wejściu na nowy poziom pojawia się baner „POZIOM N – nazwa” (przetłumaczony na 5 języków), a grafika zmienia się od razu. Po zakończeniu biegu menu wraca do motywu poziomu 1.

### 🎨 Nowe skórki (25 razem)
Dodano 11 nowych: Lime (130 pkt), Teal (150), **Shadow – czarna kulka (167)**, Sunset (200), Crimson (250), Navy (300), Mint (400), Lava (500), Bronze (650), Emerald (800) i Galaxy (1100). Skórki odblokowuje suma punktów ze wszystkich biegów.

### 🛠️ Poprawki
- Brakujący przecinek po skórce Diamond powodował błąd składni, więc dodana skórka nie mogła się załadować. Naprawione.
- Druga skórka miała to samo `id: 'black'` co pierwsza, więc wybór jednej zaznaczał obie. Teraz ma osobne `id: 'shadow'`.
- Sklep ze skórkami przewija się, gdy skórek jest więcej, niż mieści ekran.
- Menu admina: przycisk „Jump to next level / ending” do szybkiego testowania poziomów.
