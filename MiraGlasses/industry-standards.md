# Mira Glasses — Industry Standards & Regulatory Requirements
*Based on device-summary.md — April 2026*

---

## Overview

Mira Glasses is a Bluetooth wearable device with embedded Li-Po battery, dual MEMS microphones, open-ear speakers, a dual waveguide optical display, and motion/light sensors. It captures and transmits audio and pairs with an iOS app that processes and stores transcripts. The product ships with prescription lens options. This combination touches multiple regulatory domains: wireless/RF, electrical safety, optical/photobiological safety, audio safety, battery safety, privacy law, and prescription optics regulation.

---

## 1. Wireless & RF Certification

### FCC (United States)
- **FCC Part 15 Subpart C** — Intentional radiators; required for all BLE-transmitting devices sold in the US
- **FCC Part 15.247** — Specific rules for 2.4GHz spread-spectrum devices (BLE operates at 2.4GHz)
- Device must display FCC ID on product or in packaging
- OTA firmware updates must not alter the radio parameters in ways that void authorization

### ISED (Canada)
- **RSS-247** — Digital transmission systems in the 2.4GHz band (equivalent to FCC Part 15.247)
- Requires IC (Industry Canada) certification mark

### CE / RED (European Union)
- **Radio Equipment Directive (RED) 2014/53/EU** — Mandatory for all radio-transmitting devices sold in the EU
- Covers: radio performance, EMC, electrical safety, and (for body-worn devices) health/safety
- Requires CE mark; Declaration of Conformity; Technical File
- **ETSI EN 300 328** — Harmonized standard for wideband 2.4GHz devices (BLE compliance path under RED)
- **ETSI EN 301 489-1 / -17** — EMC standard for radio equipment

### Bluetooth SIG
- **Bluetooth Qualification** — All products using Bluetooth must be qualified through the Bluetooth SIG and listed in the Bluetooth Qualified Products Database
- BLE 5.2 qualification required; use of the Bluetooth name/logo requires membership and passing QDID listing

### UKCA (United Kingdom)
- Post-Brexit equivalent of CE marking; required for UK market
- Follows similar framework to RED

---

## 2. Electrical Safety

### IEC 62368-1
- **IEC 62368-1:2018** (and regional adoptions: UL 62368-1, EN 62368-1) — Audio/video, IT, and communications equipment safety standard
- The primary safety standard for consumer electronics of this type
- Covers: electrical hazards, energy hazards, thermal hazards, mechanical hazards, radiation

### IEC 60950-1 (legacy)
- Largely superseded by IEC 62368-1; some markets may still reference it for legacy certifications

### UL (United States)
- **UL 62368-1** — US adoption of IEC 62368-1; required for NRTL listing (UL, ETL, CSA marks) often required by US retailers

### EN 62368-1 (EU)
- Harmonized standard under the Low Voltage Directive / RED for electrical safety

---

## 3. Battery Safety

### Li-Po Cell Safety
- **IEC 62133-2:2017** — Safety requirements for portable sealed secondary lithium cells and batteries in portable applications; required in most markets for rechargeable Li-Po/Li-ion batteries
- **UN 38.3** — UN Manual of Tests and Criteria, Section 38.3: required for all lithium battery shipments (air, sea, ground); tests include altitude simulation, thermal, vibration, shock, short circuit, impact, overcharge, forced discharge
- **IEC 62368-1** also covers battery/energy hazard requirements at the system level

### EU Battery Regulation
- **EU Battery Regulation 2023/1542** — Replaced the Battery Directive; covers sustainability, labeling, and end-of-life requirements for batteries sold in the EU

### DOT / IATA (Shipping)
- Li-Po batteries in devices are subject to IATA Dangerous Goods Regulations (DGR) for air freight; relevant for both product shipment and returns logistics

---

## 4. Electromagnetic Compatibility (EMC)

- **FCC Part 15 Subpart B** — Unintentional radiators; limits on emissions from digital electronics (US)
- **EN 55032** (CISPR 32) — Emissions standard for multimedia equipment (EU)
- **EN 55035** (CISPR 35) — Immunity standard for multimedia equipment (EU)
- **EN 61000-3-2 / -3-3** — Harmonics and flicker limits (EU, relevant to charging adapter)

