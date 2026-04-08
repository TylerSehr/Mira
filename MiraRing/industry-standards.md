# Mira Ring — Industry Standards & Regulatory Requirements
**Prepared for:** Supplier Sourcing & Manufacturing
**Date:** April 2026
**Based on:** device-summary.md

---

## Overview

The Mira Ring is a Bluetooth Low Energy smart ring containing a LiPo battery, capacitive touch sensor, and magnetic charging system. It is worn directly against skin on the index finger. It is manufactured in China and sold primarily in the United States. These characteristics trigger requirements across six regulatory domains: radio/wireless, electrical safety, battery safety and transport, chemical/material compliance, biocompatibility, and environmental/waste. Compliance is required before the product can legally be sold or imported.

Primary market: **United States**
Secondary markets to plan for: **Canada, European Union, United Kingdom**
Manufacturing origin: **China**

---

## 1. Radio & Wireless Certification

BLE 5.2 transmission is the primary regulatory trigger. Any product intentionally radiating RF must be certified before sale or import in every target market. This is a hard legal requirement — uncertified products cannot be legally imported or sold.

### 1.1 United States — FCC
| Requirement | Detail |
|-------------|--------|
| Regulation | FCC Part 15, Subpart C (intentional radiators) |
| Standard | 47 CFR Part 15.247 (BLE operates in 2.4 GHz ISM band) |
| Process | FCC certification via accredited TCB (Telecommunications Certification Body) |
| Output | FCC ID assigned; must be marked on device or packaging |
| Marking | "FCC ID: XXXXXXX" required on product or in electronic labeling |
| SAR | FCC OET Bulletin 65 — RF exposure evaluation required for body-worn device; BLE at low power typically passes with standard separation distance declaration, but worn-on-finger placement requires documented evaluation |
| Grant | Available on FCC's equipment authorization database (fccid.io) |

**Note:** If Mira uses a pre-certified BLE module (e.g., Nordic nRF52840 with FCC modular approval), they can leverage the module's existing FCC ID and file a Class II Permissive Change or Class B SDoC for the end product rather than full certification. This is the most common and cost-effective path for ring-form-factor BLE devices.

### 1.2 Canada — ISED (formerly Industry Canada)
| Requirement | Detail |
|-------------|--------|
| Regulation | RSS-247 Issue 2 (2.4 GHz spread spectrum devices) |
| Standard | ISED RSS-Gen (general requirements) |
| Process | Certification via recognized Canadian certification body |
| Output | IC ID assigned (format: XXXX-MODELNAME) |
| Marking | "IC: XXXX-MODELNAME" required |
| RF Exposure | RSS-102 — RF exposure evaluation for body-worn devices |

Canada is typically tested and certified simultaneously with FCC using shared test data; marginal additional cost.

### 1.3 European Union — Radio Equipment Directive (RED)
| Requirement | Detail |
|-------------|--------|
| Directive | 2014/53/EU — Radio Equipment Directive (RED) |
| Radio standard | ETSI EN 300 328 V2.2.2 (BLE in 2.4 GHz wideband) |
| EMC standard | ETSI EN 301 489-1 + EN 301 489-17 (radio EMC) |
| Safety standard | EN IEC 62368-1:2020 (audio/video and IT equipment safety) |
| RF exposure | EN 50566 + EN 62209-2 (RF exposure for body-worn wireless devices) |
| Process | Self-declaration via Notified Body or internal Technical File; CE mark affixed |
| Output | CE marking + EU Declaration of Conformity (DoC) |
| Marking | CE mark on product and/or packaging; WEEE symbol required |
| EU Rep | An EU-authorized representative is required for non-EU manufacturers |

### 1.4 United Kingdom — UKCA
| Requirement | Detail |
|-------------|--------|
| Regulation | UK Radio Equipment Regulations 2017 (post-Brexit equivalent of RED) |
| Standards | Same ETSI standards as EU RED apply (UK continues to recognize ETSI) |
| Marking | UKCA mark (replaces CE for UK Great Britain market post-2024) |
| Process | UK Declaration of Conformity; UK Responsible Person required |

### 1.5 Bluetooth SIG Qualification
| Requirement | Detail |
|-------------|--------|
| Requirement | Any product using Bluetooth branding or the Bluetooth logo must be Bluetooth SIG qualified |
| Process | End Product Listing (EPL) via Bluetooth SIG member account |
| Path | If using a pre-qualified BLE module/stack, end product qualification is significantly simplified (declare use of qualified subsystem) |
| Cost | Bluetooth SIG membership + listing fee |

