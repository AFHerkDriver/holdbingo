# Hold / Bingo Calculator

**Version 1.1** · Installable, offline-first EFB tool for the 757 / 767.

**Live:** https://afherkdriver.github.io/holdbingo/

A holding / bingo decision tool that answers two questions at a glance: **how long can I hold**, and **what fuel and clock time forces me to leave for my divert**.

- **Aircraft presets** — tap `757` or `767` to load that fleet's Min fuel, Emergency fuel, Final approach, and GA & return numbers. `MANUAL` for anything custom.
- **Core math** — enter fuel on board, hold fuel flow, divert fuel, and reserve floor; it returns **Max hold time**, the **Push time** (Zulu + local), a **live countdown**, and **Bingo fuel** (divert + reserve) as its own large readout.
- **Reserve floor toggle** — `MIN` or `EMERG`, auto-filled per aircraft; the labels track which floor you're protecting.
- **Fuel bar + color states** — splits fuel on board into burnable Hold / Divert / Reserve, and shifts green → amber (~10 min out) → red (below bingo).
- **Optional builders** — derive divert fuel from leg distance / groundspeed / fuel flow plus a Final approach or GA & return chip; derive reserve from minutes × fuel flow.
- **Push alarm** — arm it for an audible alert at hold-time expiration; holds the screen awake while armed. Foreground only — iOS won't sound it if the app is backgrounded or the phone is locked.
- **Offline** — after the first load it runs with no connection of any kind.

---

*Decision support only. Always verify against approved aircraft performance data and fuel reserves.*