---

## 5. Optical & Photobiological Safety

### Waveguide Display / Projector
- **IEC 62471 / EN 62471** — Photobiological safety of lamps and lamp systems; applies to any light source directed at the human eye, including display projectors in smart glasses
  - At 2000 nits with a micro-projector coupled into a waveguide, the projector source must be evaluated for blue-light hazard, retinal thermal hazard, and UV hazard
  - Risk group classification (RG0–RG3) must be established
- **IEC TR 62778** — Application of IEC 62471 to light sources in products (guidance document for display/projector integration)
- **ANSI Z80.3** — Prescription and non-prescription ophthalmic lenses (US); relevant to lens substrate, coatings, and optical quality
- **ISO 12312-1** — Eye and face protection for sunglasses (if any tinted lens variant is introduced)

---

## 6. Acoustic / Hearing Safety

- **EN 50332-1 / -2** — Sound pressure levels for audio equipment with earphones/headphones; open-ear speakers near the ear canal must not exceed safe SPL thresholds
- **IEC 60268-7** — Headphone/earphone performance measurement standard (relevant for speaker characterization)
- **WHO / ITU-T H.870** — Safe listening guidelines for consumer audio devices; increasingly adopted by regulators as a design baseline

---

## 7. SAR — Specific Absorption Rate

- **FCC OET Bulletin 65 / KDB 447498** — SAR testing requirements for body-worn wireless devices (US); BLE devices worn on the head/face must demonstrate SAR compliance at specified separation distances
- **EN 50566 / IEC 62209-2** — SAR measurement for handheld and body-mounted devices (EU)
- At BLE power levels (typically ≤10 dBm), SAR is generally well within limits, but testing and documentation are required for certification

---

## 8. IP / Water Resistance Rating

- **IEC 60529** — Degrees of protection provided by enclosures (IP Code)
  - Mira Glasses are rated **IPX2** — protection against dripping water at 15° tilt; must be tested per IEC 60529 methodology to substantiate the claim
  - Test must be performed by an accredited lab; results documented in the Technical File

---

## 9. Prescription Optics Regulation

### United States
- **FDA 21 CFR Part 886** — Ophthalmic devices; prescription lenses are regulated as Class II medical devices
- **FDA 21 CFR Part 801** — Labeling requirements for medical devices, including ophthalmic lenses
- **Rx-only sale rules** — Prescription lenses in the US legally require a valid prescription from a licensed eye care professional; Mira's prescription order flow must comply with this requirement
- **FTC Eyeglass Rule (16 CFR Part 456)** — Requires that patients receive a copy of their prescription; relevant if Mira collects Rx data directly

### European Union
- **EU Regulation 2017/745 (MDR)** — Medical Device Regulation; prescription corrective lenses are Class I medical devices and require CE marking under MDR, with a Declaration of Conformity and registration in EUDAMED
- **EN ISO 21987** — Ophthalmic optics: mounted spectacle lenses (quality and performance standard)
- **EN ISO 8624** — Ophthalmic optics: spectacle frames — measuring system and terminology

---

## 10. Privacy & Audio Recording Law

### United States — Federal
- **Electronic Communications Privacy Act (ECPA) / Wiretap Act (18 U.S.C. § 2511)** — Federal prohibition on unauthorized interception of oral/electronic communications; always-on audio recording must include informed consent mechanisms
- **FTC Act Section 5** — Prohibits unfair or deceptive trade practices; privacy claims (e.g., "audio deleted immediately") must be accurate and verifiable

### United States — State
- **California Invasion of Privacy Act (CIPA) / Penal Code § 632** — Two-party (all-party) consent required for recording confidential communications in California; Mira's "opt-in only" design and user-consent guidance is directly responsive to this
- **Illinois BIPA (740 ILCS 14)** — Biometric Information Privacy Act; does not directly apply (no biometric data collected), but sets precedent for wearable data regulation
- Multiple other states (Florida, Maryland, Michigan, etc.) have all-party consent recording laws; product documentation must address user responsibilities

### European Union
- **GDPR (Regulation 2016/679)** — Applies to any personal data (including transcripts) of EU residents; key obligations:
  - Lawful basis for processing (consent or legitimate interest)
  - Right to erasure / right to access
  - Data minimization
  - Privacy by design and by default
  - Data Processing Agreements with AI backend providers (Google, Anthropic)
