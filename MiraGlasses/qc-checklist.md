# Mira Glasses — Quality Control Checklist
*Based on device-summary.md and industry-standards.md — April 2026*

---

## How to Use This Checklist

Each item is assigned a **stage** indicating when the check occurs:
- **IQC** — Incoming Quality Control (components received from suppliers)
- **IPQC** — In-Process Quality Control (during assembly)
- **OQC** — Outgoing Quality Control (finished unit before shipment)
- **Cert** — Certification / lab testing (third-party or regulatory, not per-unit)

Each item is assigned a **severity**:
- **Critical** — Unit must be rejected; cannot ship
- **Major** — Functional defect; unit must be reworked or rejected
- **Minor** — Cosmetic or documentation defect; may ship with deviation approval

---

## 1. Physical & Mechanical

| # | Check | Method | Stage | Severity |
|---|-------|--------|-------|----------|
| 1.1 | Weight within spec: 39g ± 1g | Precision scale | OQC | Major |
| 1.2 | Dimensions within spec: 140 × 45 × 150mm ± 0.5mm | Calipers / CMM | OQC | Major |
| 1.3 | Frame width: 145.6mm ± 0.5mm | Calipers | OQC | Major |
| 1.4 | Frame shows no cracks, warping, or sink marks | Visual inspection | OQC | Major |
| 1.5 | Matte black finish uniform — no chips, scratches, or gloss spots | Visual / light box | OQC | Minor |
| 1.6 | "MIRA" temple logo correctly positioned, legible, and durable | Visual + adhesion test | OQC | Minor |
| 1.7 | Temple arms open and close smoothly; hinge torque within spec | Functional test | OQC | Major |
| 1.8 | Metal hinges properly seated; no play or rattle | Physical inspection | OQC | Major |
| 1.9 | Nose pad arms properly aligned and seated | Visual + fit check | OQC | Minor |
| 1.10 | All 3 replacement nosepads included in box | Contents count | OQC | Minor |
| 1.11 | No sharp edges or protrusions on frame or temples | Touch / visual | OQC | Major |
| 1.12 | Universal bridge fit verified across size range | Fit test on head forms | Cert | Major |
| 1.13 | Temple tip rubber/silicone properly bonded — no delamination | Pull test | OQC | Major |

---

## 2. Display System

| # | Check | Method | Stage | Severity |
|---|-------|--------|-------|----------|
| 2.1 | Both waveguides power on and display image | Functional test via app | OQC | Critical |
| 2.2 | Display color is green (monochrome); no color shift | Visual inspection | OQC | Major |
| 2.3 | Resolution renders correctly at 640×480 | Test pattern display | OQC | Major |
| 2.4 | Refresh rate confirmed at 60Hz | Oscilloscope / test tool | Cert | Major |
| 2.5 | Brightness reaches ≥ 2000 nits | Luminance meter | Cert | Major |
| 2.6 | Field of view confirms ≥ 28 degrees | Optical bench measurement | Cert | Major |
| 2.7 | Passthrough ≥ 98% (no excessive tinting or obstruction) | Spectrophotometer | Cert | Major |
| 2.8 | Display is fully private — image not visible at 45° side angle | Visual off-axis check | OQC | Critical |
| 2.9 | No dead pixels, bright spots, or waveguide delamination | Full-screen white/black test pattern | OQC | Major |
| 2.10 | Waveguide correctly aligned in both lenses — image centered in FoV | Optical alignment jig | IPQC | Major |
| 2.11 | Anti-reflective coating applied uniformly — no streaks or gaps | Visual under UV/light box | OQC | Minor |
| 2.12 | Anti-fingerprint coating applied — verified by fingerprint wipe test | Wipe test | OQC | Minor |
| 2.13 | Photobiological safety (IEC 62471) risk group classification documented | Lab test report | Cert | Critical |
| 2.14 | Display legible under bright ambient light (outdoor simulation) | Functional test | OQC | Major |

---

## 3. Audio System

