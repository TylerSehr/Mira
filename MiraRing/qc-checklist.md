# Mira Ring — Quality Control Checklist
**Prepared for:** Supplier Sourcing & Manufacturing
**Date:** April 2026
**Based on:** device-summary.md, industry-standards.md

---

## How to Use This Checklist

This checklist covers three inspection stages:
- **IQC** — Incoming Quality Control (components arriving at factory)
- **IPQC** — In-Process Quality Control (during assembly)
- **OQC** — Outgoing Quality Control (finished units before shipment)

Each item includes the inspection method, acceptance criteria, and the regulatory or design requirement it supports. Items marked **[CRITICAL]** are blockers — any failure must halt the production lot and trigger root cause investigation before release.

Sampling plans should follow AQL 2.5 (general inspection) and AQL 1.0 (critical defects) per ANSI/ASQ Z1.4 unless otherwise specified.

---

## Section 1 — Incoming Quality Control (IQC)

### 1.1 LiPo Battery Cell

| # | Check | Method | Acceptance Criteria | Requirement |
|---|-------|--------|---------------------|-------------|
| 1.1.1 | **[CRITICAL]** Cell supplier certification | Document review | IEC 62133-2 cert current and valid; UL 1642 cert present | IEC 62133-2; UL 1642 |
| 1.1.2 | **[CRITICAL]** UN 38.3 test report | Document review | Valid UN 38.3 report on file for this cell model/lot | UN 38.3 (required for any international shipment) |
| 1.1.3 | Cell capacity (mAh) | Charge/discharge cycle test on sampled cells | Within ±5% of rated capacity | Product spec |
| 1.1.4 | Cell dimensions | Calipers | Within ±0.2mm of specified dimensions | Fit within ring form factor |
| 1.1.5 | Cell open-circuit voltage | Multimeter | Per cell spec (typically 3.6–3.7V for LiPo) | Safety / BMS calibration |
| 1.1.6 | Cell visual inspection | Visual | No deformation, swelling, puncture, discoloration, or electrolyte leakage | Safety |
| 1.1.7 | Cell protection circuit (BMS/PCM) | Functional test | Overcharge, over-discharge, and short-circuit protection active | UL 62368-1; CPSC |
| 1.1.8 | Cell lot traceability | Document review | Lot number, date code, and cell spec sheet match purchase order | Supply chain traceability |

### 1.2 BLE SoC / Module

| # | Check | Method | Acceptance Criteria | Requirement |
|---|-------|--------|---------------------|-------------|
| 1.2.1 | **[CRITICAL]** FCC modular approval | Document review | FCC Grant of Authorization on file for this module; FCC ID confirmed | FCC Part 15C |
| 1.2.2 | **[CRITICAL]** IC (Canada) certification | Document review | IC ID on file for this module | ISED RSS-247 |
| 1.2.3 | CE RED certification (EU) | Document review | EN 300 328 test report and DoC on file | EU RED 2014/53/EU |
| 1.2.4 | Bluetooth SIG qualification | Document review | QDID on file; module listed in Bluetooth SIG QDID database | Bluetooth SIG |
| 1.2.5 | Part number and revision | Visual / document | Part number and hardware revision match approved BOM | BOM integrity |
| 1.2.6 | Country of origin marking | Visual | Correctly marked per customs requirements | Import compliance |

### 1.3 Ring Shell & Outer Body

| # | Check | Method | Acceptance Criteria | Requirement |
|---|-------|--------|---------------------|-------------|
| 1.3.1 | **[CRITICAL]** RoHS material declaration | Document review | IPC-1752A or equivalent material declaration from supplier; all restricted substances below limits | EU RoHS 2011/65/EU |
| 1.3.2 | **[CRITICAL]** REACH SVHC declaration | Document review | SVHC declaration provided; any SVHC above 0.1% w/w disclosed | EU REACH |
| 1.3.3 | **[CRITICAL]** CPSIA lead content (plastics) | XRF screening or lab report | Lead ≤ 100 ppm in substrate; ≤ 90 ppm in surface coating | CPSIA |
| 1.3.4 | CPSIA phthalates (plastics) | Lab test report from supplier | Each phthalate ≤ 1000 ppm | CPSIA |
| 1.3.5 | Outer shell color | Visual comparison to golden sample | Matte black, uniform, matching approved color standard | Design spec |
| 1.3.6 | Outer shell surface finish | Visual + tactile | Smooth matte texture; no gloss patches, texture variation, visible mold lines on cosmetic surfaces | Design spec |
| 1.3.7 | Shell dimensions per size SKU | Calipers / ring gauge | Inner diameter matches ring size spec ±0.1mm; band width and wall thickness within tolerance | Sizing spec |
| 1.3.8 | Shell structural integrity | Drop test sample units | No cracking or delamination after 1m drop onto concrete (each orientation) | Durability |

