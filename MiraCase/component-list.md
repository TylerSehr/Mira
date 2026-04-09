# MiraCase — Component List
*Based on device-summary.md, industry-standards.md — April 2026*

---

## How to Read This List

- **Qty/Unit:** Quantity per finished MiraCase unit
- **Regulatory flag:** Components with active certification requirements called out explicitly
- **[INFERRED]:** Where exact spec is not yet locked, industry-standard equivalent noted

---

## 1. Enclosure & Mechanical

| # | Component | Description | Key Specs | Qty/Unit | Regulatory / Notes |
|---|-----------|-------------|-----------|----------|--------------------|
| 1.1 | Outer shell — upper half | Rigid case lid; holds interior lining and glasses | Material: ABS + leather wrap (soft option) or zinc alloy die-cast (silver/chrome option); external dimensions to be confirmed in design phase | 1 | RoHS material declaration required; no restricted pigments in leather dye |
| 1.2 | Outer shell — lower half | Rigid case base; houses PCB, battery, charging interfaces | Same material as upper; must include PCB mounting bosses, battery pocket, pogo/magnetic contact cutouts, USB-C port cutout, LED window | 1 | RoHS declaration required |
| 1.3 | Leather / PU wrap — upper | Decorative and tactile exterior covering for upper shell | Genuine leather or PU leather; color: TBD (black preferred); bonded to shell with contact adhesive; ≥ 1.0mm thickness | 1 | REACH SVHC check on dyes and adhesives; Prop 65 check on chromium (if genuine leather) |
| 1.4 | Leather / PU wrap — lower | Same as 1.3 for lower shell | Same material and spec | 1 | Same as 1.3 |
| 1.5 | Interior lining — upper | Soft lining preventing lens contact with hard surfaces | Microfiber or velvet; bonded to interior shell contours; full coverage of all surfaces glasses will contact | 1 | No sharp edges or exposed adhesive permissible; glasses lenses must not contact hard surface |
| 1.6 | Interior lining — lower | Soft lining for lower shell interior (glasses temple rest area, ring dock surround) | Same material as upper; pre-cut for pogo pin, USB-C, and ring dock access | 1 | Same as 1.5 |
| 1.7 | Hinge assembly | Connects upper and lower shell; allows case to open/close | Metal (stainless steel or zinc alloy); rated ≥ 5,000 cycles; smooth torque profile; no sharp protrusion when open or closed | 1 set (2 hinge barrels typical) | Must not create pinch point accessible per IEC 62368-1 mechanical safety |
| 1.8 | Latch / magnetic closure | Keeps case closed during transport | Magnetic latch (preferred for tool-free operation) or snap latch; holding force sufficient to resist casual opening; must not interfere with glasses charging magnets | 1 | Magnet field must not degrade glasses or ring BLE / charging magnets; test for interference |
| 1.9 | Glasses seating cradle / foam insert | Contoured interior form to hold glasses in correct position for pogo pin alignment | EVA foam or thermoformed insert; contoured to Mira Glasses frame profile (145.6mm wide); positions glasses precisely over charging contacts; covered by lining | 1 | Dimensionally critical — pogo pin alignment tolerance ±0.5mm |
| 1.10 | Rubber / silicone bumpers | Corner and edge protection for glasses inside case | Silicone or TPE; bonded to cradle or lining; protects temple arms and frame edges | 4–6 | RoHS declaration required |
| 1.11 | Assembly screws | PCB and subassembly mounting | M2 × 4mm self-tapping or machine screws; stainless steel | 4–8 | — |
| 1.12 | Structural adhesive | Bonding shell halves, lining, wrap, and subassemblies | Two-part epoxy or contact cement as appropriate per substrate; must be compatible with ABS, leather, and microfiber | As required | REACH SVHC check; no benzene-class solvents |

---

## 2. Battery System

| # | Component | Description | Key Specs | Qty/Unit | Regulatory / Notes |
|---|-----------|-------------|-----------|----------|--------------------|
| 2.1 | Lithium-polymer (Li-Po) cell | Primary energy storage for the case | Capacity: ≥ 500mAh (recommend 1000–2000mAh for meaningful glasses top-up); Voltage: 3.7V nominal; Form factor: flat pouch cell sized to fit shell; Operating temp: 0–45°C charge, -20–60°C storage | 1 | **UN 38.3 mandatory**; **IEC 62133-2 certification required**; **UL 2054 certification required**; must have integrated PTC (positive temperature coefficient) protection or PCM |
| 2.2 | Protection circuit module (PCM / BMS) | Overcurrent, overvoltage, overdischarge, and short-circuit protection for Li-Po cell | Rated for cell capacity; overcharge cutoff ≤ 4.25V; overdischarge cutoff ≥ 2.5V; overcurrent protection; operating temp range matches cell | 1 | Required by IEC 62133-2 and UL 62368-1; must be present for regulatory compliance |
| 2.3 | Battery connector / cable | Electrical connection from battery/PCM to main PCB | JST PH 2.0 or equivalent 2-pin connector; wire gauge appropriate for rated current (≥ 24 AWG); red/black polarity convention | 1 | Polarity marking required; must be keyed to prevent reverse insertion |
| 2.4 | Battery adhesive pad | Double-sided foam tape securing cell in battery pocket | 3M 9080 or equivalent; prevents cell movement during drop events | 1 | — |

