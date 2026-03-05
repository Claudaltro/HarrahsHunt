# 🥚 Harrah's Gulf Coast — AR Egg Hunt 2026

## About This Project

**Live URL:** https://harrahs-hunt.vercel.app

This is a **location-based Augmented Reality (AR) Easter Egg Hunt** web application built for Harrah's Gulf Coast (Caesars Entertainment). It runs entirely in the mobile browser — no app download required — using the device's GPS and rear camera to create an immersive AR experience for guests and employees.

---

## 📋 For the Caesars IT / Security Team

> **This application is an approved internal marketing activation project.**
> It is a lightweight, read-only web experience hosted on Vercel (a trusted cloud platform). It does **not** collect sensitive personal data, does not access any Caesars internal systems, and does not require VPN or network-level changes.

### What it does:
- Uses the device **GPS** to detect proximity (within ~15 feet) to pre-defined egg locations on the casino floor.
- Uses the device **camera** (rear-facing only) as an AR viewfinder — purely a browser `getUserMedia` stream; no footage is recorded or transmitted.
- When a player is near an egg, a **3D animated egg** appears on screen via CSS/HTML rendering.
- The player enters their name and a **notification email** is sent via the device's native mail client (no SMTP server, no stored credentials).
- Winner data can optionally be logged to a **Google Sheets** spreadsheet via a Google Apps Script Web App URL (configured separately by the project team).
- Player claim status is stored in **browser localStorage only** — no cookies, no backend database, no authentication.

### Technical Stack:
| Component | Technology |
|---|---|
| Frontend | Pure HTML5 / CSS3 / Vanilla JavaScript |
| Hosting | Vercel (vercel.com) — static site |
| Repository | GitHub (github.com/Claudaltro/HarrahsHunt) |
| GPS | Browser Geolocation API (W3C standard) |
| Camera | Browser MediaDevices API (W3C standard) |
| Data persistence | Browser localStorage (device-only) |
| Winner logging | Google Apps Script (optional, not yet configured) |

### Permissions required on player's device:
- ✅ Location (GPS) — to detect proximity to egg locations
- ✅ Camera — to display the AR view
- ❌ No microphone, no contacts, no photos, no network beyond the public Vercel URL

---

## 🎯 How to Play

1. Open **https://harrahs-hunt.vercel.app** on a mobile browser (Chrome recommended).
2. Allow camera and location permissions when prompted.
3. Walk around the **Casino Area** — eggs are hidden in specific spots.
4. When you get within ~15 feet of an egg, it appears on your screen!
5. Take a screenshot, then enter your name to claim your prize.
6. Head to the **SportsBook Counter** to redeem.

> ⚠️ **Each person may claim ONE egg only.**

---

## 🏨 Interested in Bringing This to Your Property?

This concept is fully portable and can be customized for any Caesars Entertainment hotel, casino, or resort property. It supports:
- Custom egg locations (any GPS coordinates)
- Custom branding and color themes
- Employee-only eggs, guest eggs, or mixed events
- Integration with Google Sheets for real-time winner tracking

### Contact the Project Directors:

| Role | Name | Email |
|---|---|---|
| Marketing Manager | **Casey Paro** | cparo@caesars.com |
| AR Artist, Programmer & Marketing Specialist | **Claudia Daltro** | cdaltrodesouza@caesars.com |

We welcome collaboration with other Caesars properties to scale this experience chain-wide.

---

*Built with ❤️ for Harrah's Gulf Coast — Biloxi, MS — 2026*