### 1.4 Inner Metallic Band

| # | Check | Method | Acceptance Criteria | Requirement |
|---|-------|--------|---------------------|-------------|
| 1.4.1 | **[CRITICAL]** Nickel release rate | EN 1811 test report from accredited lab | Nickel release ≤ 0.5 µg/cm²/week | EU REACH Annex XVII Entry 27 |
| 1.4.2 | Material grade verification | Material cert / XRF | 316L stainless steel or approved nickel-free alternative confirmed | EU Nickel Directive; skin safety |
| 1.4.3 | RoHS compliance | XRF screening | Hexavalent chromium absent; all restricted substances within limits | EU RoHS |
| 1.4.4 | Surface finish | Visual | Chrome/silver finish uniform, no pits, scratches, or plating defects | Design spec |
| 1.4.5 | Inner diameter tolerance | Ring gauge / calipers | ±0.1mm per size SKU | Fit and comfort |

### 1.5 Magnetic Charging Cradle

| # | Check | Method | Acceptance Criteria | Requirement |
|---|-------|--------|---------------------|-------------|
| 1.5.1 | RoHS compliance | Material declaration | Full RoHS declaration from supplier | EU RoHS |
| 1.5.2 | USB-C connector spec | Document / visual | USB-C 2.0 minimum; meets USB-IF mechanical spec | Interoperability |
| 1.5.3 | Magnetic alignment | Functional test | Ring seats and holds on cradle consistently across all size SKUs; no lateral drift during charge | Product spec |
| 1.5.4 | Cradle charging output | Multimeter / power analyzer | Output voltage and current within spec for the ring's BMS input requirements | Battery safety |
| 1.5.5 | Cable strain relief | Pull test | Cable withstands 10N pull without separation or damage to connector | Durability |

### 1.6 PCB / Flex Assembly

| # | Check | Method | Acceptance Criteria | Requirement |
|---|-------|--------|---------------------|-------------|
| 1.6.1 | RoHS solder compliance | Document review / XRF | Lead-free solder confirmed; no RoHS-restricted substances | EU RoHS |
| 1.6.2 | PCB visual inspection | AOI or visual | No solder bridges, tombstoning, missing components, or lifted pads | Assembly quality |
| 1.6.3 | Conformal coating (if applicable) | Visual under UV | Full coverage of PCB where specified; no bare uncoated areas in moisture-sensitive zones | Water resistance |

---

## Section 2 — In-Process Quality Control (IPQC)

### 2.1 Assembly & Sealing

| # | Check | Method | Acceptance Criteria | Requirement |
|---|-------|--------|---------------------|-------------|
| 2.1.1 | **[CRITICAL]** Hermetic seal integrity — 100% | Air pressure decay or bubble test per unit | Zero leakage detected; passes defined pressure hold test per sealing spec | 5ATM water resistance |
| 2.1.2 | Shell-to-band bond strength | Peel/pull test on sample units | No separation at joint under specified force | Structural integrity |
| 2.1.3 | Charging contacts alignment | Functional test | Contacts make consistent electrical connection with cradle; charge initiates within 3 seconds of seating | Product spec |
| 2.1.4 | Battery installation polarity | Visual + functional check | Correct polarity; device powers on normally | Safety |
| 2.1.5 | Internal component clearance | X-ray or visual inspection before sealing | No component contact with outer shell; clearance within spec to allow for LiPo expansion | Battery safety (swelling risk) |
| 2.1.6 | Adhesive cure | Process control / timed hold | Adhesive fully cured per manufacturer's time-temperature spec before proceeding | Sealing integrity |
| 2.1.7 | Antenna placement | Visual / dimensional check | BLE antenna positioned per approved assembly drawing; no metal contact within exclusion zone | RF performance |

### 2.2 Firmware Flashing

| # | Check | Method | Acceptance Criteria | Requirement |
|---|-------|--------|---------------------|-------------|
| 2.2.1 | **[CRITICAL]** Firmware version | Automated flash station log | Correct production firmware version flashed; version string verified post-flash | Product spec |
| 2.2.2 | Unique device ID / MAC address | Flash station log | Each unit has a unique BLE MAC address assigned and logged | BLE spec |
| 2.2.3 | Flash verification | Checksum / CRC | Firmware CRC matches golden binary; no corruption | Software integrity |
| 2.2.4 | BLE advertisement | BT sniffer / automated test | Device advertises correct service UUID immediately after power-on | BLE spec |

