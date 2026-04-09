# MiraCase — Quality Control Checklist
*Based on device-summary.md and industry-standards.md — April 2026*

---

## How to Use This Checklist

- **IQC (Incoming Quality Control):** Performed on components before assembly
- **IPQC (In-Process Quality Control):** Performed during assembly on the line
- **OQC (Outgoing Quality Control):** Performed on finished units before shipment
- **AQL:** Acceptable Quality Level — use AQL 1.0 for critical defects, AQL 2.5 for major, AQL 4.0 for minor per ANSI/ASQ Z1.4

---

## Section 1 — Incoming Quality Control (IQC)

### 1.1 Shell / Enclosure

| # | Check | Method | Spec |
|---|-------|--------|------|
| 1.1.1 | Shell dimensions (L × W × H) | Calipers | Within ±0.3mm of approved drawing |
| 1.1.2 | Hinge / latch mechanism operation | Manual operation × 200 cycles | Opens and closes smoothly; no binding or cracking |
| 1.1.3 | Surface finish — leather or metal | Visual + tactile | No peeling, bubbling, scratching, or color deviation from approved sample |
| 1.1.4 | Interior lining — microfiber/velvet | Visual + tactile | No loose threads, tears, or glue bleed-through; full coverage of all contact surfaces |
| 1.1.5 | Material RoHS declaration | Supplier DoC | Written declaration confirming RoHS 3 compliance for all materials |
| 1.1.6 | REACH SVHC declaration | Supplier DoC | Written declaration that no SVHC exceed 0.1% w/w |
| 1.1.7 | Drop / impact resistance (sample) | 1m drop onto concrete × 4 faces | Shell does not crack; interior lining remains seated |

### 1.2 Internal Battery (Li-Po Cell)

| # | Check | Method | Spec |
|---|-------|--------|------|
| 1.2.1 | Capacity | Charge/discharge cycle | ≥ rated capacity (minimum 500mAh) |
| 1.2.2 | Nominal voltage | Multimeter | 3.6–3.7V nominal |
| 1.2.3 | UN 38.3 test report | Document review | Valid UN 38.3 test report from accredited lab on file |
| 1.2.4 | IEC 62133-2 certification | Document review | Certificate on file from accredited lab |
| 1.2.5 | UL 2054 certification | Document review | UL listing or equivalent on file |
| 1.2.6 | Cell dimensions | Calipers | Matches approved drawing; fits designated battery pocket without stress |
| 1.2.7 | Cell marking / labeling | Visual | Capacity (mAh + Wh), chemistry, voltage, manufacturer, date code legible on cell |
| 1.2.8 | Protection circuit module (PCM) | Visual + electrical | PCM present; overcurrent, overvoltage, undervoltage protection confirmed functional |
| 1.2.9 | RoHS / REACH declaration | Supplier DoC | Written declaration on file |

### 1.3 PCB / Charge Controller

| # | Check | Method | Spec |
|---|-------|--------|------|
| 1.3.1 | PCB dimensions | Calipers | Fits designated PCB pocket; within ±0.2mm |
| 1.3.2 | Solder quality | Visual under 10× magnification | No cold joints, bridges, missing components, or tombstoning |
| 1.3.3 | Component placement | Visual vs. BOM/schematic | All components present and correctly oriented |
| 1.3.4 | USB-C port alignment | Calipers + fit check | Port centered within ±0.5mm of shell opening; connector mates fully |
| 1.3.5 | IEC 62368-1 / UL 62368-1 compliance | Document review | Test report or certification on file for charging circuit |
| 1.3.6 | FCC Part 15B pre-scan (sample) | EMC pre-scan | Emissions within Class B limits |
| 1.3.7 | RoHS solder compliance | Supplier DoC | Lead-free solder (Sn/Ag/Cu) confirmed; no RoHS-restricted substances |

### 1.4 Pogo Pins / Magnetic Contacts (Glasses Charging Interface)

