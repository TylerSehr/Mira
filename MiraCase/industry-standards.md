# MiraCase — Industry Standards & Regulatory Requirements
*Based on device-summary.md — April 2026*

---

## Overview

The MiraCase is an active consumer electronics charging accessory containing a lithium-polymer battery, USB-C power input, and charging output contacts (pogo pin or magnetic). This combination triggers regulatory obligations across battery safety, electrical safety, RF/EMC, chemical compliance, and transport. Primary market is the United States (Mira is SF-based, shipping domestically); EU and UK obligations are included as likely secondary markets.

---

## 1. Battery Safety

The internal Li-Po battery (≥500mAh) is the highest-risk regulatory component and drives the most critical certifications.

| Standard | Body | Scope | Required? |
|----------|------|-------|-----------|
| **UN 38.3** | United Nations | Transport testing for lithium cells/batteries — altitude, thermal, vibration, shock, external short, impact, overcharge, forced discharge. Required for all lithium batteries shipped by air or sea. | **Yes — mandatory for air freight** |
| **IEC 62133-2** | IEC | Safety for portable sealed secondary lithium cells and batteries in consumer applications | **Yes — required for CE / market access** |
| **UL 2054** | UL | Household and commercial batteries — US market standard for lithium battery safety | **Yes — required for US market** |
| **IEC 62368-1** | IEC | Audio/video/IT and communications technology equipment safety — covers the charging system as a whole | **Yes** |
| **UL 62368-1** | UL | US/Canada equivalent of IEC 62368-1 | **Yes — required for US/CA market** |

---

## 2. Electrical & Charging Safety

The MiraCase functions as a charger/power bank and must comply with electrical safety standards for that product class.

| Standard | Body | Scope | Required? |
|----------|------|-------|-----------|
| **IEC 62368-1 (3rd ed.)** | IEC | Supersedes IEC 60950-1 and IEC 60065; covers safety for consumer electronics chargers and power accessories | **Yes** |
| **UL 62368-1** | UL | US/Canada version — required for UL listing or ETL certification | **Yes** |
| **IEC 60664-1** | IEC | Insulation coordination for equipment — governs creepage/clearance distances on PCB | Yes (engineering reference) |
| **IEC 60529 (IP Code)** | IEC | Ingress protection — if any IP rating is claimed on the case itself | If claimed |
| **USB Power Delivery Specification** | USB-IF | Governs USB-C port behavior, voltage negotiation, and cable requirements | **Yes — for USB-C compliance** |
| **IEC 62680-1-3** | IEC | USB interfaces for data and power — USB-C connector and cable standard | **Yes** |

### Pogo Pin / Contact Charging Specific
- Contact spacing and insulation must comply with **IEC 62368-1** touch-current and accessibility requirements
- Exposed contacts must be designed to prevent unintended short circuits (e.g., via recessed design or spring-loaded pins that retract when not engaged)
- Output voltage/current limits must be within safe touch-voltage thresholds per IEC 62368-1 Annex criteria

---

## 3. Electromagnetic Compatibility (EMC)

Switching regulators inside the charging circuit are unintentional RF radiators and must be tested for emissions and immunity.

| Standard | Body | Scope | Required? |
|----------|------|-------|-----------|
| **FCC Part 15 Subpart B** | FCC (US) | Unintentional radiators — emissions limits for consumer electronics with switching power supplies | **Yes — required for US market** |
| **ICES-003** | ISED (Canada) | Canadian equivalent of FCC Part 15B | **Yes — required for CA market** |
| **EN 55032 / CISPR 32** | CENELEC / IEC | Emissions standard for multimedia equipment (EU) | **Yes — required for CE marking** |
| **EN 55035 / CISPR 35** | CENELEC / IEC | Immunity standard for multimedia equipment (EU) | **Yes — required for CE marking** |
| **EN IEC 61000-3-2** | IEC | Harmonic current emissions (EU) | **Yes — required for CE marking** |
| **EN IEC 61000-3-3** | IEC | Voltage fluctuations and flicker (EU) | **Yes — required for CE marking** |

---

## 4. CE Marking (European Union)

CE marking is required if the product is sold in EU/EEA markets. The MiraCase will need to comply with the following directives and demonstrate conformity via a Declaration of Conformity (DoC).

| Directive / Regulation | Scope |
|------------------------|-------|
| **Low Voltage Directive (LVD) 2014/35/EU** | Electrical safety for devices operating at 50–1000V AC or 75–1500V DC; applies to the charging circuit |
| **EMC Directive 2014/30/EU** | Electromagnetic compatibility — emissions and immunity |
| **EU Battery Regulation 2023/1542** | Replaces Battery Directive; requires battery labeling, capacity declaration, carbon footprint declaration (phased), and recyclability requirements — applies to Li-Po cells |
| **RoHS Directive 2011/65/EU + Amendment 2015/863 (RoHS 3)** | Restriction of hazardous substances in electronic equipment — limits Pb, Hg, Cd, Cr(VI), PBB, PBDE, DEHP, BBP, DBP, DIBP |
| **WEEE Directive 2012/19/EU** | Waste Electrical and Electronic Equipment — producer registration, take-back obligations, WEEE marking required |
| **REACH Regulation (EC) No 1907/2006** | Chemicals — if any SVHC (Substances of Very High Concern) are present above 0.1% w/w, disclosure and potentially authorization required |
| **Packaging Directive 94/62/EC + revisions** | Packaging must be recyclable; heavy metal limits apply |
| **Ecodesign Regulation (EU) 2019/1782** | External power supplies — if the USB-C adapter counts as a standalone EPS, efficiency requirements apply |

