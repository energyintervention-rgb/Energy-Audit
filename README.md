# Supermarket Energy Audit Tool

A self-contained, single-file HTML tool for conducting on-site supermarket energy audits. Built for City Technical Solutions (CTS) field engineers — works fully offline, no installation, no server, no internet connection required after the first load.

## File

`supermarket_energy_audit_v2.html` — open this file in any modern browser (Chrome, Safari, Edge). That's it.

## How to use on a phone

1. Send the HTML file to your phone (WhatsApp, email, AirDrop, USB transfer).
2. Open it in **Safari** (iPhone) or **Chrome** (Android).
3. Tap **Share** → **Add to Home Screen**. This installs it like an app icon with the City logo, so you don't need to dig through Files every time.
4. Open it from the home screen during the audit. Works without signal/data once loaded.

## Site information panel

At the top of the form, collapsible (tap the header to expand/collapse):

- **Audit reference no.** — auto-generated as `CFM-EA-YYYYMMDD-001`, increments per day, but fully editable if you need to change it.
- **Store code, name, type, address, state, floor area, operating hours**
- **GPS location** — tap **Get GPS** to capture coordinates and accuracy; a Google Maps link lets you verify the pin before saving.
- **Auditor name, company (pre-filled), audit date**
- **Site contact, monthly bill (RM), TNB tariff category, max demand (kW)**
- **General site notes**

The reference number stays visible in the header even when the panel is collapsed.

## Audit sections

Six tabs across the top, each independently scored:

| Section | Content |
|---|---|
| Lighting | LED coverage, sensors, dimming, sub-metering, maintenance |
| Refrigeration | Door seals, night blinds, defrost, compressor, refrigerant, fan motors, cold room condition, ice machine |
| HVAC | Filters, setpoints, zoning, heat recovery, CO₂ control, condenser condition |
| Equipment | Energy rating, idle shutdown, servicing, motor control, food warmer type |
| Building envelope | Insulation, door/window seals, loading bay, glass tint |
| Monitoring & renewables | Sub-meters, dashboards, alarms, baselines, solar PV, EV charging |

Each question is answered **Yes / No / N/A** with a points value attached. Dropdown questions (compressor type, refrigerant, etc.) score based on the selected option. Scores roll up per section and overall, shown live as a percentage at the top of the page.

## Photos

- **Per-question camera icon (📷)** — tap to take a photo or pick from gallery; it attaches directly under that question as a thumbnail. Tap the thumbnail to remove it.
- **Section photo gallery** — at the bottom of each section, for general shots that don't belong to one specific question. Includes a caption box.
- On mobile, the camera button opens the device's rear camera directly.

## Findings notes

Each section has a free-text box for site observations, measurements, or corrective actions that don't fit the structured questions.

## Saving the completed audit

This tool stores everything **in browser memory only** — closing or refreshing the page will lose your answers and photos. To keep a record:

- Tap **Print / save as PDF** at the bottom of the page once the audit is complete. This captures all sections, scores, answers, photos, and notes in a clean printable layout.
- Do this before closing the browser tab or app.

## Known limitations

- No save/reload of in-progress audits — complete and export to PDF in one sitting, or note your answers elsewhere if you need to pause partway through.
- GPS requires location permission to be granted in the browser.
- Works fully offline once the page has loaded; only the GPS feature needs a location signal (not internet data).

## Customising the checklist

The audit questions, point weights, and dropdown options live in the `DATA` array inside the `<script>` tag of the HTML file. To add, remove, or edit any item, share the file back and we can update it together — no need to touch the code directly.

## Branding

City Technical Solutions logo, favicon, and home-screen icon are embedded directly in the file (base64), so the tool carries CTS branding wherever it's opened or installed.

---
*Built for City Technical Solutions — Energy Eye / supermarket energy audit programme.*
