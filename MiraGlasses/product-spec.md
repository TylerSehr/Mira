# Mira Glasses — Complete Product Specification
*Compiled from device-summary.md, industry-standards.md, qc-checklist.md, component-list.md — April 2026*

Where official specs are not publicly disclosed, values are marked **[INFERRED]** based on industry-standard analogues for this device class.

---

## 1. Product Identity

| Field | Value |
|-------|-------|
| Product name | Mira Glasses |
| Brand | MIRA |
| Legal entity | Industrials, Inc. |
| Website | trymira.com |
| SKU variants | Non-prescription (clear lens); Prescription (1.74 high-index, custom Rx) |
| Color | Matte Black (only available color) |
| Platform compatibility | iOS 18.0+ (Android planned) |
| Price | $649 (non-Rx); $799 (Rx) |
| Warranty | 1 year |
| Return policy | 14-day (non-Rx only; Rx lenses non-refundable once ordered) |

---

## 2. Physical Specifications

### 2.1 Dimensions & Weight

| Spec | Value | Tolerance |
|------|-------|-----------|
| Weight (assembled) | 39g | ± 1g |
| Overall width | 145.6mm (5.73 in) | ± 0.5mm |
| Frame width (lens to lens) | 140mm | ± 0.5mm |
| Frame height | 45mm | ± 0.5mm |
| Temple length (depth) | 150mm | ± 0.5mm |

### 2.2 Frame Construction

| Spec | Value |
|------|-------|
| Frame style | Full-rim rectangular/square |
| Frame material | Injection-molded nylon or TR-90 (thermoplastic rubber) [INFERRED] |
| Temple arms | Hollow thickened arms housing all electronics [INFERRED] |
| Internal structure | Metal chassis/ribs for structural rigidity [INFERRED] |
| Hinge type | Spring-loaded barrel hinge (5- or 7-barrel) [INFERRED] |
| Hinge material | Stainless steel or titanium alloy [INFERRED] |
| Hinge screws | M1.4–M1.6 stainless steel [INFERRED] |
| Bridge | Universal bridge fit |
| Nose pad arms | Adjustable stainless steel saddle arms |
| Nose pads | Replaceable silicone push-fit; 3 included in box |
| Temple tips | Soft silicone overmold for comfort [INFERRED] |
| Finish | Matte black; uniform — no chips, scratches, or gloss variation |
| Logo | "MIRA" on outer temple arm; engraved, pad-printed, or laser-etched |
| Sealing | Silicone gaskets at speaker/mic port openings for IPX2 compliance |

### 2.3 Environmental Ratings

| Spec | Value | Standard |
|------|-------|----------|
| Water resistance | IPX2 | IEC 60529 |
| IPX2 definition | Protected against dripping water at up to 15° tilt; 3.3mm/min for 10 min | IEC 60529 |

---

## 3. Display System

### 3.1 Overview

Binocular dual waveguide display — one optical system per lens. A micro-projector at the inner edge of each lens projects light into a waveguide substrate, which redirects it into the wearer's eye. The image is visible only to the wearer.

### 3.2 Display Specifications

| Spec | Value |
|------|-------|
| Display type | Dual waveguide (binocular) |
| Projector type | Micro-OLED or LCoS [INFERRED] |
| Display color | Green (monochrome) |
| Resolution | 640 × 480 |
| Refresh rate | 60Hz |
| Brightness | Up to 2000 nits |
| Field of view | 28 degrees |
| Passthrough | 98% |
| Privacy | Fully private — image not visible beyond ±45° off-axis |
| Content type | Text only: AI responses, notifications, translations, teleprompter |
| Lens coating | Anti-reflective + anti-fingerprint on all outer surfaces |

### 3.3 Photobiological Safety

| Spec | Value | Standard |
|------|-------|----------|
| Risk group classification | Must be documented; target RG0 or RG1 | IEC 62471 |
| Hazard evaluation | Blue-light hazard, retinal thermal hazard, UV hazard | IEC 62471 / TR 62778 |

---

## 4. Audio System

### 4.1 Microphones

| Spec | Value |
|------|-------|
| Type | Dual MEMS digital microphones |
| Quantity | 2 (one per temple arm) |
| Mode | Always-on (low-power standby until recording activated) |
| Interface | PDM or I2S to SoC [INFERRED] |
| Features | Noise reduction, voice activity detection (VAD) [INFERRED] |
| Port protection | Acoustic mesh for IPX2 ingress protection |

### 4.2 Speakers