### 2.3 Capacitive Touch Calibration

| # | Check | Method | Acceptance Criteria | Requirement |
|---|-------|--------|---------------------|-------------|
| 2.3.1 | Touch sensitivity calibration | Automated jig | Baseline capacitance reading recorded; calibration offsets written to device | Product spec |
| 2.3.2 | Single tap detection | Automated jig or manual | Single tap registered reliably ≥ 95% of the time across 20 test taps | Gesture reliability |
| 2.3.3 | Double tap detection | Automated jig or manual | Double tap distinguished from single tap reliably ≥ 95% across 20 test sequences | Gesture reliability |
| 2.3.4 | Hold gesture detection | Automated jig or manual | Hold gesture (≥ defined duration) registered reliably ≥ 95% across 20 test sequences | Gesture reliability |
| 2.3.5 | False positive rate | Automated test | Resting false-trigger rate < 1 per 10 minutes of idle | User experience |
| 2.3.6 | Touch through glove / wet skin | Manual test | Confirm behavior is acceptable (or documented limitation) when surface is wet | Real-world use |

---

## Section 3 — Outgoing Quality Control (OQC)

### 3.1 Water & Dust Resistance — Sample Testing

| # | Check | Method | Acceptance Criteria | Requirement |
|---|-------|--------|---------------------|-------------|
| 3.1.1 | **[CRITICAL]** Water resistance — production sample | IEC 60529 / ISO 22810 immersion test at factory on sampled units | Passes 5ATM (50m) immersion for 10 minutes; no water ingress; full functionality post-test | 5ATM claim; ISO 22810 |
| 3.1.2 | Post-immersion functional check | Full functional test suite | All functions pass after water resistance test | Product spec |
| 3.1.3 | Seal integrity — production sample | Pressure decay test on sampled units per lot | Zero failures in sample; any failure triggers 100% test of lot | 5ATM claim |

### 3.2 BLE Connectivity & Range

| # | Check | Method | Acceptance Criteria | Requirement |
|---|-------|--------|---------------------|-------------|
| 3.2.1 | **[CRITICAL]** BLE pairing — 100% | Pair each unit with test device | Pairs within 30 seconds; stable connection maintained | Product spec |
| 3.2.2 | BLE range | Over-the-air test in open space | Maintains connection at ≥ 10 meters (sufficient for glasses-to-ring use case) | Product spec |
| 3.2.3 | BLE reconnection | Drop and reconnect test | Automatically reconnects within 10 seconds after temporary disconnection | User experience |
| 3.2.4 | RF output power | Spectrum analyzer (sample) | TX power within FCC/IC/CE permitted limits; within ±2 dBm of spec | FCC Part 15C compliance |

### 3.3 Touch & Gesture Function — 100% Test

| # | Check | Method | Acceptance Criteria | Requirement |
|---|-------|--------|---------------------|-------------|
| 3.3.1 | **[CRITICAL]** Single tap → AI activate | Automated test jig or manual | Command correctly transmitted to paired device on single tap | Product spec |
| 3.3.2 | **[CRITICAL]** Gesture → call answer | Automated test jig or manual | Call answer gesture correctly transmitted | Product spec |
| 3.3.3 | All defined gesture vocabulary | Automated test jig | Each gesture in the defined vocabulary registers ≥ 95% success over 10 attempts | Product spec |
| 3.3.4 | No ghost touch at rest | Leave idle for 2 minutes | Zero unintended commands sent during idle period | User experience |

### 3.4 Battery & Charging — 100% Test

| # | Check | Method | Acceptance Criteria | Requirement |
|---|-------|--------|---------------------|-------------|
| 3.4.1 | **[CRITICAL]** Charging function | Place on cradle; monitor charge status | Charging initiates within 5 seconds; charge current within spec; device reports charging state | Product spec |
| 3.4.2 | Battery voltage at ship | Multimeter / firmware read | Ships at 40–60% state of charge (prevents deep discharge during transit/storage) | Battery longevity |
| 3.4.3 | Charge cycle to full | Full charge test on sample units | Reaches 100% SOC within specified time; charge current tapers correctly (CC-CV profile) | Battery safety |
| 3.4.4 | Over-charge protection | Apply excess voltage via bench PSU on sample | BMS cuts off charge at correct voltage; no thermal event | UL 62368-1; battery safety |
| 3.4.5 | Battery life — sample | Continuous BLE advertising + touch events | Meets minimum specified battery life target (hours) | Product spec |

### 3.5 Physical & Cosmetic Inspection — 100% Test