---

## 2. Electrical Safety

### 2.1 United States — UL / NRTL
| Requirement | Detail |
|-------------|--------|
| Standard | UL 62368-1 (Audio/Video, Information and Communication Technology Equipment) |
| Alternative | IEC 62368-1 tested to UL national differences |
| Process | Testing by a Nationally Recognized Testing Laboratory (NRTL) such as UL, CSA, TÜV |
| Output | NRTL mark on product (UL Listed, ETL Listed, etc.) |
| Mandatory? | Not federally mandated for consumer electronics, but required by most US retailers and essential for FCC certification ecosystem; practically required for market access |

### 2.2 Canada — CSA / cUL
| Requirement | Detail |
|-------------|--------|
| Standard | CSA C22.2 No. 62368-1 (harmonized with IEC 62368-1) |
| Process | Combined testing with UL via cUL or cETL mark covers both US and Canada |
| Output | cUL or cETL mark |

### 2.3 European Union — LVD (Low Voltage Directive)
| Requirement | Detail |
|-------------|--------|
| Directive | 2014/35/EU — Low Voltage Directive (LVD) |
| Standard | EN IEC 62368-1:2020 |
| Note | For battery-powered wearables operating below 50V AC / 75V DC, LVD may not apply; in that case, general product safety under GPSD (2001/95/EC) / successor GPSR (2023/988/EU, applicable from Dec 2024) governs |
| Process | Self-declaration; CE marking covers this alongside RED |

---

## 3. Battery Safety & Transport

The LiPo (lithium-polymer) cell in the ring triggers mandatory requirements for both product safety and transport. These apply regardless of target market.

### 3.1 Transport — UN 38.3 (Global, Mandatory)
| Requirement | Detail |
|-------------|--------|
| Standard | UN Manual of Tests and Criteria, Part III, Section 38.3 |
| Scope | All lithium batteries shipped by air, sea, or ground internationally |
| Tests | Altitude simulation, thermal cycling, vibration, shock, external short circuit, impact/crush, overcharge, forced discharge |
| Who certifies | Accredited third-party lab (SGS, Intertek, Bureau Veritas, etc.) |
| Mandatory? | YES — required by IATA (air), IMDG (sea), and ADR (EU road) for any shipment |
| Output | UN 38.3 test report; must accompany shipment documentation |

**Critical:** No lithium battery cells or products can be legally shipped internationally without a valid UN 38.3 test report. This must be obtained before any sample or production shipment.

### 3.2 Cell Safety — IEC 62133-2
| Requirement | Detail |
|-------------|--------|
| Standard | IEC 62133-2:2017 (Safety requirements for portable sealed secondary lithium cells/batteries) |
| Scope | The LiPo cell itself (not the end product) |
| Process | Cell supplier should have existing IEC 62133-2 certification; request cert from supplier |
| Relevance | Required for CE (EU), and referenced by UL 62368-1 safety testing |

### 3.3 United States — UL 1642 / UL 2054
| Standard | Scope |
|----------|-------|
| UL 1642 | Standard for Lithium Batteries (cells) |
| UL 2054 | Standard for Household and Commercial Batteries (battery packs) |
| Note | Cell supplier should hold UL 1642; the ring's battery pack assembly should comply with UL 2054 |

### 3.4 California Proposition 65
| Requirement | Detail |
|-------------|--------|
| Regulation | California Safe Drinking Water and Toxic Enforcement Act (Prop 65) |
| Scope | Any product sold in California must carry a warning if it contains chemicals on the Prop 65 list above safe harbor levels |
| Relevance to ring | Lithium batteries, electronic components, and certain plastics/coatings may contain listed chemicals (lead, cobalt compounds, DEHP) |
| Requirement | Either conduct exposure assessment to demonstrate no warning needed, or apply Prop 65 warning to product/packaging |

### 3.5 FCC Battery / Charging Safety (US)
| Requirement | Detail |
|-------------|--------|
| Regulation | FCC Part 15 indirectly; CPSC enforcement under Consumer Product Safety Act |
| CPSC | Consumer Product Safety Improvement Act (CPSIA) — CPSC has authority over consumer electronics battery safety |
| Practical requirement | Battery must include overcharge, over-discharge, and short-circuit protection circuit (PCM/BMS) — this is required to pass UL 62368-1 and is standard practice |

---

## 4. Electromagnetic Compatibility (EMC)