| # | Check | Method | Spec |
|---|-------|--------|------|
| 1.4.1 | Pin spring force | Force gauge | Within spec range (typically 50–150g per pin); consistent across all pins |
| 1.4.2 | Pin travel / stroke | Calipers | Full travel within spec; pins do not stick or bind |
| 1.4.3 | Contact resistance | Milliohm meter | < 50mΩ per pin at rated spring force |
| 1.4.4 | Pin plating | Visual + supplier DoC | Gold-plated (Au ≥ 0.2µm) or as specified; no oxidation |
| 1.4.5 | Pin cycle life | Supplier test report | ≥ 10,000 mating cycles rated |
| 1.4.6 | Positional accuracy | Fixture + calipers | Pin center positions within ±0.15mm of drawing |

### 1.5 Ring Charging Dock / Magnetic Charger

| # | Check | Method | Spec |
|---|-------|--------|------|
| 1.5.1 | Magnetic holding force | Force gauge | Sufficient to retain ring in dock during normal handling; ring does not fall out when case is inverted |
| 1.5.2 | Output voltage / current | Multimeter + load | Matches spec (e.g., 5V / rated mA); within ±5% |
| 1.5.3 | Ring fit — size range | Physical test with size 7 and size 14 rings | Both sizes seat properly and make contact |
| 1.5.4 | Contact resistance | Milliohm meter | < 100mΩ at full contact |

### 1.6 LED Indicator

| # | Check | Method | Spec |
|---|-------|--------|------|
| 1.6.1 | LED illumination — all states | Functional test (charging, full, low battery) | Correct color/blink pattern per spec for each state |
| 1.6.2 | LED brightness | Visual in normal lighting | Clearly visible; not excessively bright (no glare) |
| 1.6.3 | LED lens / diffuser | Visual | No cracks, cloudiness, or color deviation from approved sample |

### 1.7 USB-C Port

| # | Check | Method | Spec |
|---|-------|--------|------|
| 1.7.1 | Connector mating | Physical test with USB-C cable | Full insertion; no excessive play; no unintended disconnection |
| 1.7.2 | USB-C retention force | Pull gauge | Within USB-IF spec; cable does not pull out under 10N |
| 1.7.3 | USB-IF compliance documentation | Document review | USB-C connector from USB-IF certified vendor, or compliance evidence on file |

---

## Section 2 — In-Process Quality Control (IPQC)

### 2.1 Assembly

| # | Check | Method | Spec |
|---|-------|--------|------|
| 2.1.1 | Battery orientation | Visual before enclosure close | Correct polarity; no reversal |
| 2.1.2 | Battery connector seating | Visual + tug test | Connector fully seated; will not pull free under 5N |
| 2.1.3 | PCB mounting | Visual | PCB fully seated in standoffs/posts; no flex or rattle |
| 2.1.4 | Wire routing | Visual | No pinched wires at case closure points; no contact with sharp edges |
| 2.1.5 | Pogo pin assembly | Visual + function | Pins spring freely; correct orientation; wires soldered to correct pads |
| 2.1.6 | Interior lining installation | Visual | Lining seated flat with no wrinkles, bubbles, or exposed adhesive |
| 2.1.7 | Ring dock installation | Visual + fit test | Dock centered and secured; ring seats and contacts align |
| 2.1.8 | Shell closure / snap fit | Manual | Case closes flush with no gap > 0.3mm; latch engages positively |
| 2.1.9 | No foreign objects inside case | Visual before close | No debris, wire clippings, or foreign material |

### 2.2 First Article Inspection (FAI) — Per Production Run

| # | Check | Method | Spec |
|---|-------|--------|------|
| 2.2.1 | First 5 units fully inspected against drawing | Full dimensional check | All dimensions within tolerance |
| 2.2.2 | Functional test on first article | Full functional test sequence | Pass all OQC checks before run continues |
| 2.2.3 | Charging alignment with Mira Glasses | Physical fit with production glasses unit | Glasses seat correctly; pogo pins or magnetic contacts engage fully |
| 2.2.4 | Charging alignment with Mira Ring | Physical fit with production ring unit | Ring seats in dock; charging initiates |

---

## Section 3 — Outgoing Quality Control (OQC)

All finished units sampled per AQL 1.0 (critical) / AQL 2.5 (major) / AQL 4.0 (minor) from ANSI/ASQ Z1.4.

