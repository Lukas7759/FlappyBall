**Language:** [Polski](README.md) · English · [中文](README.zh.md)

# Flappy Ball – update

A browser game in a single file: `flapy.html`. Just open the file in a browser, nothing to install.

## What's new

### 🌍 Five interface languages
Polish, English, Russian, Chinese and Japanese.

- The language buttons (`PL`, `EN`, `RU`, `中文`, `日本語`) are at the top of the main menu.
- On first launch the game picks your browser's language, or English if that isn't supported.
- Your language choice is remembered.
- Translated: menu, difficulty levels and their descriptions, skin shop (including skin names), game over screen, pause, the data-storage notice and the secret ending text.
- Controller/gamepad messages and the admin panel are still English only.

### ⏸️ Pause
- Press **Esc** or **P**, tap the **⏸** button in the top-left corner, or switch browser tabs.
- While paused, the music, pipe movement and the shield/autopilot timers all stop (before, they could run out during a pause).
- From the pause screen you can resume or go back to the menu.

### 🏆 "NEW BEST!" banner
Shown on the game over screen when you beat your best score.

### 🐛 Bug fixes
- **The admin menu no longer opens during a run.** Before, fast mouse clicking (3 clicks within 0.6 s) could open it by accident.
- **Saving uses `localStorage` instead of cookies.** Chrome doesn't keep cookies for locally opened files (`file://`), so progress could be lost. Old cookie saves are still read, so nothing is lost.
- The data-storage consent text now matches the new way of saving.
- Added fallback fonts for Chinese and Japanese characters.

## Controls

| Action | PC | Phone | Gamepad |
|---|---|---|---|
| Flap | Space / mouse click | tap the screen | A button |
| Pause | Esc / P / ⏸ button | ⏸ button | – |

## Save keys

Data is stored in the browser's `localStorage`:

`flappyBestScore`, `flappyTotalScore`, `flappySkin`, `flappyDifficulty`, `flappyCookieConsent`, `flappyMuted`, `flappyLang`

They can be cleared with "Reset saved progress" in the admin menu (triple-click in the menu or a four-finger tap).

## What to check after the update

The code passed a syntax check but hasn't been tested in a browser yet. It's worth checking:

- [ ] Each of the 5 languages in the menu, the shop and the game over screen
- [ ] Pause: Esc, P, the ⏸ button and switching tabs
- [ ] Shield and autopilot after resuming from pause
- [ ] Leaving to the menu from pause, then starting a new game
- [ ] The "NEW BEST!" banner
- [ ] Score and skin saved after refreshing the page
- [ ] Fast clicking during a run (the admin menu should not open)

## Known gaps and plans

- A countdown before the start and power-up icons on screen (HUD)
- New power-ups: magnet, slow motion, score multiplier
- Translating the controller/gamepad messages
- The "Exit" button still doesn't close the tab (browsers block `window.close()`)

## Version 2 – levels and new skins

### 🎚️ 5 levels (based on your score in a single run)

| Level | From points | Theme |
|---|---|---|
| 1 | 0 | Day – blue sky, green pipes |
| 2 | 200 | Sunset – orange sky, sandy ground, copper pipes |
| 3 | 500 | Night – stars, moon, teal pipes |
| 4 | 800 | Cosmos – purple nebula, planet, neon pipes |
| 5 | 1100 | The end – the secret ending (it used to trigger at 200 points) |

When you reach a new level, a "LEVEL N – name" banner appears (translated into all 5 languages) and the graphics change right away. After a run ends, the menu goes back to the level 1 theme.

### 🎨 New skins (25 in total)
11 new ones were added: Lime (130 pts), Teal (150), **Shadow – the black ball (167)**, Sunset (200), Crimson (250), Navy (300), Mint (400), Lava (500), Bronze (650), Emerald (800) and Galaxy (1100). Skins unlock based on your total points across all runs.

