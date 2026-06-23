# Hold / Bingo Calculator

**Version 1.2** · Offline-first EFB tool for the 757 / 767.

**Live:** https://afherkdriver.github.io/holdbingo/

A holding and bingo fuel decision tool that answers two questions at a glance: **how long can I hold**, and **what fuel and clock time forces me to leave for my divert**.

---

## Features

**Aircraft Presets**
Select `757` or `767` to instantly load that fleet's Min fuel, Emergency fuel, Final approach, and GA & return numbers — including a typical hold fuel flow. `MANUAL` for anything custom. The app remembers your last selection between sessions.

**Core Readouts**
Enter fuel on board, hold fuel flow, divert fuel, and reserve floor. The app returns:
- Live **countdown to push** (large hero display, ticking in real time)
- **Push time** in Zulu and local
- **Max hold time** (static, computed at entry)
- **Bingo fuel** as its own large readout, broken down into Divert + Reserve + Above Bingo

**Reserve Floor**
One-tap `MIN` or `EMERG` chips auto-fill the correct value for the selected aircraft. The legend labels track which floor you're protecting.

**Fuel Bar**
Splits fuel on board into Hold / Divert / Reserve segments. The Hold segment shifts green → amber → red as you approach bingo, with the whole bar glowing and pulsing at the threshold. Adjustable caution threshold (default 10 minutes).

**Input Lock**
Once data is set, tap `LOCK` to freeze all inputs against accidental changes. A hold elapsed timer (`HOLD 00:00`) starts counting in the top bar from the moment you lock.

**Push Alarm**
Arm for an audible three-tone alert at hold-time expiration. Holds the screen awake while armed. Foreground only — iOS will not sound it if the app is backgrounded or the screen is locked.

**Night Mode**
Red-tinted dim display for night ops and night-vision preservation.

**Orientation Aware**
Rotates seamlessly between portrait and landscape. In landscape the hero numbers maximize to fill the screen — optimized for kneeboard or glareshield mount.

**Optional Builders**
- Derive divert fuel from leg distance, groundspeed, and fuel flow — with one-tap Final approach or GA & return arrival chips
- Derive reserve from minutes × fuel flow

**Offline**
Runs with no network connection after the first load. Airplane mode safe.

---

## Fleet Reference

| | 757 | 767 |
|---|---|---|
| Min Fuel | 4,500 lb | 7,300 lb |
| Emergency Fuel | 3,500 lb | 5,300 lb |
| Final Approach | 300 lb | 500 lb |
| GA & Return | 2,500 lb | 3,000 lb |

**Min Fuel** — Fuel to hold at 1,500 ft for 30 minutes plus fly one approach.

**Emergency Fuel** — Fuel to initiate a missed approach at 200 ft AFE, climb to 1,500 ft AFE, proceed downwind, and fly another approach from a 10 NM point from the end of the runway; approximately 30 minutes of fuel remaining.

**Final Approach** — Fuel to complete a normal approach from the final approach fix.

**Go-Around & Return** — Fuel including final approach, based on a go-around at 200 ft AFE, climb to 1,500 ft pattern altitude, configuration and speed per go-around procedure, turn to 7 NM final, sea-level standard day, calm wind, max landing weight.

---

## Files

| File | Purpose |
|---|---|
| `index.html` | The app — all HTML, CSS, and JavaScript inline |
| `manifest.webmanifest` | Makes it installable to the Home Screen |
| `sw.js` | Service worker — offline caching |
| `apple-touch-icon.png` | Home Screen icon (180px) |
| `icon-192.png` / `icon-512.png` | Manifest icons |

---

*Decision support only. Always verify against approved aircraft performance data and fuel reserves.*
