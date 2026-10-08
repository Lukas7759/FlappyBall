# Flappy Ball – Update 8.10.2026

A single-file browser game: `flapy.html`. Simply open the file in your browser; no installation is required.

## What's New

### 🌍 Five Interface Languages
Polish, English, Russian, Chinese, and Japanese.

- Language selection buttons (`PL`, `EN`, `RU`, `中文`, `日本語`) are located at the top of the main menu.
- Upon first launch, the game detects your browser's language. If it is not supported, English is selected by default.
- Language selection is saved.
- Translated elements: menu, difficulty levels and their descriptions, the skin shop (including skin names), game-over screen, pause screen, data save notification, and secret ending text.
- Controller/gamepad prompts and the admin panel remain in English only.

### ⏸️ Pause
- Triggered by the **Esc** or **P** keys, the **⏸** button in the top-left corner, or by switching browser tabs.
- Pausing halts the music, pipe movement, and the shield/autopilot timers (previously, these could expire while the game was paused).
- You can resume the game or return to the menu from the pause screen.

### 🏆 "NEW RECORD!" Banner
Appears on the game-over screen when you beat your personal best score.

### 🐛 Bug Fixes
- **The admin menu no longer opens during gameplay.** Previously, rapid mouse clicking (3 clicks within 0.6 seconds) could accidentally trigger it. - **Saving to `localStorage` instead of cookies.** Chrome does not save cookies for locally opened files (`file://`), so progress could be lost. Old cookie-based saves are still read, so nothing will be lost.
- The data consent text has been updated to match the new saving method.
- Fallback fonts added for Chinese and Japanese characters.

## Controls

| Action | PC | Phone | Gamepad |
|---|---|---|---|
| Flap wings | Space / Mouse click | Touchscreen | A button |
| Pause | Esc / P / ⏸ button | ⏸ button | – |

## Save keys

Data is stored in the browser's `localStorage`:

`flappyBestScore`, `flappyTotalScore`, `flappySkin`, `flappyDifficulty`, `flappyCookieConsent`, `flappyMuted`, `flappyLang`

These are reset via the "Reset saved progress" option in the admin menu (triple-click the menu or tap with four fingers).

## What to check after the update

The code has passed syntax checks but has not yet been tested in a browser. It is worth checking:

- [ ] Each of the 5 languages ​​in the menu, shop, and game-over screen
- [ ] Pause: Esc, P, ⏸ button, and tab switching
- [ ] Shield and autopilot status after resuming from pause
- [ ] Exiting to the menu from pause, then starting a new game
- [ ] "NEW RECORD!" banner - [ ] Save score and skin after page refresh
- [ ] Rapid clicking during gameplay (admin menu should not open)

## Known missing features and plans

- Pre-start countdown and on-screen power-up icons (HUD)
- New power-ups: magnet, slow-motion, score multiplier
- Translation of controller/gamepad messages
- "Exit" button still does not close the tab (browsers block `window.close()`)


# 🚀 Flappy Ball — Update (September 26, 2026)