---

## 3. Main PCB & Electronics

| # | Component | Description | Key Specs | Qty/Unit | Regulatory / Notes |
|---|-----------|-------------|-----------|----------|--------------------|
| 3.1 | Main PCB | Single-sided or double-sided PCB carrying all active electronics | FR4, 1.6mm thickness [INFERRED]; sized to fit lower shell; includes USB-C input, charge controller, cell management, LED driver, pogo pin outputs, ring dock output | 1 | Lead-free solder required (RoHS); PCB fabricator must provide RoHS declaration |
| 3.2 | Power bank / charge management IC | Integrated IC managing: USB-C input charging, Li-Po cell charge/discharge, output regulation to pogo pins and ring dock | Example class: IP5306, IP5328P, or equivalent power bank SoC; features: 5V boost output, 1A+ input, LED fuel gauge output, pass-through charging support; USB-C 5V/2A input min | 1 | Must support protection features required by IEC 62368-1; datasheet required for compliance documentation |
| 3.3 | USB-C receptacle (input) | Female USB-C port for wall adapter input | USB-C 2.0 receptacle (power only, no data required unless desired); rated ≥ 5A; SMD or through-hole; USB-IF compliant connector from certified vendor | 1 | USB-IF connector compliance documentation required; rated for ≥ 10,000 mating cycles |
| 3.4 | Input filtering capacitors | EMC input filtering on USB-C input | 100nF + 10µF ceramic / electrolytic combination at USB-C input; X2Y or similar for common-mode filtering | 2–4 | Reduces conducted emissions for FCC Part 15B compliance |
| 3.5 | Output filtering / decoupling capacitors | Filtering on pogo pin and ring dock outputs | 100nF ceramic decoupling per output rail | 4–6 | — |
| 3.6 | ESD protection diodes | Transient protection on USB-C input and output contacts | TVS or Schottky array; USB-C IEC 61000-4-2 level 4 rated | 1–2 arrays | Required for IEC 62368-1 and FCC/CE EMC compliance |
| 3.7 | Ferrite bead / common-mode choke | EMI suppression on USB-C input | Rated for input current; impedance ≥ 600Ω at 100MHz | 1 | Supports FCC Part 15B conducted emissions compliance |
| 3.8 | LED indicator(s) | Visual status indication | Quantity: 1–3 LEDs (single multi-color LED or discrete red/green/blue); Color: TBD per UX spec (recommend: red = charging / green = full / amber = low battery); 0603 or 0402 SMD | 1–3 | Must be visible through LED window in shell |
| 3.9 | LED current-limiting resistors | Sets LED drive current | Value calculated per LED forward voltage and desired brightness; 0402 SMD | 1 per LED | — |
| 3.10 | LED light pipe / window | Transmits LED light through shell to exterior | Clear or frosted acrylic or polycarbonate light pipe; press-fit or bonded into shell LED cutout; diffuses LED for even appearance | 1 | Material must be RoHS compliant |
| 3.11 | Passive components (resistors, capacitors, inductors) | Supporting passives for charge controller reference circuit, voltage dividers, filters | Per IC datasheet requirements; 0402 SMD; lead-free | ~10–20 | RoHS compliance via PCB assembly house declaration |
| 3.12 | PCB standoffs / mounting posts | Secures PCB to lower shell | Brass or nylon M2 standoffs; height to match PCB-to-shell clearance | 4 | — |

---

## 4. Glasses Charging Interface

| # | Component | Description | Key Specs | Qty/Unit | Regulatory / Notes |
|---|-----------|-------------|-----------|----------|--------------------|
| 4.1 | Pogo pin contacts — glasses charging | Spring-loaded contacts that mate with Mira Glasses charging pads on temple arm | Quantity: 2 pins minimum (+ and GND) or as required by glasses charging spec; Gold-plated (Au ≥ 0.3µm over Ni); spring force: 50–150g; stroke: ≥ 0.5mm; rated current ≥ 1A per pin; cycle life ≥ 10,000 | 2–4 | Contact spacing and accessibility must comply with IEC 62368-1 touch current requirements; exposed contacts are a safety-critical item |
| 4.2 | Pogo pin carrier / housing | Mounts pogo pins in precise position aligned to glasses charging contacts | Injection-molded LCP or PA66; positions pins within ±0.15mm of drawing; press-fit or screw-mounted to lower shell | 1 | Dimensional accuracy critical for charging reliability |
| 4.3 | Pogo pin wiring harness | Connects pogo pins to PCB output | 26 AWG silicone or PVC wire; length as required; crimped terminals or soldered to PCB and pin tails | 1 set | Current rating must match charging output |
| 4.4 | Magnetic alignment feature (optional) | Small N35–N52 neodymium magnet(s) embedded in cradle to guide glasses into charging position | Diameter 3–6mm disc magnet; positioned to attract glasses frame to correct seated position without interfering with glasses magnetics | 0–2 | Must not interfere with Mira Glasses BLE antenna or internal magnets; field strength and placement to be validated |