### 3.1 Functional — Charging Performance

| # | Check | Method | Spec | Class |
|---|-------|--------|------|-------|
| 3.1.1 | USB-C input charging | Connect USB-C 5V/2A; verify LED indicates charging | LED activates; battery voltage rises | Critical |
| 3.1.2 | Glasses charging output — pogo pin or magnetic | Insert glasses; measure voltage at charging contacts | Output voltage matches glasses charging spec; glasses begin charging | Critical |
| 3.1.3 | Ring charging output | Insert ring; verify charging initiates | Ring charging confirmed (ring LED indicates charging) | Critical |
| 3.1.4 | Simultaneous charging (glasses + ring + USB-C in) | All three active simultaneously | Both devices charge without thermal cutoff or error | Critical |
| 3.1.5 | Charge completion / cutoff | Charge to 100%; monitor | Charging stops or tapers at full charge; no overcharge | Critical |
| 3.1.6 | Battery protection — short circuit | Apply momentary short to output contacts | PCM activates; no damage; recovers after short removal | Critical |
| 3.1.7 | Battery protection — overdischarge | Drain battery to cutoff voltage | PCM cuts off before cell voltage drops below 2.5V | Critical |
| 3.1.8 | LED indicator states | Cycle through all states | Charging: correct indicator; Full: correct indicator; Low battery: correct indicator | Major |
| 3.1.9 | Pass-through charging (if supported) | USB-C in while glasses/ring connected | Devices charge from wall while case battery also charges | Major |

### 3.2 Physical / Dimensional

| # | Check | Method | Spec | Class |
|---|-------|--------|------|-------|
| 3.2.1 | Overall dimensions | Calipers | Within ±0.5mm of approved drawing | Major |
| 3.2.2 | Glasses fit | Insert production Mira Glasses | Glasses seat fully with no force; lenses do not contact hard surfaces | Critical |
| 3.2.3 | Ring fit (size 7 and size 14) | Insert size 7 and size 14 rings | Both sizes seat; neither falls out under gravity inversion | Major |
| 3.2.4 | Case closure | Close and inspect | Flush closure; gap ≤ 0.3mm; latch engages positively | Major |
| 3.2.5 | Hinge / latch operation | Open/close × 20 | Smooth operation; no binding, cracking, or deformation | Major |
| 3.2.6 | USB-C port accessibility | Insert and remove cable × 5 | Full insertion/removal with no obstruction | Major |

### 3.3 Cosmetic / Appearance

| # | Check | Method | Spec | Class |
|---|-------|--------|------|-------|
| 3.3.1 | Exterior surface — leather | Visual under standard lighting | No scratches, cuts, peeling, uneven color, or glue bleed | Major |
| 3.3.2 | Exterior surface — metal/silver | Visual under standard lighting | No scratches > 5mm, dents, oxidation, or plating defects | Major |
| 3.3.3 | Interior lining | Visual | No tears, loose edges, wrinkles, or adhesive visible | Major |
| 3.3.4 | LED window / lens | Visual | No cracks, cloudiness, misalignment | Minor |
| 3.3.5 | Branding / marking | Visual | Correct; properly positioned; no smearing or misalignment | Minor |
| 3.3.6 | Color match to approved sample | Visual vs. approved limit sample | Within approved color tolerance | Major |
| 3.3.7 | No foreign material / contamination | Visual | Interior clean; no debris, fingerprints on interior lining | Minor |

### 3.4 Safety & Compliance

| # | Check | Method | Spec | Class |
|---|-------|--------|------|-------|
| 3.4.1 | Required labels present | Visual | FCC, CE (if applicable), WEEE, battery capacity (Wh), lithium battery caution label — all present and legible | Critical |
| 3.4.2 | Pogo pin / contact accessibility | Touch test with fingertip | Contacts recessed or spring-retracted when no device present; no accessible live contact at > 42.4V peak | Critical |
| 3.4.3 | Thermal — charging session | Charge for 60 min in ambient 25°C | Exterior case surface temperature ≤ 45°C | Critical |
| 3.4.4 | No battery swelling | Visual | No case deformation or bulging indicating cell swelling | Critical |
| 3.4.5 | Drop test (sample — 5 units per lot) | 1m drop, 4 faces onto concrete | No cracking of shell; all functions pass post-drop | Major |
| 3.4.6 | Regulatory documentation packet | Document review | UN 38.3, IEC 62133-2, UL 2054, IEC/UL 62368-1, FCC test report — all on file and current | Critical |

