# 🥚 Harrah's Gulf Coast — AR Egg Hunt 2026

**Live URL:** https://harrahs-hunt.vercel.app

---

## What This Is

This is a **location-based Augmented Reality (AR) Easter Egg Hunt** web application built for Harrah's Gulf Coast (Caesars Entertainment). It runs entirely in the mobile browser — no app download required — using the device's GPS and rear camera to create an immersive AR experience for guests and employees.

---

## How It Works

1. The player opens the URL on a mobile browser (Chrome recommended).
2. The app requests **camera** and **location (GPS)** permissions.
3. The player walks around the Casino Area. The app continuously checks the device's GPS coordinates against a list of pre-defined egg locations.
4. When the player comes within **~15 feet** of an egg location, a **3D animated egg** appears on screen via CSS/HTML rendering.
5. The player takes a screenshot, enters their name, and submits a claim.
6. A notification email is sent via the device's native mail client to the organizer.
7. The player heads to the **SportsBook Counter** to redeem their prize.

> ⚠️ Each person may claim **ONE egg only.** Claim status is stored in browser localStorage.

---

## Technical Stack

| Component | Technology |
|---|---|
| Frontend | Pure HTML5 / CSS3 / Vanilla JavaScript |
| Hosting | Vercel (vercel.com) — static site, zero backend |
| Repository | GitHub (github.com/Claudaltro/HarrahsHunt) |
| GPS | Browser Geolocation API (W3C standard) |
| Camera | Browser MediaDevices API (W3C standard) |
| Data persistence | Browser localStorage (device-only, no server) |
| Winner logging | Google Apps Script (optional — configure GOOGLE_SHEET_URL in index.html) |

---

## Permissions Required on Player's Device

- ✅ **Location (GPS)** — to detect proximity to egg locations
- ✅ **Camera** — to display the live AR camera view
- ❌ No microphone, no contacts, no photos library, no Caesars network access

> The app does **not** collect sensitive personal data, does not access any Caesars internal systems, and does not require VPN or network-level changes. Camera feed is displayed locally only — nothing is recorded or transmitted.

---

## How to Update Egg Locations (Lat/Lon)

To set the real egg positions before the event, edit the `EGGS` array in `index.html`:

```js
const EGGS = [
    { id: "guest_1", lat: 30.39400, lon: -88.97750, loc: "SportsBook Stand", type: "guest" },
    { id: "guest_2", lat: 30.39410, lon: -88.97760, loc: "Casino Floor North", type: "guest" },
    // Add more eggs here...
];
```

- **lat** = latitude (e.g. `30.39400`)
- **lon** = longitude (e.g. `-88.97750`)
- **loc** = friendly location name shown to the winner
- **type** = `"guest"` or `"employee"`
- Detection radius is set to **15 feet** — adjustable in the `onPos()` function (`dist <= 15`)

---

## Files

| File | Description |
|---|---|
| `index.html` | Entire application — HTML, CSS, and JavaScript in one file |
| `README.md` | This document |

---

*Built for Harrah's Gulf Coast — Biloxi, MS — 2026*
