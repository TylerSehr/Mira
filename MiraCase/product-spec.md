# MiraCase — Product Specification
*Version 1.0 — April 2026*

---

## 1. Product Overview

| Field | Value |
|-------|-------|
| Product name | MiraCase |
| Product type | Charging case for Mira Glasses + Mira Ring |
| Manufacturer | TBD (Chinese OEM/ODM — Shenzhen) |
| Target market | United States (primary); EU, UK (secondary) |
| Production volume | 2,000 units total; 500 units/month run rate |
| Target lead time | ≤ 2 months from PO to first shipment |
| Target ex-factory unit cost | TBD (to be determined from BOM + supplier quotes) |

### 1.1 Purpose

The MiraCase is a premium carry and charging case that houses, protects, and simultaneously charges both the Mira Glasses and Mira Ring. It consolidates the existing separate magnetic glasses charger and magnetic ring charger accessories into a single self-contained case, rechargeable via USB-C. The case is included with the Mira system and must reflect Mira's premium product positioning.

---

## 2. Compatibility

| Device | Interface | Notes |
|--------|-----------|-------|
| Mira Glasses | Pogo pin contacts (preferred) or integrated magnetic charging dock | Glasses frame width 145.6mm; charging contacts located on temple arm; 5V charging, 40-min full charge time |
| Mira Ring | Magnetic ring charging dock | Ring sizes 7–14; 5ATM water resistant; small Li-Po cell |

The case must be validated for charging compatibility with production Mira Glasses and Ring units before mass production approval.

---

## 3. Mechanical Specification

### 3.1 Exterior Dimensions

| Parameter | Value |
|-----------|-------|
| Exterior length | TBD in design phase — must accommodate glasses (140mm W × 150mm D) with margin |
| Exterior width | TBD — minimum ~160mm to clear glasses frame width of 145.6mm + lining thickness |
| Exterior height (closed) | TBD — minimum ~55mm to accommodate glasses height (45mm) + lining + PCB stack |
| Wall thickness | ≥ 2.5mm (hard shell); ≥ 1.5mm minimum at thinnest section |
| Weight (complete unit, empty) | Target < 200g; TBD after material selection |

*Note: Exact exterior dimensions to be finalized in 3D CAD during tooling design phase. All above are minimum functional envelopes.*

### 3.2 Shell Construction

| Parameter | Spec |
|-----------|------|
| Shell material — option A (silver/chrome) | Die-cast zinc alloy (Zamak 3 or equivalent) with chrome or brushed silver plating; or injection-molded ABS with vacuum-metallized chrome finish |
| Shell material — option B (leather) | Injection-molded ABS rigid inner shell with genuine leather or PU leather exterior wrap; leather thickness ≥ 1.0mm; bonded with contact cement |
| Preferred material | To be confirmed by Mira design approval |
| Shell color | Silver/chrome (option A) or Matte Black with leather wrap (option B) |
| Interior lining | Microfiber or short-pile velvet; full coverage of all interior surfaces that contact the glasses or ring; no hard surface exposed to lens or frame contact |
| Closure type | Magnetic latch (preferred) — concealed magnets in shell lip; closes flush with tactile snap |
| Hinge type | Dual barrel metal hinge (stainless steel or zinc alloy); integrated into shell at rear edge |
| Hinge open angle | 90°–110° (sufficient to remove glasses single-handed) |

### 3.3 Interior Layout

```
[Case open — interior view, lower shell]

┌─────────────────────────────────────────────────┐
│                                                 │
│    [Glasses cradle — soft-lined contoured]      │
│    145.6mm wide seating zone                    │
│    Glasses rest temples-down                    │
│    Pogo pins / magnetic contacts at             │
│    temple arm position                          │
│                                                 │
│  ┌──────────┐    ┌──────────────────────────┐   │
│  │Ring dock │    │  PCB / battery zone      │   │
│  │(magnetic)│    │  (concealed under lining)│   │
│  └──────────┘    └──────────────────────────┘   │
│                                                 │
│  [USB-C port]   [LED indicator window]          │
│  (short edge)   (short edge or lid)             │
└─────────────────────────────────────────────────┘
```

- Glasses sit in the lower shell, lenses facing up, temples resting in contoured cradle
- Ring dock positioned in lower shell at a corner or side zone not occupied by glasses
- PCB and battery are beneath the lining, not accessible to user
- USB-C port and LED indicator accessible on exterior of closed case

### 3.4 Drop & Impact Resistance