---

## 5. UKCA Marking (United Kingdom)

Post-Brexit, the UK requires UKCA marking for products placed on the GB market (England, Wales, Scotland). Equivalent to CE but registered with UK authorities.

| Regulation | UK Equivalent of |
|-----------|-----------------|
| UK Electrical Equipment (Safety) Regulations 2016 | LVD |
| UK Electromagnetic Compatibility Regulations 2016 | EMC Directive |
| UK Batteries and Accumulators Regulations 2008 (+ amendments) | Battery Directive |
| UK RoHS Regulations 2012 (+ amendments) | RoHS |

---

## 6. US Market — Additional Requirements

| Standard / Regulation | Body | Scope |
|----------------------|------|-------|
| **FCC Part 15B** | FCC | Emissions — required before sale in US (FCC ID or SDoC) |
| **California Proposition 65** | CA OEHHA | Warning labels required if product contains listed chemicals above safe harbor levels (common for electronics with solder, cables, plastics) |
| **CPSC 16 CFR** | CPSC | Consumer Product Safety — general duty clause; battery-powered consumer accessories subject to CPSC oversight; no specific mandatory standard but must not present unreasonable hazard |
| **UL 2054** | UL | Battery safety — UL listing is a strong de-facto requirement for US retail channels |
| **USB-IF Certification** | USB-IF | USB-C connector and cable compliance; required by some retailers (e.g., Amazon) and recommended for all USB-C products |

---

## 7. Transport & Shipping Regulations

Li-Po batteries trigger dangerous goods (DG) classification for shipping.

| Regulation | Body | Scope | Required? |
|-----------|------|-------|-----------|
| **UN 38.3** | UN | Lithium battery transport testing — must pass before any shipping by air or sea | **Yes — mandatory** |
| **IATA Dangerous Goods Regulations (DGR)** | IATA | Air freight rules for lithium batteries — Section II (small batteries in equipment/packaging); governs packaging, labeling, quantity limits per package | **Yes — for air freight** |
| **DOT 49 CFR Parts 171–180** | US DOT | US domestic ground and air transport of hazardous materials including lithium batteries | **Yes — for US domestic shipping** |
| **IMDG Code** | IMO | Sea freight — lithium battery shipping rules for ocean freight (Shenzhen → US) | **Yes — for ocean freight from China** |

**Key thresholds for MiraCase battery (≥500mAh, ~1.85Wh at 3.7V):**
- A 500mAh / 3.7V cell = ~1.85Wh — well below the 20Wh per-cell / 100Wh per-battery threshold for Section II classification
- Ships as **UN3481** (lithium ion batteries packed with or contained in equipment) or **UN3091** (lithium metal equivalent) if applicable
- Must include UN38.3 test summary and comply with IATA Packing Instruction PI967 or PI970

---

## 8. Chemical & Material Compliance

| Standard | Scope |
|----------|-------|
| **RoHS 3 (EU 2015/863)** | 10 restricted substances in electronics — applies to PCB, solder, cables, plastics |
| **China RoHS (GB/T 26572)** | Chinese equivalent — mandatory for products sold in China; requires SJ/T 11364 hazardous substance marking |
| **REACH SVHC** | EU — disclosure if any SVHC in article above 0.1% w/w |
| **California Prop 65** | US — warning if listed substances present (common in PVC cables, solder, leather dyes) |
| **Conflict Minerals (Dodd-Frank Section 1409 / SEC Rule)** | If Mira is or becomes a public company, supply chain due diligence on tin, tantalum, tungsten, gold (3TG) required; good practice for responsible sourcing regardless |

---

## 9. Labeling Requirements

| Requirement | Jurisdiction | Notes |
|-------------|-------------|-------|
| FCC SDoC or FCC ID label | US | "Contains FCC ID: XXXX" or Supplier Declaration of Conformity statement |
| CE mark | EU | Required on product and packaging |
| UKCA mark | UK | Required for GB market |
| WEEE symbol (crossed-out wheelie bin) | EU / UK | Mandatory on product or packaging for EEE |
| Battery capacity label | EU (Battery Reg 2023/1542) | Rated capacity in Wh must be marked on battery or product |
| Lithium battery caution label | IATA / DOT | Required on shipping carton: "LITHIUM ION BATTERY" caution label |
| Prop 65 warning | California | If applicable chemicals present |
| China RoHS hazardous substance table | China | SJ/T 11364 marking if sold in China |
| USB-C symbol | USB-IF | Recommended; required if USB-IF certified |

---

## 10. Standards Summary — Priority Matrix

| Standard | Priority | Timing |
|----------|----------|--------|
| UN 38.3 (battery transport) | Critical | Before first shipment from China |
| UL 2054 (battery safety) | Critical | Before US retail/DTC launch |
| UL 62368-1 / IEC 62368-1 (electrical safety) | Critical | Before launch |
| FCC Part 15B (US EMC) | Critical | Before US sale |
| IEC 62133-2 (battery safety, international) | High | Before EU launch |
| CE marking (LVD + EMC + Battery Reg + RoHS) | High | Before EU sale |
| RoHS 3 compliance | High | Design phase — supplier declarations |
| REACH SVHC | High | Design phase — supplier declarations |
| USB-IF compliance | Medium | Before launch — required by some retail channels |
| IATA DGR (air freight) | High | Before first air shipment |
| California Prop 65 | Medium | Before California sale — assess chemical content |
| UKCA | Medium | Before UK sale |
| China RoHS | Low (if no CN sales) | If sold in China |
| WEEE registration | Medium | Before EU sale — register as producer |