### 🛠️ Fixes
- A missing comma after the Diamond skin caused a syntax error, so the added skin couldn't load. Fixed.
- The second skin had the same `id: 'black'` as the first one, so picking one selected both. It now has its own `id: 'shadow'`.
- The skin shop now scrolls when there are more skins than fit on the screen.
- Admin menu: a "Jump to next level / ending" button for quickly testing levels.

## Version 3 – power-ups, countdown and HUD

- **🧲 Magnet (12 s):** coins within about 190 px fly to the bird.
- **🐢 Slow motion (8 s):** the whole game slows to about 55% speed, and the screen gets a purple glow.
- **×2 Multiplier (15 s):** every coin gives double points.
- The new power-ups appear from 5 points on, each with a 3% chance per coin (shield 5%, autopilot 4%). Collecting one again refreshes its time.
- **On-screen icons:** active power-ups (shield, autopilot, magnet, slow motion, ×2) are shown under the score with a bar for the time left. They replace the old "Autopilot: 30s" text.
- **3-2-1-GO! countdown** before every run (translated into 5 languages). The bird stays still during the countdown.

## Version 4 – gamepad, Exit and durable saving

- **Pause on the gamepad:** the **Start/Options** button pauses, **A** resumes, **B** goes back to the menu. The old hidden "double Start = +198 pts" shortcut is gone (use the admin menu for testing).
- **Exit** now takes you to Google (`https://www.google.com`).
- **Durable progress saving:** your score, skins and settings are saved in both `localStorage` and a cookie that lasts about a year (browsers cap cookies at about 400 days, and every save renews it). On every launch the game restores a missing copy from the one that survived, and asks the browser to protect the data from automatic cleanup. The consent text was updated in all 5 languages.
- Note: Chrome doesn't store cookies for locally opened files (`file://`). There only `localStorage` works; the double save works once the game is hosted on a website (http/https).

## Version 5 – level 5, boss and the real ending

- **Level 5 "Inferno" (from 1100 pts):** red-black sky, stone pipes with lava and a lava floor.
- **Boss – the giant eagle 🦅:** appears every few seconds. First a ⚠ warning blinks at the height it will fly in from, then the eagle sweeps across the screen. The shield absorbs one hit, and autopilot ignores the eagle.
- **The real ending at 1400 pts** (the end of level 5). The old "Wait for updates..." joke was replaced with a congratulations message, translated into 5 languages.
- **Reward:** the **Phoenix** skin (skin number 26, unlocked at 1400 total points, so automatically after finishing the game).
- Admin menu: the "Jump to next level / ending" button also jumps to level 5 and to the ending.

## License

This project is released under the **MIT License**. The full text is in `LICENSE.md`, and a notice is at the top of `flapy.html`. You are free to use, copy, modify and distribute the game, including commercially, as long as you keep the copyright notice and the license text. The game comes with no warranty of any kind.

## Version 6 – eagles by difficulty, autopilot, performance

- **Autopilot:** when it ends, the ball gets **5 more seconds** to pass through pipes and other obstacles (it blinks, and a 👻 icon with a time bar is shown).
- **Easy:** no eagles appear (including the level 5 boss).
- **Normal:** eagles dive **from top to bottom, between the pipes**, not through them. A ⚠ warning blinks before each dive. This includes the boss.
- **Hard:** unchanged.
- **Old saves keep working:** key names and skin ids did not change. The game only validates the numbers and adds a save version, so a damaged value can never lock anyone out.
- **Device adaptation:** the game checks memory, CPU cores, OS version and the reduced-motion setting, picks a graphics quality (high, medium, low), and measures FPS while playing, lowering the quality if needed. On small screens (e.g. iPhone 4s) the pipe gaps are scaled down accordingly. Fallback styles were added for older browsers.
- **Dark skins** (Black, Shadow, Navy) get a thin light outline so they stay visible on the dark levels.
- The game is now called **Inferno Ball**.