### 4.1 United States — FCC Part 15B
| Requirement | Detail |
|-------------|--------|
| Regulation | FCC 47 CFR Part 15, Subpart B (unintentional radiators) |
| Scope | Limits on unintentional RF emissions from digital devices |
| Classification | Class B (consumer/residential environment) |
| Process | Covered under the FCC Part 15C certification process for the BLE radio; unintentional emissions evaluated as part of same test campaign |

### 4.2 European Union — EN 301 489 + EN 55032
| Standard | Scope |
|----------|-------|
| EN 301 489-1 + EN 301 489-17 | EMC for radio equipment (BLE) — required under RED |
| EN 55032 | EMC for multimedia equipment (emissions) |
| EN 55035 | EMC for multimedia equipment (immunity) |

---

## 5. Chemical & Material Compliance

This is a critical category for the Mira Ring due to its direct, prolonged skin contact and its metallic inner band. These requirements are often overlooked during early hardware development.

### 5.1 EU RoHS — Restriction of Hazardous Substances
| Requirement | Detail |
|-------------|--------|
| Directive | EU 2011/65/EU (RoHS 2) + amendment 2015/863/EU (RoHS 3, adding phthalates) |
| UK equivalent | UK RoHS (SI 2012/3032) |
| Restricted substances | Lead (Pb), Mercury (Hg), Cadmium (Cd), Hexavalent Chromium (Cr6+), PBB, PBDE, DEHP, BBP, DBP, DIBP |
| Scope | All electronic and electrical equipment sold in EU |
| Limits | Lead ≤ 1000 ppm; Cadmium ≤ 100 ppm; others ≤ 1000 ppm |
| Process | Material declarations from component suppliers; third-party XRF screening of parts; DoC |
| Output | RoHS Declaration of Conformity; incorporated into CE technical file |
| Mandatory? | YES for EU/UK market |

**Practical action:** Require full material declarations (IPC-1752A or equivalent) from all component and material suppliers. Spot-check with XRF testing during production.

### 5.2 EU REACH — Registration, Evaluation, Authorisation and Restriction of Chemicals
| Requirement | Detail |
|-------------|--------|
| Regulation | EC No 1907/2006 (REACH) |
| Key obligation | Substances of Very High Concern (SVHC) — if any SVHC is present in the article above 0.1% by weight, the supplier must notify customers and (if >1 tonne/year) notify ECHA |
| SVHC list | Updated biannually; currently 240+ substances |
| Relevant SVHC for rings | Nickel compounds, certain phthalates, cobalt compounds (in battery), certain flame retardants in PCB/plastics |
| Process | Full materials disclosure from supply chain; SVHC screening |

### 5.3 EU Nickel Directive — REACH Annex XVII, Entry 27 (CRITICAL for rings)
| Requirement | Detail |
|-------------|--------|
| Regulation | REACH Annex XVII, Entry 27 (formerly Nickel Directive 94/27/EC) |
| Scope | Articles inserted into pierced ears/skin OR articles in prolonged skin contact (including rings, bracelets, watches) |
| Limit | Nickel release rate must not exceed **0.5 µg/cm²/week** for prolonged skin-contact items |
| Test standard | EN 1811:2011+A1:2015 (reference test for nickel release) |
| Relevance | CRITICAL — the Mira Ring's metallic inner band (stainless steel or aluminum) and any plated surfaces must be tested and comply with this limit |
| Consequence of failure | Product banned from EU sale; potential recall |

**Action required:** Specify nickel-free or low-nickel-release materials for all skin-contact surfaces. Request EN 1811 test reports from the ring manufacturer. 316L stainless steel typically complies; lower grades may not.

### 5.4 California Proposition 65 (see Section 3.4 above)
Also relevant for material compliance — certain pigments, flame retardants, and plasticizers in the ring body may trigger Prop 65 requirements.

### 5.5 US CPSC — Consumer Product Safety Improvement Act (CPSIA)
| Requirement | Detail |
|-------------|--------|
| Regulation | CPSIA (15 U.S.C. § 2051 et seq.) |
| Lead content | ≤ 100 ppm lead in substrate; ≤ 90 ppm lead in surface coating |
| Phthalates | ≤ 1000 ppm each for DEHP, DBP, BBP, DINP, DPENP, DHEXP, DCHP in any accessible component (primarily plastics) |
| Relevance | Applies to consumer products; most relevant for plastic components of the ring body |

---

## 6. Biocompatibility & Skin Safety

The Mira Ring is worn continuously against skin on the index finger. This creates obligations beyond standard electronics regulation.