| # | Check | Method | Acceptance Criteria | Requirement |
|---|-------|--------|---------------------|-------------|
| 3.5.1 | **[CRITICAL]** Ring size correctness | Ring gauge | Inner diameter matches size code labeled on packaging; ±0.1mm | Sizing accuracy |
| 3.5.2 | Outer shell cosmetic | Visual under standard lighting | Zero Class A defects: scratches, dents, chips, color non-uniformity on visible surfaces | Design spec |
| 3.5.3 | Matte finish uniformity | Visual | No shiny spots, streaks, or coating holidays on outer shell | Design spec |
| 3.5.4 | Inner band finish | Visual | No pitting, corrosion, sharp edges, or burrs on inner bore surfaces | Skin safety / comfort |
| 3.5.5 | Band width and profile | Calipers | Width and wall thickness within ±0.2mm of nominal | Design spec |
| 3.5.6 | No sharp edges or protrusions | Tactile / visual | No sharp edges anywhere; all radii meet minimum spec | Safety / comfort |
| 3.5.7 | Charging contacts condition | Visual + electrical | Contacts clean, not recessed, making consistent electrical connection | Product spec |
| 3.5.8 | Markings / labeling | Visual | Any required regulatory markings (FCC ID, CE, IC, WEEE symbol) present, legible, and correctly placed | FCC / CE marking requirements |

### 3.6 Drop & Mechanical Durability — Sample Testing

| # | Check | Method | Acceptance Criteria | Requirement |
|---|-------|--------|---------------------|-------------|
| 3.6.1 | Drop test | Drop 1m onto hardwood/concrete in 6 orientations | No cracking, shell separation, or functional failure post-drop | Durability |
| 3.6.2 | Bend/squeeze test | Apply lateral force per spec | Shell does not crack or deform permanently under normal wearing forces | Structural integrity |
| 3.6.3 | Thermal cycling — sample | IEC 60068-2-14 or equivalent | No functional failure or cosmetic damage after -20°C to +60°C cycling (5 cycles) | Environmental durability |

### 3.7 Regulatory Marking & Documentation — 100% Per Lot

| # | Check | Method | Acceptance Criteria | Requirement |
|---|-------|--------|---------------------|-------------|
| 3.7.1 | **[CRITICAL]** FCC ID on product or packaging | Visual | FCC ID visible and legible; matches granted FCC ID | FCC Part 15 |
| 3.7.2 | **[CRITICAL]** CE mark (EU units) | Visual | CE mark present and correctly formed on product or packaging | EU RED |
| 3.7.3 | IC ID (Canada units) | Visual | IC ID present and legible | ISED RSS-247 |
| 3.7.4 | WEEE symbol (EU units) | Visual | Crossed-out wheelie bin symbol on packaging | EU WEEE Directive |
| 3.7.5 | Battery recycling label | Visual | Battery chemistry and recycling symbol on product or packaging | EU Battery Regulation |
| 3.7.6 | China RoHS EFUP label | Visual | Environmental Friendly Use Period label on product or packaging | China RoHS SJ/T 11364 |
| 3.7.7 | Country of origin | Visual | "Made in China" (or correct origin) on product and packaging | US CBP marking requirements |
| 3.7.8 | Prop 65 warning (CA units) | Visual | Warning present on product/packaging where required | California Prop 65 |
| 3.7.9 | Serial number / IMEI traceability | Scan barcode | Each unit has unique serial number; scannable; logged in MES system | Traceability / warranty |

### 3.8 Packaging & In-Box Contents — 100% Per Shipment Lot

| # | Check | Method | Acceptance Criteria | Requirement |
|---|-------|--------|---------------------|-------------|
| 3.8.1 | Ring present | Visual / count | Correct ring (size-matched) in box | Order fulfillment |
| 3.8.2 | Magnetic ring charger present | Visual | Charger present; USB-C cable attached or included | In-box spec |
| 3.8.3 | Ring size label on packaging | Visual | Size clearly printed on outer box; matches ring inside | Sizing accuracy |
| 3.8.4 | Packaging integrity | Visual | Box not crushed, wet, or open; seals intact | Shipping integrity |
| 3.8.5 | Recycled packaging declaration | Document / visual | "100% recyclable cardboard" per Mira's sustainability claim; verified with supplier | Brand spec |
| 3.8.6 | Battery shipping label on outer carton | Visual | UN 3481 lithium battery hazmat label on outer shipping carton (for bulk shipments) | IATA / IMDG shipping regulations |

---

## Section 4 — Regulatory Document Package

The following documents must be on file before any production lot is released for shipment. All must be current, valid, and specific to the production unit (not a prior prototype revision).