| Spec | Value |
|------|-------|
| Type | Open-ear directional micro-speakers |
| Quantity | 2 (one per temple arm, angled toward ear canal) |
| Audio quality | Crystal-clear; described as dual built-in speakers |
| Maximum SPL | Must comply with EN 50332 safe hearing limits |
| Port protection | Acoustic mesh for IPX2 ingress protection |

### 4.3 No Camera

The device deliberately contains no camera, image sensor, image signal processor, or optical imaging components. This is a confirmed design decision and must be verified at IQC and OQC.

### 4.4 Audio Processing Pipeline

```
[Dual MEMS mics] → [On-device DSP: noise reduction, VAD] → [BLE stream to iPhone]
→ [Mira App: speech-to-text transcription] → [Audio deleted immediately]
→ [Transcript stored locally on iPhone] → [AI inference: Google/Anthropic LLMs]
→ [Response text → BLE → glasses display]
```

End-to-end latency target: **< 700ms**

---

## 5. Sensors

| Sensor | Type | Interface | Function |
|--------|------|-----------|----------|
| Accelerometer | 3-axis MEMS | I2C / SPI | Motion detection, orientation |
| Gyroscope | 3-axis MEMS | I2C / SPI | Angular rotation; combined 6-axis IMU with accelerometer [INFERRED] |
| Ambient light sensor | Photodiode-based | I2C | Adaptive display brightness |
| Wear detection | IR proximity or capacitive | GPIO / I2C | On-head / off-head detection; auto-pause recording when removed |

---

## 6. Compute & Connectivity

### 6.1 On-Device Compute

| Spec | Value |
|------|-------|
| SoC / MCU | Low-power BLE SoC (e.g. Nordic nRF5340 or equivalent) [INFERRED] |
| Responsibilities | BLE 5.2 stack, audio capture/routing, display driver, sensor polling, power management, OTA DFU |
| External flash | 4–8MB SPI NOR flash for firmware [INFERRED] |
| EMI shielding | Metal shielding can over radio section |

### 6.2 Bluetooth

| Spec | Value | Standard |
|------|-------|----------|
| Bluetooth version | BLE 5.2 | Bluetooth SIG |
| Frequency | 2.4GHz ISM band | |
| Qualification | Must hold valid Bluetooth SIG QDID | Bluetooth SIG |
| Pairing | Pairs with iPhone running Mira App (iOS 18.0+) | |
| Profiles | Audio stream (mic data to phone); display data (text to glasses); sensor data; control channel | |
| Reconnection | Automatic on proximity | |

### 6.3 Regulatory RF Requirements

| Market | Standard | Requirement |
|--------|----------|-------------|
| USA | FCC Part 15.247 | Conducted + radiated emission limits; FCC ID required |
| Canada | ISED RSS-247 | IC certification required |
| EU | RED 2014/53/EU + ETSI EN 300 328 | CE mark; Declaration of Conformity |
| UK | UKCA + UK RED equivalent | UKCA mark |

### 6.4 EMC

| Standard | Scope |
|----------|-------|
| FCC Part 15 Subpart B | Unintentional emissions (US) |
| EN 55032 (CISPR 32) | Emissions — multimedia equipment (EU) |
| EN 55035 (CISPR 35) | Immunity — multimedia equipment (EU) |

### 6.5 SAR

| Market | Standard | Limit |
|--------|----------|-------|
| USA | FCC OET Bulletin 65 / KDB 447498 | 1.6 W/kg over 1g tissue |
| EU | EN 50566 / IEC 62209-2 | 2.0 W/kg over 10g tissue |

---

## 7. Power System

### 7.1 Battery

| Spec | Value | Standard |
|------|-------|----------|
| Battery type | Lithium polymer (Li-Po) [INFERRED] | |
| Configuration | Split cells — one per temple arm [INFERRED] | |
| Battery life | 10 hours (continuous BLE + display + audio operation) | |
| Charge time (full) | 40 minutes | |
| Charging method | Magnetic charger (contact pins on temple arm) | |
| Input | USB-C adapter (included) | |
| Safety certification | IEC 62133-2 (cells); UN 38.3 (transport) | |
| Protections | Overcharge, over-discharge, short-circuit, thermal (NTC thermistor) | IEC 62133-2 |

### 7.2 Power Management

| Spec | Value |
|------|-------|
| PMIC | Dedicated power management IC [INFERRED] |
| Display power gating | Display off when glasses removed (wear detection) |
| Sleep state | BLE connectable; touch/gesture input maintained; microphone standby |
| Charging IC | CC/CV charging profile; target C-rate for 40-min charge [INFERRED] |