### 3.5 Packaging

| # | Check | Method | Spec | Class |
|---|-------|--------|------|-------|
| 3.5.1 | Lithium battery outer carton label | Visual | "LITHIUM ION BATTERY" IATA/DOT caution label affixed to outer shipping carton | Critical |
| 3.5.2 | Product packaging — labels | Visual | CE, FCC, WEEE, recycling symbols present on retail packaging | Major |
| 3.5.3 | Packaging integrity | Visual + drop | Retail packaging undamaged; product secured inside without movement | Minor |
| 3.5.4 | Accessory completeness | Contents check | All included items per BOM present in box | Major |
| 3.5.5 | Serial number / traceability label | Visual + scan | S/N label present, scannable, matches production records | Major |

---

## Section 4 — Reliability & Durability Testing (Type / Qualification Testing)

Performed on pre-production samples and at major design/tooling changes. Not 100% lot inspection.

| # | Test | Standard Reference | Spec |
|---|------|--------------------|------|
| 4.1 | Hinge cycle life | Internal procedure | 5,000 open/close cycles; no structural failure |
| 4.2 | Latch retention | Internal procedure | Latch holds case closed under 20N lateral force |
| 4.3 | Charge cycle life — internal battery | IEC 62133-2 ref. | ≥ 300 full charge/discharge cycles to ≥ 80% capacity retention |
| 4.4 | Temperature storage | IEC 60068-2-1/2 | Functional after 72h at -20°C and 72h at 60°C |
| 4.5 | Humidity exposure | IEC 60068-2-78 | Functional after 96h at 40°C / 93% RH |
| 4.6 | Pogo pin contact cycle life | Internal procedure | 10,000 insertion cycles; contact resistance remains < 100mΩ |
| 4.7 | USB-C port insertion life | USB-IF standard | 10,000 mating cycles; port remains functional |
| 4.8 | Vibration (shipping simulation) | ISTA 2A or ASTM D4169 | No damage or functional failure after simulated shipping profile |
| 4.9 | EMC pre-compliance scan | FCC 15B / CISPR 32 | Emissions within Class B limits at pre-compliance lab |
| 4.10 | Thermal runaway / overcharge abuse | IEC 62133-2 | No fire, explosion, or venting with flame; PCM prevents overcharge |

---

## Section 5 — Defect Classification Summary

| Class | Definition | Disposition |
|-------|-----------|-------------|
| **Critical** | Safety hazard (fire, shock, injury risk) or regulatory non-compliance (missing certifications, unlabeled lithium battery) | 100% inspection; zero tolerance; reject lot |
| **Major** | Functional failure or defect that renders product unusable or significantly degrades user experience | AQL 1.0 sampling; reject lot if exceeded |
| **Minor** | Cosmetic or non-functional deviation from spec that does not affect usability | AQL 2.5 sampling; accept with documented deviation if below AQL |

---

## Section 6 — Required Documentation Packet (Per Lot)

| Document | Source |
|----------|--------|
| UN 38.3 test report (battery cell) | Battery supplier |
| IEC 62133-2 certificate (battery cell) | Battery supplier |
| UL 2054 certificate or equivalent (battery) | Battery supplier |
| IEC/UL 62368-1 test report (finished product) | Accredited test lab |
| FCC Part 15B test report | Accredited test lab |
| CE Declaration of Conformity (DoC) | Mira / contract manufacturer |
| RoHS compliance declarations — all key components | Component suppliers |
| REACH SVHC declarations — all key components | Component suppliers |
| Production lot inspection report (IQC + OQC) | Contract manufacturer |
| Certificate of Conformance (CoC) | Contract manufacturer |
| Packing list with S/N range | Contract manufacturer |