| # | Check | Method | Stage | Severity |
|---|-------|--------|-------|----------|
| 3.1 | Both MEMS microphones functional — audio captured on both channels | Signal test via app | OQC | Critical |
| 3.2 | Microphone sensitivity within spec — no dead mics or low-gain units | Acoustic test chamber | OQC | Critical |
| 3.3 | Microphone SNR within acceptable range | Acoustic measurement | Cert | Major |
| 3.4 | Both speakers produce audio output — no silence or distortion | Tone playback test | OQC | Critical |
| 3.5 | Speaker SPL within safe hearing limits (EN 50332) | SPL meter | Cert | Critical |
| 3.6 | No audio bleed between left and right channels | Acoustic isolation test | Cert | Major |
| 3.7 | Open-ear audio is sufficiently discreet at normal listening volume | Listening test at 1m distance | OQC | Major |
| 3.8 | Audio pathway from mic → BLE → app → speaker functional end-to-end | System integration test | OQC | Critical |
| 3.9 | No camera component present (verify BOM and X-ray if required) | BOM audit + visual inspection | IQC / Cert | Critical |

---

## 4. Sensors

| # | Check | Method | Stage | Severity |
|---|-------|--------|-------|----------|
| 4.1 | Accelerometer functional — detects head motion | App diagnostic mode | OQC | Major |
| 4.2 | Gyroscope functional — detects angular rotation | App diagnostic mode | OQC | Major |
| 4.3 | Environmental Light Sensor functional — responds to light changes | Cover/uncover test | OQC | Major |
| 4.4 | Automatic wear detection triggers correctly (on-head / off-head) | Put on / remove test | OQC | Major |
| 4.5 | Sensor data correctly relayed to app via BLE | App sensor readout | OQC | Major |

---

## 5. Connectivity & Firmware

| # | Check | Method | Stage | Severity |
|---|-------|--------|-------|----------|
| 5.1 | BLE 5.2 pairing with iPhone completes successfully | Pairing test | OQC | Critical |
| 5.2 | BLE connection stable for ≥ 10 minutes without drops | Soak test | OQC | Critical |
| 5.3 | BLE reconnects automatically after intentional disconnect | Drop/reconnect test | OQC | Major |
| 5.4 | Audio stream latency meets sub-700ms end-to-end requirement | Latency measurement | OQC | Critical |
| 5.5 | OTA firmware update successfully applied via BLE DFU | OTA update test | Cert | Major |
| 5.6 | Firmware version matches production release manifest | Version check via app | OQC | Critical |
| 5.7 | BLE RF output within FCC / RED / ISED emission limits | RF conducted measurement | Cert | Critical |
| 5.8 | EMC emissions within FCC Part 15B / EN 55032 limits | Anechoic chamber test | Cert | Critical |
| 5.9 | SAR measurement within FCC / EN 50566 limits | SAR lab test | Cert | Critical |
| 5.10 | FCC ID / IC / CE mark correctly displayed on unit or packaging | Label audit | OQC | Critical |
| 5.11 | Bluetooth SIG QDID listed and compliant | Documentation audit | Cert | Critical |

---

## 6. Battery & Charging

| # | Check | Method | Stage | Severity |
|---|-------|--------|-------|----------|
| 6.1 | Battery cells from IQC pass incoming inspection (IEC 62133-2 cert on file) | Supplier cert audit | IQC | Critical |
| 6.2 | UN 38.3 test report on file for battery cells | Documentation audit | IQC | Critical |
| 6.3 | Battery charges to full in ≤ 40 minutes | Charge time measurement | OQC | Major |
| 6.4 | Battery life ≥ 10 hours at normal operating load | Discharge test | OQC | Critical |
| 6.5 | Magnetic charger attaches and seats correctly | Physical fit test | OQC | Major |
| 6.6 | USB-C adapter included in box and functional | Contents check + charge test | OQC | Minor |
| 6.7 | No battery swelling after 50 charge cycles | Accelerated cycle test | Cert | Critical |
| 6.8 | Overcharge protection functional — charging stops at 100% | Overcharge test | Cert | Critical |
| 6.9 | Over-discharge protection functional | Deep discharge test | Cert | Critical |
| 6.10 | Short circuit protection on battery circuit | Short circuit test | Cert | Critical |
| 6.11 | No thermal runaway under abuse conditions (nail penetration, crush) | IEC 62133-2 abuse tests | Cert | Critical |
| 6.12 | Battery cells correctly installed in both temple arms — no movement or rattle | Physical inspection | IPQC | Major |