| # | Document | Required For | Who Provides |
|---|----------|--------------|--------------|
| 4.1 | **[CRITICAL]** FCC Grant of Authorization | US market | Test lab / FCC database |
| 4.2 | **[CRITICAL]** UN 38.3 Test Report (cell-level) | All markets (shipping) | Cell supplier or accredited lab |
| 4.3 | **[CRITICAL]** IEC 62133-2 Certificate (cell-level) | EU/US markets | Cell supplier |
| 4.4 | **[CRITICAL]** EU Declaration of Conformity (RED) | EU market | Mira / Notified Body |
| 4.5 | **[CRITICAL]** EN 1811 Nickel Release Test Report | EU market | Accredited lab |
| 4.6 | RoHS Declaration of Conformity | EU/UK market | Manufacturer + Mira |
| 4.7 | REACH SVHC Declaration | EU market | Manufacturer |
| 4.8 | IC Certification (ISED) | Canada market | Test lab / ISED database |
| 4.9 | UL 62368-1 Test Report | US/Canada market | NRTL |
| 4.10 | Bluetooth SIG End Product Listing (EPL) | All markets (Bluetooth branding) | Mira (via Bluetooth SIG portal) |
| 4.11 | ISO 22810 or IEC 60529 Water Resistance Test Report | All markets (supports 5ATM claim) | Factory or accredited lab |
| 4.12 | CPSIA General Conformity Certificate (GCC) | US market | Manufacturer |
| 4.13 | ISO 10993-10 Skin Sensitization Test Report | All markets (best practice) | Accredited lab |
| 4.14 | Material Data Sheets (IPC-1752A) for all components | All markets | Component suppliers |
| 4.15 | UKCA Declaration of Conformity | UK market | Mira / UK Responsible Person |

---

## Section 5 — Defect Classification

| Class | Definition | Action |
|-------|------------|--------|
| **Critical (C)** | Safety hazard, regulatory non-compliance, or complete functional failure | Zero tolerance — reject unit; halt lot; root cause investigation required |
| **Major (A)** | Functional impairment not a safety risk; cosmetic defect visible at normal viewing distance; sizing error | AQL 1.0 — lot rejected if exceeded |
| **Minor (B)** | Cosmetic defect visible only on close inspection; non-functional deviation from spec with no user impact | AQL 2.5 — lot accepted with corrective action request |

### Critical Defect Examples (auto-reject, zero tolerance)
- Any water ingress during 5ATM test
- BLE fails to pair
- No charging function
- Incorrect ring size vs. label
- Battery thermal event or swelling
- Missing FCC ID / CE mark on production unit
- Wrong firmware version flashed
- Nickel release above 0.5 µg/cm²/week (lot hold)

### Major Defect Examples (AQL 1.0)
- Scratch or chip on outer shell visible at arm's length
- Gesture miss rate > 10% on any gesture type
- Charging initiates but takes > 30 seconds
- Battery ships below 30% SOC
- WEEE or battery recycling symbol missing from packaging

### Minor Defect Examples (AQL 2.5)
- Hairline mark on inner bore not on skin-contact surface
- Packaging box slightly dented but product intact
- Minor color variation vs. golden sample not visible at arm's length

---

## Section 6 — Golden Sample Requirements

Before mass production begins, the following golden samples must be established and held on file:

| # | Golden Sample | Purpose |
|---|---------------|---------|
| 6.1 | Approved production ring (each size SKU) | Color, finish, and dimension reference for all cosmetic and dimensional inspections |
| 6.2 | Approved charging cradle | Reference for magnetic alignment and charging function tests |
| 6.3 | Approved packaging (each variant) | Reference for marking, labeling, and in-box content checks |
| 6.4 | Known-bad battery (swollen/discharged) | Training reference for incoming cell inspection |
| 6.5 | Known-bad nickel release sample (if available) | Training reference for skin-contact surface awareness |

---

## Section 7 — Ongoing Production Monitoring

| Check | Frequency | Action Threshold |
|-------|-----------|-----------------|
| Water resistance sample test | Every production lot (min. 3 units) | Any failure → 100% test of lot; investigation |
| Touch gesture accuracy audit | Every production lot (min. 5 units) | Miss rate > 5% → tune calibration; retest |
| Cosmetic AQL audit | Every lot per AQL 1.0/2.5 plan | Per defect classification table |
| Battery SOC at ship | Every lot (sample) | Any unit < 30% SOC → hold lot |
| Firmware version verification | Every unit (100%) | Any mismatch → reflash and verify |
| Regulatory document currency | Quarterly | Any expired cert → halt production until renewed |
| EN 1811 nickel retest | Annually or on any material/supplier change | Failure → halt lot; material change required |