| Parameter | Spec |
|-----------|------|
| Drop height | 1.0m onto concrete; 4 faces + 4 edges |
| Post-drop requirement | Shell intact (no cracks); all functions pass; glasses inside undamaged |
| Interior protection | Glasses must not shift > 5mm from seated position during drop |

### 3.5 Hinge & Latch Life

| Parameter | Spec |
|-----------|------|
| Hinge rated cycle life | ≥ 5,000 open/close cycles |
| Latch rated cycle life | ≥ 5,000 open/close cycles |
| Post-life-test requirement | Full function; no structural failure; closure gap ≤ 0.5mm |

---

## 4. Electrical Specification

### 4.1 Internal Battery

| Parameter | Spec |
|-----------|------|
| Chemistry | Lithium-polymer (Li-Po) |
| Nominal voltage | 3.7V |
| Minimum capacity | 500mAh |
| Recommended capacity | 1,000–2,000mAh (for meaningful glasses top-up charge) |
| Maximum dimensions | To fit within shell envelope — TBD in design phase |
| Operating charge temperature | 0°C to +45°C |
| Operating discharge temperature | -20°C to +60°C |
| Storage temperature | -20°C to +35°C recommended |
| Self-discharge rate | ≤ 3% per month at 25°C [INFERRED typical] |
| Protection | Integrated PCM required: overcurrent, overvoltage (≤ 4.25V cutoff), overdischarge (≥ 2.5V cutoff), short-circuit |
| Required certifications | UN 38.3, IEC 62133-2, UL 2054 |

### 4.2 USB-C Input

| Parameter | Spec |
|-----------|------|
| Connector type | USB-C receptacle (female) |
| Input voltage | 5V |
| Input current | 2A nominal (10W max) |
| Charging protocol | Standard 5V/2A; USB-PD not required but acceptable |
| Connector mating life | ≥ 10,000 cycles |
| ESD protection | IEC 61000-4-2 Level 4 rated TVS on input |
| USB-IF compliance | Connector from USB-IF certified vendor |

### 4.3 Glasses Charging Output (Pogo Pin Interface)

| Parameter | Spec |
|-----------|------|
| Interface type | Pogo pin contact (spring-loaded, gold-plated) |
| Number of contacts | 2 minimum (VCC + GND); expand to match Mira Glasses charging pad layout |
| Output voltage | 5V (to match glasses magnetic charger spec) |
| Output current | ≥ 1A (match glasses 40-min charge requirement) |
| Contact plating | Au ≥ 0.3µm over Ni |
| Spring force per pin | 80–150g |
| Contact cycle life | ≥ 10,000 mating cycles |
| Contact resistance | < 50mΩ per pin at rated spring force |
| Positional accuracy | Pin centers within ±0.15mm of drawing |
| Short-circuit protection | Output current-limited; PCM/IC protects against dead short |
| Touch safety | Contacts recessed or spring-retracted when no device present; output voltage ≤ 42.4V peak (inherently safe at 5V) |

### 4.4 Ring Charging Output (Magnetic Dock)

| Parameter | Spec |
|-----------|------|
| Interface type | Magnetic contact dock (contact-based preferred; Qi coil optional) |
| Output voltage | Per Mira Ring charging spec (5V assumed [INFERRED] — to be confirmed) |
| Output current | Per Mira Ring charging spec (500mA assumed [INFERRED]) |
| Ring size compatibility | Sizes 7–14 (inner diameter 17.3mm–23.0mm) |
| Magnetic retention | Ring held in dock under gravity inversion (case inverted upside-down) |
| Contact resistance | < 100mΩ at full engagement |
| Interference | Dock magnets must not corrupt ring BLE pairing data or MCU memory |

### 4.5 Charge Management System

| Parameter | Spec |
|-----------|------|
| Architecture | Power bank IC (e.g., IP5306-class or equivalent); manages: USB-C input → Li-Po charge + simultaneous output regulation to glasses + ring outputs |
| Pass-through charging | Supported: wall power (USB-C in) charges case battery AND case simultaneously charges glasses + ring |
| Output boost | 5V regulated boost output from 3.7V Li-Po cell |
| Charging priority | Simultaneous charging of both glasses and ring when case is plugged in |
| Standby current drain | ≤ 100µA (case with devices not present and not charging) |
| Over-temperature protection | Charging IC thermally derated or shut down if internal temp > 60°C |
| Thermal design | No external surface to exceed 45°C during 60-min charging session at 25°C ambient |

### 4.6 LED Indicator