---

## 7. Water Resistance (IPX2)

| # | Check | Method | Stage | Severity |
|---|-------|--------|-------|----------|
| 7.1 | IPX2 drip test passed — no ingress at 15° tilt, 3.3 mm/min for 10 min | IEC 60529 drip test | Cert | Critical |
| 7.2 | All seams and port openings sealed correctly | Visual inspection post-IPX test | OQC | Major |
| 7.3 | Functional test post-IPX exposure — all features operational | Full function test after drip | Cert | Critical |
| 7.4 | IPX2 claim substantiated by lab test report on file | Documentation audit | Cert | Critical |

---

## 8. Optical Lenses

| # | Check | Method | Stage | Severity |
|---|-------|--------|-------|----------|
| 8.1 | Non-Rx lens clear, scratch-free, and correctly seated in frame | Visual inspection | OQC | Major |
| 8.2 | Waveguide not damaged during lens installation | Visual + display check | IPQC | Critical |
| 8.3 | Prescription lenses ground to correct Rx within ANSI Z80.3 tolerances | Lensometer verification | OQC (Rx) | Critical |
| 8.4 | Prescription lens power, cylinder, and axis within ± tolerances | Lensometer | OQC (Rx) | Critical |
| 8.5 | Rx lens optical center aligned to pupillary distance (PD) spec | PD ruler / lensometer | OQC (Rx) | Critical |
| 8.6 | 1.74 index material confirmed from supplier | Material cert / spec sheet | IQC | Major |
| 8.7 | Anti-reflective and anti-fingerprint coatings present on both lens types | Visual / wipe test | OQC | Minor |
| 8.8 | No lens distortion or visual aberration in non-waveguide areas | Visual through-lens test | OQC | Major |

---

## 9. Electrical Safety

| # | Check | Method | Stage | Severity |
|---|-------|--------|-------|----------|
| 9.1 | IEC 62368-1 / UL 62368-1 compliance test report on file | Documentation audit | Cert | Critical |
| 9.2 | No exposed live conductors accessible during normal use | Hi-pot / visual inspection | Cert | Critical |
| 9.3 | Insulation resistance within spec | Insulation resistance test | Cert | Critical |
| 9.4 | Charging circuit complies with IEC 62368-1 energy hazard requirements | Lab test | Cert | Critical |
| 9.5 | Magnetic charger does not pose accessible energy hazard | Lab test | Cert | Critical |

---

## 10. Environmental & Substance Compliance

| # | Check | Method | Stage | Severity |
|---|-------|--------|-------|----------|
| 10.1 | RoHS compliance declarations received from all component suppliers | Supplier audit | IQC | Critical |
| 10.2 | REACH SVHC screening completed for frame, lens, and PCB materials | Material declarations | IQC | Critical |
| 10.3 | California Prop 65 screening completed; warning label applied if required | Material review | IQC | Major |
| 10.4 | WEEE symbol on product/packaging (EU units) | Label audit | OQC | Major |
| 10.5 | China RoHS hazardous substance table in manual (CN units) | Documentation audit | OQC | Major |
| 10.6 | Packaging is 100% recyclable; correct disposal markings present | Packaging audit | OQC | Minor |

---

## 11. Labeling & Documentation