Play the game online right now: **[Play Flappy Ball on Google Sites](https://sites.google.com/view/x09drk-io/flapy-ball)**

 -  All. Ver. **[All versions game](https://mega.nz/folder/IIkhTJoL#IPl5EX_y7FkW3kuHl0GnMQ)**
---

## 🎮 Controller Support

Flappy Ball supports **PS3 and Xbox controllers** on compatible systems.

### PlayStation 3 Controller

* **Cross (✕)** — Flap / jump
* **Circle (○)** — Open the Skin Shop / go back
* **D-pad ↑ / ↓** — Navigate the main menu
* **D-pad ← / →** — Browse skins in the Skin Shop

### Xbox Controller

* **A** — Flap / jump
* **B** — Open the Skin Shop / go back
* **D-pad ↑ / ↓** — Navigate the main menu
* **D-pad ← / →** — Browse skins in the Skin Shop

### 🖥️ Platform Support

| Platform          | Controller Support    |
| ----------------- | --------------------- |
| 🐧 Linux          | ✅ Supported           |
| 🍎 macOS          | ✅ Supported           |
| 🎮 Console setups | ✅ Compatible gamepads |
| 🪟 Windows        | 🚧 Not supported yet  |

> **Note:** Windows controller support is planned for a future update.

The game automatically detects a connected controller and displays a **"Gamepad connected"** indicator.


### ✨ What's New in this Update:

* **Dynamic Coin System:** Collect three types of coins spawning inside pipe gaps (Gold = 2 pts, Green = 1 pt, Blue = 0.5 pts) to boost your total score.
* **Skin Shop & Rewards:** Unlock 14 unique ball skins (from basic colors to Silver, Gold, and Diamond) by accumulating total points across your runs.
* **Full Gamepad Support:** Seamlessly navigate menus, browse the shop, and play using Xbox, PlayStation, or mobile Bluetooth controllers.
* **High-Refresh-Rate Fix:** Implemented delta-time physics to ensure smooth, consistent gameplay across 60Hz, 90Hz, and 120Hz displays.
* **Cookie Consent & Saves:** Added persistent local storage for high scores, total points, and equipped skins.

---

### 📝 Short Version (For Quick Copy-Paste)

> **Flappy Ball Update (2026.09.26)**
> Play online: https://sites.google.com/view/x09drk-io/flapy-ball or shorten link https://tiny.pl/qbys4-9v9
> * **New Features:** Added a multi-tier coin system (Gold, Green, Blue coins), a 14-skin unlockable shop based on total score, and full gamepad/controller support.
> * **Improvements:** Added delta-time physics for smooth 60/120Hz gameplay, cookie consent notice, and robust score/skin persistence.


_____________________
2024-11-06 update 



**Polski:**

### **Flappy Ball**

**Flappy Ball** to przeglądarkowa gra zręcznościowa inspirowana klasycznym "Flappy Bird". Gracz kontroluje kolorową kulę, której wygląd można dostosować w sklepie przed rozpoczęciem gry. Celem gry jest przelatywanie przez przeszkody w postaci pionowych rur, omijając je i zdobywając punkty za każdą pomyślnie minioną rurę.

#### **Główne Funkcje:**

- **Sterowanie:** Gracz porusza kulą, klikając myszką, dotykając ekranu lub naciskając klawisz spacji, co powoduje, że kula unosi się w górę. Następnie kula opada pod wpływem grawitacji.
- **Przeszkody:** Rury pojawiają się z prawej strony ekranu i przesuwają się w lewą, tworząc przeszkody, które trzeba omijać.
- **Sklep z Skórkami:** Przed rozpoczęciem gry gracze mogą wybrać jedną z dostępnych skórek dla kuli:
  - **Red Ball** – Czerwona Kula
  - **Blue Ball** – Niebieska Kula
  - **Yellow Ball** – Żółta Kula
  - **White Ball** – Biała Kula
- **Ekran Ładowania:** Początkowy ekran z logo studia wyświetlany przez 4 sekundy, po czym przechodzi do menu głównego.
- **Menu Główne:** Opcje rozpoczęcia gry, przejścia do sklepu z skórkami oraz wyjścia z gry.
- **Ekran Końca Gry:** Po kolizji z rurą lub ziemią wyświetla się wynik oraz opcje powrotu do menu głównego lub ponownej próby.

**Flappy Ball** oferuje prostą, ale wciągającą rozgrywkę, która sprawdzi refleks i precyzję gracza. Dodatkowo możliwość personalizacji kuli dodaje elementy zabawy i indywidualizacji.

---

**English:**

### **Flappy Ball**

**Flappy Ball** is a browser-based arcade game inspired by the classic "Flappy Bird." Players control a colorful ball, with customizable appearances available in the shop before starting the game. The objective is to navigate through vertical pipe obstacles, dodging them and earning points for each successfully passed pipe.

#### **Key Features:**

- **Controls:** Players maneuver the ball by clicking the mouse, tapping the screen, or pressing the spacebar, causing the ball to move upward. Gravity then pulls the ball back down.
- **Obstacles:** Pipes appear from the right side of the screen and move to the left, creating barriers that must be avoided.
- **Skin Shop:** Before starting the game, players can choose from available ball skins:
  - **Red Ball**
  - **Blue Ball**
  - **Yellow Ball**
  - **White Ball**
- **Loading Screen:** An initial screen displaying the studio logo for 4 seconds, transitioning to the main menu.
- **Main Menu:** Options to start the game, access the skin shop, and exit the game.
- **Game Over Screen:** Upon collision with a pipe or the ground, the player's score is displayed along with options to return to the main menu or try again.

**Flappy Ball** offers simple yet addictive gameplay that tests the player's reflexes and precision. Additionally, the ability to customize the ball adds a fun and personalized touch to the gaming experience.


---
FlappyBall
---
---


**Polski:**

**Flappy Ball** to przeglądarkowa gra zręcznościowa inspirowana klasycznym "Flappy Bird". Gracz steruje kolorową kulą, której kolor może wybrać w sklepie przed rozpoczęciem gry. Celem jest przelatywanie przez przeszkody w postaci rur, omijając je i zdobywając punkty. Gra wymaga precyzyjnych ruchów — każdy naciśnięcie klawisza lub kliknięcie podnosi kulę, a następnie opada pod wpływem grawitacji. Kolizja z rurą lub ziemią kończy grę, wyświetlając wynik oraz opcje powrotu do menu lub ponownej próby.

---

**English:**

**Flappy Ball** is a browser-based arcade game inspired by the classic "Flappy Bird." The player controls a colorful ball, choosing its color from the shop before starting the game. The objective is to fly through pipe obstacles, dodging them and earning points. Precision is key — each key press or click makes the ball move up, while gravity pulls it down. Colliding with a pipe or the ground ends the game, displaying the score along with options to return to the menu or try again.