| Parameter | Spec |
|-----------|------|
| Number of LEDs | 1–3 (single RGB LED preferred for minimal PCB footprint) |
| Indicator states | Charging (USB-C connected): pulsing or solid amber/red; Full charge: solid green; Low internal battery (≤ 20%): solid or blinking red; Idle (no USB-C, no device): off or dim |
| Visibility | Clearly visible in ambient office lighting; not blindingly bright |
| Viewing angle | ≥ 120° (diffused via light pipe) |
| Light pipe | Clear or frosted polycarbonate; flush with or recessed 0.5mm from exterior surface |

---

## 5. Charging Performance Specification

| Parameter | Spec |
|-----------|------|
| Time to charge Mira Glasses (0→100%) | ≤ 50 minutes (glasses native charge time is 40 min; case output must sustain ≥ 1A at 5V) |
| Time to charge Mira Ring (0→100%) | TBD — to be measured with production ring unit |
| Time to charge case internal battery (0→100%) via USB-C 5V/2A | TBD — dependent on final battery capacity selection |
| Simultaneous charging efficiency | Both glasses and ring must charge to 100% without thermal shutdown |
| Glasses charge passes through closed case | Yes — case does not need to be open to charge glasses |
| Ring charge passes through closed case | Yes — ring charges in dock regardless of lid state |

---

## 6. Environmental Specification

| Parameter | Spec |
|-----------|------|
| Operating temperature | 0°C to +45°C |
| Storage temperature | -20°C to +60°C |
| Operating humidity | 15%–85% RH, non-condensing |
| IP rating (case itself) | Not required; case is not waterproof — no IP claim unless specifically added |
| Altitude (storage/shipping) | Per UN 38.3 test requirements (up to 15,000m simulated for air freight) |

---

## 7. Regulatory & Compliance Specification

| Requirement | Standard | Market |
|-------------|----------|--------|
| Battery transport | UN 38.3 | All markets |
| Battery safety (cell) | IEC 62133-2, UL 2054 | US + international |
| Electrical safety | IEC 62368-1, UL 62368-1 | US + international |
| US EMC emissions | FCC Part 15B Subpart B (Class B) | US |
| Canadian EMC | ICES-003 | Canada |
| EU EMC emissions | EN 55032 / CISPR 32 | EU |
| EU EMC immunity | EN 55035 / CISPR 35 | EU |
| EU Low Voltage | LVD 2014/35/EU | EU |
| EU Battery Regulation | EU 2023/1542 | EU |
| RoHS | RoHS 3 (EU 2015/863) | EU + US best practice |
| REACH | REACH Regulation 1907/2006 | EU |
| WEEE | WEEE Directive 2012/19/EU | EU |
| UK CE equivalent | UKCA | UK |
| California chemicals | Proposition 65 | California (US) |
| Air freight compliance | IATA DGR Section II (UN3481) | All markets |
| US domestic shipping | DOT 49 CFR | US |
| USB-C connector | USB-IF compliance | All markets |

**CE marking:** Required. Technical file must include DoC signed by Mira (or authorized representative) covering LVD, EMC Directive, Battery Regulation, and RoHS.

**FCC:** SDoC (Supplier Declaration of Conformity) approach acceptable for Class B unintentional radiator. FCC ID not required if no intentional radio transmitter in the case.

---

## 8. Labeling Specification

All labels must be permanent (not removable by hand), legible at normal reading distance, and durable for product lifetime.

| Label | Location | Required Content |
|-------|----------|-----------------|
| Product / compliance label | Exterior bottom or inside lid | Model name, input rating (5V/2A), battery capacity (mAh + Wh), FCC SDoC statement, CE mark (EU), UKCA mark (UK), WEEE symbol, manufacturer name and address, country of origin |
| Serial number label | Exterior bottom or inside lid | Unique S/N per unit; scannable barcode (QR or 1D) |
| Battery caution label | Inside case or on battery | "Li-Po battery — do not puncture, incinerate, or short circuit" |
| Lithium battery shipping label | Outer carton | IATA "LITHIUM ION BATTERY" caution label, UN3481 marking |
| Recycling symbol | Retail packaging | Chasing arrows recycling symbol; "100% recyclable packaging" |
| Prop 65 warning | Retail packaging (California) | Required if applicable chemicals detected in materials |

---

## 9. Packaging Specification