| # | Check | Method | Stage | Severity |
|---|-------|--------|-------|----------|
| 11.1 | FCC ID label correct and legible (US units) | Label audit | OQC | Critical |
| 11.2 | IC certification number present (Canada units) | Label audit | OQC | Critical |
| 11.3 | CE mark present (EU units) | Label audit | OQC | Critical |
| 11.4 | UKCA mark present (UK units) | Label audit | OQC | Critical |
| 11.5 | WEEE symbol present (EU units) | Label audit | OQC | Major |
| 11.6 | Battery EU Battery Regulation compliance label / markings present | Label audit | OQC | Major |
| 11.7 | Serial number / lot code traceable and correctly applied | Traceability audit | OQC | Critical |
| 11.8 | Quick start guide / user manual included in correct language(s) | Contents check | OQC | Minor |
| 11.9 | Safety warnings (audio volume, recording consent) present in documentation | Documentation review | OQC | Major |
| 11.10 | Prescription lens non-refundable notice included with Rx orders | Documentation check | OQC (Rx) | Major |
| 11.11 | Warranty card or warranty information present | Contents check | OQC | Minor |

---

## 12. Packaging & Fulfillment

| # | Check | Method | Stage | Severity |
|---|-------|--------|-------|----------|
| 12.1 | All in-box contents present: glasses, ring, case, 3 nosepads, cloth, magnetic charger, USB-C adapter, ring charger | Contents count | OQC | Critical |
| 12.2 | Glasses correctly seated in protective packaging — no movement | Drop/shake test of sealed box | OQC | Major |
| 12.3 | Box not damaged or compromised | Visual inspection | OQC | Minor |
| 12.4 | SKU / model / variant (Rx vs non-Rx) matches label on box | Label vs. contents audit | OQC | Critical |
| 12.5 | Ring size correct for Rx orders where size was specified | Order-to-pack audit | OQC (Rx) | Critical |
| 12.6 | Li-Po battery packaging complies with IATA DGR for air shipment | Shipping label / packing audit | OQC | Critical |

---

## 13. System Integration & User Acceptance

| # | Check | Method | Stage | Severity |
|---|-------|--------|-------|----------|
| 13.1 | Full pairing flow with iPhone iOS 18+ completes without errors | End-to-end test | OQC | Critical |
| 13.2 | AI response delivered to display within 700ms under normal conditions | Latency test | OQC | Critical |
| 13.3 | Real-time transcription accurate in quiet and moderately noisy environments | Audio test | OQC | Major |
| 13.4 | Wear detection triggers app correctly on put-on and removal | Functional test | OQC | Major |
| 13.5 | Display turns off when glasses are removed (power gating) | Wear detection test | OQC | Major |
| 13.6 | 10-hour battery life test with continuous BLE + display usage | Full soak test | Cert | Critical |
| 13.7 | No unexpected reboots, freezes, or BLE drops over 4-hour soak | Reliability soak | OQC | Critical |
| 13.8 | OTA update does not brick device or degrade RF compliance | OTA test + re-certification check | Cert | Critical |

---

## Certification Summary (Third-Party Lab — Not Per-Unit)

| Certification | Standard | Market | Status Tracking |
|--------------|----------|--------|----------------|
| FCC Part 15 | FCC Part 15.247 + Part 15B | US | [ ] Complete |
| IC / ISED | RSS-247 | Canada | [ ] Complete |
| CE / RED | 2014/53/EU + ETSI EN 300 328 | EU | [ ] Complete |
| UKCA | UK RED equivalent | UK | [ ] Complete |
| Bluetooth SIG | BLE 5.2 QDID | Global | [ ] Complete |
| UL 62368-1 | Electrical safety | US | [ ] Complete |
| EN 62368-1 | Electrical safety | EU | [ ] Complete |
| IEC 62133-2 | Battery cell safety | Global | [ ] Complete |
| UN 38.3 | Battery shipping | Global | [ ] Complete |
| IEC 62471 | Photobiological safety | Global | [ ] Complete |
| IEC 60529 IPX2 | Water resistance | Global | [ ] Complete |
| SAR (FCC) | FCC OET 65 / KDB 447498 | US | [ ] Complete |
| SAR (EU) | EN 50566 | EU | [ ] Complete |
| EN 50332 | Audio SPL | EU | [ ] Complete |
| RoHS | 2011/65/EU | EU | [ ] Complete |
| REACH | EC 1907/2006 | EU | [ ] Complete |
| WEEE | 2012/19/EU | EU | [ ] Complete |
| EN 303 645 | IoT Cybersecurity | EU | [ ] Complete |