---

## 8. Optical Lenses

### 8.1 Non-Prescription Variant

| Spec | Value |
|------|-------|
| Lens type | Clear optical lens with integrated waveguide |
| Index | Standard clear optic [INFERRED] |
| Coating | Anti-reflective + anti-fingerprint |
| Passthrough | 98% |

### 8.2 Prescription Variant

| Spec | Value | Standard |
|------|-------|----------|
| Lens index | 1.74 high-index (thinnest/lightest available) | |
| Customization | Ground to patient Rx (sphere, cylinder, axis, PD) | |
| Power tolerance | Per ANSI Z80.3 / EN ISO 21987 | ANSI Z80.3 |
| Coating | Anti-reflective + anti-fingerprint | |
| Legal requirement | Valid Rx from licensed eye care professional required (US) | FDA 21 CFR Part 886 |
| Returns | Non-refundable and non-reworkable once ordered | |
| EU classification | Class I medical device under EU MDR 2017/745 | EU MDR |

---

## 9. Firmware Requirements

| Requirement | Detail |
|-------------|--------|
| Bootloader | Secure; cryptographic signature verification on all firmware images |
| OTA DFU | BLE-based over-the-air firmware update; encrypted and authenticated packages |
| BLE stack | BLE 5.2 qualified (Bluetooth SIG QDID) |
| Audio pipeline | Mic capture → VAD → BLE streaming; speaker playback |
| Display driver | 640×480 @ 60Hz; brightness control; auto-off on wear removal |
| Sensor polling | IMU, ALS, wear detection; configurable sample rates |
| Power state machine | Active / idle / sleep / charging states |
| Security | No default passwords; secure update delivery; vulnerability disclosure process per EN 303 645 / EU CRA |

---

## 10. Software — Mira App

| Spec | Value |
|------|-------|
| Developer | Industrials, Inc. |
| Platform | iOS 18.0+ (iPhone, iPad, iPod touch) |
| App size | 73.1 MB |
| AI backend | Google (Alphabet) + Anthropic LLMs |
| Transcript storage | Local on iPhone only (never on Mira servers) |
| Audio handling | Deleted immediately and permanently after transcription |

**Free tier features:**
- Unlimited meeting transcription + automatic notes
- Real-time translation — 60+ languages
- Memory recall (searchable conversation history)
- Proactive AI insights
- Teleprompter mode
- Custom knowledge uploads (docs, CRM, playbooks)
- 3 configurable custom AI skills

**Premium tier ($19.99/month or $191.99/year):**
- Unlimited AI assistant queries (free tier: 3/day)
- Advanced proactive insights
- Early customers: 1-month free trial

---

## 11. System Architecture

```
┌─────────────────────────────────────────────────────┐
│                   MIRA GLASSES                       │
│                                                      │
│  [MEMS Mic L] [MEMS Mic R]                          │
│       │              │                              │
│       └──────┬───────┘                              │
│          [Audio DSP / SoC]                          │
│              │    │    │                            │
│         [IMU][ALS][Wear]  [Display Driver]          │
│                            │          │             │
│                    [Projector L] [Projector R]      │
│                    [Waveguide L] [Waveguide R]      │
│                                                     │
│  [Li-Po L] [Li-Po R] → [BMS] → [PMIC] → Rails     │
│  [Magnetic Charge Contacts]                         │
│  [BLE 5.2 Antenna]                                  │
└──────────────────┬──────────────────────────────────┘
                   │ BLE 5.2
                   │ (audio stream, display data, sensors, control)
┌──────────────────▼──────────────────────────────────┐
│              IPHONE — MIRA APP (iOS 18+)            │
│                                                      │
│  STT Transcription → Transcript (local storage)     │
│  Audio: deleted immediately post-transcription      │
│                    │                                │
│            HTTPS API calls                          │
│                    │                                │
│  ┌─────────────────▼──────────────────┐            │
│  │  Cloud AI (Google + Anthropic LLMs)│            │
│  └─────────────────┬──────────────────┘            │
│                    │ Response text                  │
│  App → BLE → Glasses display                        │
└─────────────────────────────────────────────────────┘
```

---

## 12. Regulatory Compliance Requirements

### 12.1 Certifications Required (by market)