- **ePrivacy Directive 2002/58/EC** — Governs electronic communications privacy; relevant to audio capture over networks

### Other Jurisdictions
- **PIPEDA (Canada)** — Personal Information Protection and Electronic Documents Act; consent-based data collection requirements
- **PDPA (various Asia-Pacific)** — Thailand, Singapore, and others have similar consent-based recording and data protection laws

---

## 11. Environmental & Substance Compliance

### RoHS
- **EU RoHS Directive 2011/65/EU (RoHS 2) + amendment 2015/863/EU (RoHS 3)** — Restricts hazardous substances (Pb, Hg, Cd, Cr6+, PBBs, PBDEs, DEHP, BBP, DBP, DIBP) in electrical and electronic equipment; mandatory for EU market
- All PCBs, solder, and plastic components must comply

### REACH
- **EU REACH Regulation (EC) No 1907/2006** — Restricts substances of very high concern (SVHCs) in articles; frame materials (nylon, TR-90, metal alloys), lens materials, and coatings must be screened
- Suppliers must provide REACH compliance declarations

### WEEE
- **EU WEEE Directive 2012/19/EU** — Waste electrical and electronic equipment; requires producer registration in each EU member state and take-back/recycling obligations; WEEE symbol must appear on product

### California Prop 65
- **California Safe Drinking Water and Toxic Enforcement Act (Prop 65)** — Warning required if product contains listed chemicals above safe harbor levels; applies to frame materials, coatings, and battery components

### Packaging
- **EU Packaging and Packaging Waste Directive** — Recyclable packaging requirements (Mira uses 100% recyclable cardboard — compliant intent)
- **China RoHS (SJ/T 11364)** — Required for products sold in China; hazardous substance marking on product and packaging

---

## 12. Consumer Product Safety

### United States
- **CPSA / CPSC** — Consumer Product Safety Act; general duty clause requires products be free of unreasonable risks of injury
- **CPSC 16 CFR Part 1501** — Small parts regulations (nosepads, replaceable parts must not pose choking hazard if device is used near children)

### European Union
- **General Product Safety Directive (GPSD) 2001/95/EC** (transitioning to **General Product Safety Regulation (GPSR) 2023/988** effective Dec 2024) — General safety obligation for all consumer products; requires risk assessment, incident reporting, and market surveillance cooperation

---

## 13. OTA Firmware & Cybersecurity

- **ETSI EN 303 645** — Cybersecurity baseline for consumer IoT devices (EU); covers secure update mechanisms, no default passwords, vulnerability disclosure; increasingly referenced in EU Cyber Resilience Act compliance
- **EU Cyber Resilience Act (CRA)** — Regulation on cybersecurity requirements for products with digital elements; expected to apply to connected consumer devices; mandates security-by-design, OTA update capability, and vulnerability reporting
- **NIST IR 8259** — Foundational cybersecurity activities for IoT devices (US guidance, not yet mandated but widely referenced)
- OTA firmware delivery must use authenticated, encrypted update packages to prevent unauthorized firmware injection

---

## 14. Accessibility

- **ADA (Americans with Disabilities Act)** — Applies to the companion app and any web-based purchasing/support flows; WCAG 2.1 AA compliance recommended for the iOS app
- **EN 301 549** — Accessibility requirements for ICT products and services (EU); applies to the app and any software interface

---

## Summary by Market

| Market | Key Requirements |
|--------|-----------------|
| **USA** | FCC Part 15, UL 62368-1, IEC 62133-2, UN 38.3, FDA Rx lens rules, FTC/ECPA/CIPA, Prop 65, CPSC |
| **EU** | RED (CE mark), EN 62368-1, IEC 62133-2, RoHS, REACH, WEEE, GDPR, MDR (Rx lenses), GPSR, CRA, EN 303 645 |
| **Canada** | ISED RSS-247, CSA 62368-1, PIPEDA |
| **UK** | UKCA, UKCA RED equivalent, UK GDPR |
| **Global** | Bluetooth SIG qualification, UN 38.3 (shipping), IEC 62471 (optical safety), IEC 60529 (IPX2) |