*Note: If magnetic wire charger approach is chosen over pogo pins, substitute items 4.1–4.4 with a custom magnetic cable dock permanently routed inside the case. Pogo pin approach preferred for cleaner user experience and no cable management issues.*

---

## 5. Ring Charging Interface

| # | Component | Description | Key Specs | Qty/Unit | Regulatory / Notes |
|---|-----------|-------------|-----------|----------|--------------------|
| 5.1 | Ring charging dock — magnetic contact assembly | Recessed dock within the case interior that the Mira Ring sits in for charging | Magnetic contact pair (or small Qi coil); sized to accept ring sizes 7–14; output voltage matches ring charging spec; magnet strong enough to retain ring in dock but easy to remove | 1 | Output voltage/current must be validated against Mira Ring charging spec; magnet must not erase ring MCU or corrupt BLE pairing data |
| 5.2 | Ring dock housing | Molded recess in lower shell or separate insert that positions ring over charging contacts | Injection-molded ABS or TPE; ring rests concentrically on dock; sized for size 7–14 inner diameter range (17.3–23.0mm) | 1 | Interior lined or smooth-finished to prevent ring scratching |
| 5.3 | Ring dock wiring | Connects ring dock contacts/coil to PCB output | 26 AWG wire; length as required | 1 set | — |

---

## 6. Packaging Components

| # | Component | Description | Key Specs | Qty/Unit | Regulatory / Notes |
|---|-----------|-------------|-----------|----------|--------------------|
| 6.1 | Retail box | Outer retail packaging | Rigid or folding paperboard; sized to fit MiraCase + accessories; 100% recyclable per Mira brand commitment | 1 | Must carry CE, FCC SDoC, WEEE, recycling symbols, and lithium battery caution label; EU Packaging Directive compliance |
| 6.2 | Inner tray / insert | Holds case securely in retail box | Molded pulp or PETG thermoform; no loose movement | 1 | — |
| 6.3 | Product labels | FCC, CE, WEEE, battery Wh label, serial number label | Per label specifications from compliance team; tamper-evident S/N label for traceability | 1 set | **FCC SDoC or FCC ID label mandatory for US market**; **CE + WEEE mandatory for EU market**; **battery capacity in Wh mandatory per EU Battery Reg 2023/1542** |
| 6.4 | Outer shipping carton label | Lithium battery hazard label for shipping carton | IATA/DOT "LITHIUM ION BATTERY" caution label; Class 9 hazmat label if required by shipment size | 1 per carton | **Mandatory for all air and sea freight per IATA DGR and IMDG Code** |
| 6.5 | Quick start / user guide | Printed user instructions | Language requirements per market (EN for US; EN+DE+FR+ES+IT minimum for EU); includes recycling and battery safety guidance | 1 | WEEE and battery safe disposal instructions legally required for EU |
| 6.6 | Microfiber cleaning cloth | Included accessory for lens cleaning | Microfiber, ~15×15cm; branded or unbranded | 1 | — |

---

## 7. Component Count Summary

| Category | Unique Components | Notes |
|----------|------------------|-------|
| Enclosure & Mechanical | 12 | Shell, lining, hinge, latch, cradle, bumpers, fasteners |
| Battery System | 4 | Cell, PCM, connector, adhesive |
| Main PCB & Electronics | 12 | PCB, ICs, passives, LED, USB-C port |
| Glasses Charging Interface | 4 | Pogo pins, carrier, wiring, alignment magnet |
| Ring Charging Interface | 3 | Dock assembly, housing, wiring |
| Packaging | 6 | Box, insert, labels, guide, cloth |
| **Total unique components** | **~41** | Excludes individual passive component variants |

---

## 8. Components Requiring Third-Party Certification

| Component | Required Certification | Who Provides It |
|-----------|----------------------|-----------------|
| Li-Po cell | UN 38.3, IEC 62133-2, UL 2054 | Cell supplier |
| PCM / BMS | Referenced in IEC 62368-1 test | PCM supplier (datasheet + test report) |
| Finished MiraCase (electrical) | IEC/UL 62368-1, FCC Part 15B, CE (LVD + EMC) | Accredited test lab (e.g., SGS, Intertek, TÜV) |
| USB-C receptacle | USB-IF connector compliance | Connector supplier |
| All PCB materials | RoHS 3, REACH SVHC | PCB fab + component suppliers |
| All plastic / leather / adhesive materials | RoHS 3, REACH SVHC | Material suppliers |