| Parameter | Spec |
|-----------|------|
| Retail box material | Rigid or folding paperboard; 100% recyclable |
| Inner insert | Molded pulp tray or PETG thermoform; holds case securely with no movement |
| In-box accessories | MiraCase unit; Quick Start Guide; (USB-C cable not included — Mira Glasses USB-C adapter already in main box) |
| Branding | Mira brand mark and MiraCase product name on exterior of box |
| Languages (user guide) | English (US launch); add DE, FR, ES, IT for EU |
| Outer carton (export) | Double-wall corrugated; printed lithium battery hazard labels; quantity per master carton TBD |
| Carton drop test | ISTA 2A or ASTM D4169 — no damage after simulated shipping profile |

---

## 10. Appearance & Industrial Design Specification

### 10.1 Approved Design Directions

Two design directions are under consideration, subject to Mira approval:

**Option A — Silver/Chrome Hard Shell**
- Organic sculptural form (pebble / soft geometric)
- Die-cast zinc alloy or chrome-plated ABS
- Polished or brushed chrome exterior finish
- Minimal visible seam lines
- Reference: image (2).webp (sculptural chrome pebble case) and image (1).webp (Gentle Monster silver case)

**Option B — Black Leather Soft Case**
- Structured rigid interior with leather or PU leather exterior
- Black; smooth or lightly grained leather texture
- Curved profile following Mira Glasses frame contour
- Minimal stitching visible on exterior
- Reference: image (3).webp (Hermès-style black leather glasses case)

### 10.2 Appearance Standards

| Parameter | Spec |
|-----------|------|
| Exterior scratches (accepted) | None > 3mm length in critical viewing zones (top/front faces) |
| Exterior dents (accepted) | None visible at 500mm viewing distance |
| Leather peeling / bubbling | Zero tolerance at OQC |
| Chrome plating pits or voids | None visible at 500mm viewing distance |
| Interior lining — loose edges | Zero tolerance |
| Closure gap (closed) | ≤ 0.3mm measured at any point along seam |
| Color match to approved limit sample | Within approved deviation |
| LED indicator alignment | Centered within window ± 0.5mm |

---

## 11. Production Specification

| Parameter | Value |
|-----------|-------|
| Total order quantity | 2,000 units |
| Monthly run rate | 500 units/month |
| Sample quantity (pre-production) | 5–10 engineering samples (EVT); 20–50 units (DVT/PVT) |
| Packaging unit | Individual retail box |
| Master carton quantity | TBD (suggest 10–20 units per master carton given battery weight and case size) |
| Country of origin | China (Shenzhen region preferred) |
| Target ex-factory cost | TBD — to be informed by BOM and supplier quotes |
| Payment terms | TBD — standard 30% deposit / 70% before shipment |
| Incoterms | FOB Shenzhen (or nearest port) |
| Shelf life | ≥ 2 years from manufacture date (battery self-discharge and degradation limited) |

### 11.1 Production Milestones

| Milestone | Description |
|-----------|-------------|
| EVT (Engineering Validation Test) | First physical samples; validate mechanical fit with Mira Glasses + Ring, charging function, and basic safety |
| DVT (Design Validation Test) | Refined samples; full electrical, mechanical, and regulatory pre-compliance testing |
| PVT (Production Validation Test) | Production-intent tooling and process; full OQC run; regulatory lab testing initiated |
| MP (Mass Production) | Full run; all regulatory certifications on file; OQC per checklist |

---

## 12. Open Items & Assumptions

| Item | Status | Notes |
|------|--------|-------|
| Mira Glasses pogo pin / charging contact exact layout | **Assumed** — must be confirmed with Mira hardware team before tooling | Contact positions, voltage, current draw |
| Mira Ring charging voltage and current | **Assumed 5V / 500mA** — must be confirmed | Affects ring dock output spec |
| Final case material (leather vs. silver) | **TBD — Mira design decision** | Affects tooling approach, supplier type, and unit cost |
| Final battery capacity | **Assumed 1,000–2,000mAh** — must be confirmed with final shell dimensions | Larger battery preferred for user experience |
| Ring dock interface type (contact vs. Qi coil) | **Preferred: magnetic contact** — confirm compatibility with ring charging circuit | Qi would add coil + WPC certification requirement |
| USB-C cable inclusion in box | **Assumed not included** (already in main Mira box) — confirm with Mira product team | Affects packaging spec and BOM |
| IP rating for case | **None planned** — confirm no IP claim required | Adding IP sealing would significantly increase cost and tooling complexity |
| Mira Ring size range | **Assumed sizes 7–14** per ring sourcing notes | Confirm with Mira; affects dock diameter range |