| Certification | Standard | Market |
|--------------|----------|--------|
| FCC Part 15 | Part 15.247 + Part 15B | USA |
| ISED / IC | RSS-247 | Canada |
| CE / RED | 2014/53/EU + ETSI EN 300 328 | EU |
| UKCA | UK RED equivalent | UK |
| Bluetooth SIG | BLE 5.2 QDID | Global |
| UL 62368-1 | Electrical safety | USA |
| EN 62368-1 | Electrical safety | EU |
| IEC 62133-2 | Li-Po battery safety | Global |
| UN 38.3 | Battery transport | Global |
| IEC 62471 | Photobiological safety (display) | Global |
| IEC 60529 IPX2 | Water resistance | Global |
| SAR — FCC | FCC OET 65 / KDB 447498 | USA |
| SAR — EU | EN 50566 | EU |
| EN 50332 | Audio SPL / hearing safety | EU |
| RoHS | 2011/65/EU | EU |
| REACH | EC 1907/2006 | EU |
| WEEE | 2012/19/EU | EU |
| EN 303 645 | IoT cybersecurity | EU |
| FDA 21 CFR 886 | Prescription optics (Rx variant) | USA |
| EU MDR 2017/745 | Prescription optics (Rx variant) | EU |
| ANSI Z80.3 | Ophthalmic lens quality (Rx variant) | USA |

### 12.2 Privacy & Recording Law Compliance

| Requirement | Detail |
|-------------|--------|
| ECPA / Wiretap Act | Recording opt-in only; audio deleted post-transcription |
| California CIPA | All-party consent guidance provided in user documentation |
| GDPR | Transcripts stored locally; no data sold or used for training; DPAs with Google/Anthropic required |
| CCPA | Privacy policy must disclose data handling practices |

---

## 13. In-Box Contents

| Item | Qty | Notes |
|------|-----|-------|
| Mira Glasses | 1 | Assembled, tested, firmware loaded |
| Mira Ring controller | 1 | See separate Ring product spec |
| Glasses case | 1 | Rigid protective case |
| Replacement nosepads | 3 | Silicone; same spec as installed |
| Microfiber cleaning cloth | 1 | Lens-safe |
| Magnetic charging cable | 1 | Mates to temple contacts; USB-C opposite end |
| USB-C power adapter | 1 | Regional plug variant per market |
| Quick start guide | 1 | Language set per market; includes consent guidance |
| Regulatory insert | 1 | FCC/IC/CE statements, SAR info, safety warnings |

---

## 14. Packaging

| Spec | Value |
|------|-------|
| Outer box | 100% recyclable cardboard; branded; SKU/variant label on exterior |
| Inner insert | Molded pulp or EVA foam; glasses and accessories secured against movement |
| Plastics | No single-use plastic |
| Markings | WEEE symbol, battery disposal symbol, recyclable symbol (EU); Prop 65 warning (CA if required) |
| Shipping compliance | Li-Po battery per IATA DGR Section II (devices with batteries) |

---

## 15. Quality Acceptance Criteria (Summary)

Full detail in qc-checklist.md. Key pass/fail gates:

| Gate | Criteria |
|------|----------|
| Weight | 39g ± 1g |
| Both displays functional | Green image, 640×480, no dead pixels, fully private |
| Both mics functional | Signal present on both channels; VAD responsive |
| Both speakers functional | Audio output, no distortion, SPL within EN 50332 |
| No camera present | Confirmed by BOM audit + visual |
| BLE pairing | iPhone pairing completes; stable connection |
| End-to-end latency | < 700ms mic → display |
| Battery life | ≥ 10 hours on discharge test |
| Charge time | ≤ 40 minutes to full |
| IPX2 | Passes IEC 60529 drip test; full function post-test |
| Firmware version | Matches production release manifest |
| Wear detection | On-head / off-head state transitions correctly |
| Labels | FCC ID / CE / serial number correct and legible |
| In-box contents | All 9 items present and correct |

---

## 16. Known Constraints & Open Items

| Item | Status | Note |
|------|--------|------|
| Projector type (Micro-OLED vs LCoS) | [INFERRED] | Confirm with waveguide supplier |
| SoC selection | [INFERRED] | Confirm BLE 5.2 + audio + display capability in one IC vs. separate |
| Battery capacity (mAh) | Not disclosed | Must be validated against 10hr runtime during EVT/DVT |
| Charging IC / charge rate | [INFERRED] | Must achieve 40-min charge without exceeding Li-Po thermal limits |
| Temple arm internal layout | [INFERRED] | PCB, battery, mic, speaker packing within 39g / ~150mm temple |
| Android app | Planned; no timeline | iOS only at launch |
| HSA eligibility | In progress | Not yet available |
| EU CRA compliance | Required | Cyber Resilience Act enforcement timeline; plan OTA security architecture accordingly |