### 6.1 ISO 10993 — Biocompatibility of Medical Devices
| Requirement | Detail |
|-------------|--------|
| Standard | ISO 10993-1 (Evaluation and testing within a risk management process) |
| Applicability | Technically a medical device standard; however, consumer wearables with prolonged skin contact are often evaluated against ISO 10993 framework as a best practice |
| Relevant tests | ISO 10993-10 (irritation and skin sensitization); ISO 10993-5 (cytotoxicity) |
| Practical application | Not legally required for non-medical consumer wearables, but EU GPSR (General Product Safety Regulation) and product liability risk management recommend it |
| Recommendation | Request skin sensitization and cytotoxicity test reports from ring manufacturer for all skin-contact materials |

### 6.2 EU General Product Safety Regulation (GPSR)
| Requirement | Detail |
|-------------|--------|
| Regulation | EU 2023/988 (GPSR, applicable from December 13, 2024 — replaces GPSD) |
| Scope | All consumer products sold in EU; requires products to be safe for their intended use including foreseeable misuse |
| Skin contact | Prolonged skin contact creates heightened scrutiny for irritation, sensitization, and dermal absorption of chemical substances |
| Obligation | Risk assessment documentation; incident reporting system; market surveillance cooperation |

---

## 7. Environmental & Waste Compliance

### 7.1 EU WEEE — Waste Electrical and Electronic Equipment
| Requirement | Detail |
|-------------|--------|
| Directive | 2012/19/EU (WEEE Directive) |
| Scope | All electrical/electronic equipment sold in EU |
| Obligation | Register with national WEEE scheme in each EU country of sale; pay take-back/recycling fees; mark product with crossed-out wheelie bin symbol |
| Marking | Crossed-out wheeled bin symbol required on product/packaging |

### 7.2 EU Battery Regulation
| Requirement | Detail |
|-------------|--------|
| Regulation | EU 2023/1542 (new Battery Regulation, replacing Battery Directive 2006/66/EC) |
| Scope | All batteries placed on EU market |
| Obligations | Battery labeling (capacity, chemistry, recycling symbol); carbon footprint declaration (phased in over time); battery passport (phased in); take-back/recycling requirements |
| LiPo relevance | The ring's LiPo cell triggers registration and labeling requirements |

### 7.3 China RoHS (SJ/T 11364)
| Requirement | Detail |
|-------------|--------|
| Standard | SJ/T 11364-2014 (China RoHS marking standard) |
| Scope | Electronic products manufactured in or sold in China |
| Obligation | "Environmental Friendly Use Period" (EFUP) label on product; disclosure of hazardous substances in product materials |
| Relevance | Required if product is sold in China; also required on product as manufactured in China even for export in some interpretations |

---

## 8. Trade & Import Compliance

### 8.1 HTS Classification (US Import)
| Item | HTS Code (estimated) | Duty Rate |
|------|----------------------|-----------|
| Smart ring (electronic wearable with BLE) | 8517.62.0090 or 8543.70.9960 | Varies |
| Note | The 35% tariff rate observed in Mira's cost data (vs. standard MFN rates) likely reflects Section 301 China tariffs (List 3 or List 4A) on top of base MFN duty |

**Action:** Confirm exact HTS classification with a licensed customs broker. Misclassification risks underpayment (penalty risk) or overpayment. Explore whether any exclusions or alternative classifications reduce Section 301 exposure.

### 8.2 Section 301 China Tariffs
| Detail | Value |
|--------|-------|
| Current tariff observed | 35% (from Mira cost data) |
| Basis | Section 301 tariffs on Chinese-origin goods, layered on MFN duty rate |
| Mitigation options | First Sale valuation; tariff engineering (component-level sourcing outside China); Free Trade Zone (FTZ) processing; bonded warehouse strategies |
| Note | Tariff rates on Chinese electronics remain subject to USTR review and can change; monitor USTR Section 301 docket |

### 8.3 FCC Equipment Import (US CBP)
| Requirement | Detail |
|-------------|--------|
| Regulation | 47 CFR Part 2, Subpart L |
| Obligation | RF devices imported into the US must be FCC authorized prior to importation; CBP enforces at port of entry |
| Risk | Uncertified BLE devices can be seized at customs |

---

## 9. Standards Summary Table

