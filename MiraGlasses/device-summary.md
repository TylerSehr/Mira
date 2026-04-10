# Mira Glasses — Device Summary
*Compiled from StartingData sources — April 2026*

---

## Product Overview

Mira Glasses are AI-powered smart glasses designed for continuous all-day wear. The device is audio-first with no camera — it captures ambient audio, transcribes it in real time via a paired iPhone, and surfaces AI responses and proactive insights through a private heads-up display. Positioned as a "cognitive copilot" and "second brain" for professionals.

**Tagline:** "Glasses that remember everything"
**Legal entity:** Industrials, Inc.
**Price:** $649 (non-prescription), $799 (prescription)
**Platform:** iOS only (Android planned)
**Warranty:** 1 year | **Returns:** 14-day (non-prescription only)

---

## Physical Form Factor

Full-rim rectangular/square eyeglass frame in conventional spectacles form. Matte black finish. Temple arms are noticeably thicker than standard glasses, housing all electronics (battery, PCB, microphones, speakers). "MIRA" logo on outer temple. Adjustable metal nose pads on a universal bridge fit.

| Spec | Value |
|------|-------|
| Weight | 39g |
| Dimensions | 140mm (W) × 45mm (H) × 150mm (D) |
| Frame width | 145.6mm (5.73 in) |
| Color | Matte black |
| Bridge | Universal bridge fit |
| Nosepads | Replaceable (3 included in box) |
| Water resistance | IPX2 |

---

## Display System

Dual waveguide display — one per lens (binocular). A micro-projector at the temple/lens edge couples light into a thin optical waveguide embedded in each lens, redirecting it into the wearer's eye. The image is fully private and invisible to outside observers. Content is text-based (AI responses, translations, teleprompter, notifications) — not full spatial AR.

| Spec | Value |
|------|-------|
| Type | Dual waveguide (binocular) |
| Display color | Green (monochrome) |
| Resolution | 640 × 480 |
| Field of View | 28 degrees |
| Refresh rate | 60Hz |
| Brightness | Up to 2000 nits |
| Passthrough | 98% |
| Privacy | Fully private — wearer-only visibility |
| Lens coating | Anti-reflective, anti-fingerprint |

---

## Audio System

| Spec | Value |
|------|-------|
| Microphones | Dual MEMS, positioned in temple arms |
| Speakers | Dual open-ear directional drivers, positioned in temple arms |
| Camera | None — intentionally excluded |
| Recording | Opt-in; audio deleted immediately after transcription |

**Audio pipeline:**
Microphones → BLE stream to iPhone → speech-to-text transcription in Mira App → audio permanently deleted → transcript stored locally → AI inference (Google/Anthropic LLMs) → response text pushed back to glasses display.

---

## Sensors & Connectivity

| Spec | Value |
|------|-------|
| Bluetooth | BLE 5.2 |
| Sensors | Accelerometer, Gyroscope, Environmental Light Sensor |
| Wear detection | Automatic |
| OTA firmware | Yes (confirmed via App Store changelogs) |

---

## Power System

| Spec | Value |
|------|-------|
| Battery life | 10 hours |
| Full charge time | 40 minutes |
| Charging method | Magnetic charger (USB-C adapter included) |
| Battery type | Li-Po cells in temple arms [inferred] |

---

## Lens Options

| Option | Detail |
|--------|--------|
| Non-prescription | Clear lens with embedded waveguide |
| Prescription | 1.74 high-index lenses (thinnest/lightest available); custom-ground to Rx |
| Prescription note | Non-refundable and non-reworkable once ordered |

---

## In the Box

- Mira Glasses
- Mira Ring controller
- Glasses case
- 3 replaceable nosepads
- Microfiber cloth
- Magnetic charger + USB-C adapter
- Magnetic ring charger

---

## Key Design Decisions & Tradeoffs

| Decision | Rationale |
|----------|-----------|
| No camera | Faster AI pipeline; stronger privacy positioning; simpler regulatory path |
| Dual waveguide (binocular) | More natural display vs. monocular; higher BOM cost and complexity |
| Compute offloaded to iPhone | Keeps glasses at 39g with 10hr battery; requires constant BT connection |
| 39g weight target | Below all-day discomfort threshold; constrains battery capacity and display brightness |
| Magnetic charging | Clean connector-free design; fast 40-minute charge |
| 1.74 high-index Rx lenses | Thinnest/lightest prescription option; requires custom-grind manufacturing |

---

## AI & Software

Compute is fully offloaded to the paired iPhone running the Mira App. The glasses themselves run a minimal embedded MCU handling audio capture, BLE, display driving, power management, and OTA firmware.

**AI backend:** Google (Alphabet) + Anthropic LLMs
**App features:** Real-time transcription, meeting notes, 60+ language translation, memory recall, proactive insights, teleprompter mode, custom knowledge uploads, 3 configurable AI skills
**Privacy:** Audio deleted immediately post-transcription; transcripts stored locally on device only; no sale or training use of user data

---

## Manufacturing Notes

- Waveguide display is the highest-complexity and highest-cost subsystem
- Frame and electronics integration likely requires Chinese OEM/ODM partners
- Prescription lens fulfillment requires a custom-grind manufacturing step outside standard CE pipeline
- OTA firmware confirmed — requires secure bootloader and BT DFU on MCU
- Company is seed-stage (~7 employees); manufacturing not yet at full production scale