| Standard / Regulation | Body | Region | Category | Mandatory? |
|-----------------------|------|--------|----------|------------|
| FCC Part 15C (BLE radio) | FCC | US | Radio | YES |
| FCC Part 15B (EMC emissions) | FCC | US | EMC | YES |
| FCC OET Bulletin 65 (SAR/RF exposure) | FCC | US | RF Safety | YES |
| RSS-247 + RSS-102 | ISED | Canada | Radio + RF Safety | YES |
| ETSI EN 300 328 (BLE radio) | ETSI / EC | EU | Radio (RED) | YES |
| EN 301 489-1 / -17 (radio EMC) | ETSI / EC | EU | EMC (RED) | YES |
| EN IEC 62368-1 (electrical safety) | IEC / EC | EU | Safety (RED/LVD) | YES |
| EN 50566 / EN 62209-2 (RF exposure) | CENELEC | EU | RF Safety (RED) | YES |
| UKCA / UK Radio Equipment Regs | UKAS | UK | Radio | YES |
| Bluetooth SIG Qualification | Bluetooth SIG | Global | Wireless | YES (for branding) |
| UN 38.3 (LiPo transport) | UN / IATA | Global | Battery Transport | YES |
| IEC 62133-2 (cell safety) | IEC | Global | Battery Safety | YES (via UL/CE) |
| UL 62368-1 (product safety) | UL / NRTL | US/CA | Electrical Safety | Effectively YES |
| UL 1642 / UL 2054 (battery) | UL | US | Battery Safety | Effectively YES |
| EU RoHS (2011/65/EU + 2015/863/EU) | EC | EU/UK | Chemical | YES |
| EU REACH Annex XVII Entry 27 (Nickel) | ECHA | EU | Skin Safety | YES |
| EU REACH SVHC | ECHA | EU | Chemical | YES |
| CPSIA (lead, phthalates) | CPSC | US | Chemical | YES |
| California Proposition 65 | CA OEHHA | US (CA) | Chemical | YES (if sold in CA) |
| EU WEEE (2012/19/EU) | EC | EU | Waste/Recycling | YES |
| EU Battery Regulation (2023/1542) | EC | EU | Battery/Waste | YES |
| China RoHS SJ/T 11364 | MIIT | China | Chemical Labeling | YES (manufactured in CN) |
| ISO 10993 (biocompatibility) | ISO | Global | Skin Safety | Recommended |
| EU GPSR (2023/988) | EC | EU | General Safety | YES |
| EN 1811 (nickel release test) | CEN | EU | Skin Safety | YES (test method for Entry 27) |
| IEC 60529 / ISO 22810 (water resistance) | IEC / ISO | Global | Durability | Recommended (supports 5ATM claim) |

---

## 10. Certification Sequence & Dependencies

The following order is recommended for efficient certification:

1. **Select BLE module with modular FCC/IC/CE approval** → reduces radio certification cost significantly
2. **UN 38.3** on the LiPo cell (required before any samples ship internationally) → get from cell supplier or test early prototype cells
3. **IEC 62133-2** on cell → request from cell supplier
4. **UL 62368-1 + FCC Part 15B/C** → combined US/Canada test campaign (can run in parallel with EU)
5. **EN 300 328 + EN 301 489 + EN 62368-1** → EU test campaign (can share RF data with FCC campaign if lab is accredited for both)
6. **RoHS + REACH material declarations** → collect from all component suppliers throughout development; don't leave for last
7. **EN 1811 nickel release test** → test skin-contact surfaces of ring body early — material change after tooling is expensive
8. **Bluetooth SIG EPL** → file after BLE testing is complete
9. **WEEE + Battery Regulation registration** → before first EU shipment

---

## 11. Key Risks Specific to the Mira Ring

| Risk | Detail | Mitigation |
|------|--------|------------|
| Nickel in metallic inner band | If the inner stainless steel band releases nickel above 0.5 µg/cm²/week, product cannot be sold in EU | Specify 316L SS or titanium; require EN 1811 test report from supplier early |
| Skin irritation from adhesives/coatings | Inner bore coatings or adhesives bonding components could cause allergic reactions | Test all skin-contact materials per ISO 10993-10 |
| LiPo swelling / thermal event in ring form | Small enclosed ring provides no expansion space for cell; swelling cell could crack the ring shell or injure the wearer | Require cell-level IEC 62133-2 certification; specify cell with safety vent; include BMS with overcharge protection |
| 5ATM water resistance claim without IEC 60529 testing | Making water resistance claims without certified test data is an FTC risk (US) and GPSR risk (EU) | Require ISO 22810 or IEC 60529 testing at factory |
| Section 301 tariff volatility | 35% tariff on Chinese-origin smart electronics is subject to USTR review | Track USTR docket; explore alternative sourcing |
| FCC certification delay | FCC test queues can be 8–12 weeks; uncertified product cannot legally be imported | Start FCC process early; use pre-certified module to reduce scope |
