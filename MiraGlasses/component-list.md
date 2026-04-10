# Mira Glasses — Component List
*Based on device-summary.md and industry-standards.md — April 2026*

Where official specs are not publicly disclosed, components are marked **[INFERRED]** based on industry-standard analogues for this device class.

---

## 1. Frame & Mechanical

| # | Component | Spec / Notes | Qty per Unit |
|---|-----------|--------------|--------------|
| 1.1 | Front frame | Injection-molded nylon or TR-90; matte black; full-rim rectangular profile; universal bridge fit [INFERRED] | 1 |
| 1.2 | Temple arms (L + R) | Thickened hollow temple arms to house electronics; same material as frame; must accommodate battery, PCB, mic, speaker [INFERRED] | 2 |
| 1.3 | Barrel hinges | Metal alloy (stainless steel or titanium); 5-barrel or 7-barrel; spring hinge preferred for fit durability [INFERRED] | 2 |
| 1.4 | Hinge screws | M1.4 or M1.6 stainless steel screws [INFERRED] | 4–6 |
| 1.5 | Nose pad arms | Metal alloy (stainless steel); adjustable saddle bridge style | 2 |
| 1.6 | Nose pads | Silicone or soft PVC; replaceable push-fit; 3 included in box | 3 (in box) |
| 1.7 | Temple tips (ear hooks) | Soft silicone overmold over temple end for comfort [INFERRED] | 2 |
| 1.8 | Frame logo insert | "MIRA" text on outer temple — engraved, pad-printed, or laser-etched | 2 |
| 1.9 | Internal chassis / skeleton | Thin metal internal frame or ribs to maintain structural rigidity of thickened temples under electronics load [INFERRED] | 1 set |
| 1.10 | Adhesives / gaskets | Structural adhesive for display module bonding; silicone gaskets for IPX2 sealing around speaker and mic ports [INFERRED] | 1 set |

---

## 2. Display System

| # | Component | Spec / Notes | Qty per Unit |
|---|-----------|--------------|--------------|
| 2.1 | Waveguide lens — left | Thin optical waveguide substrate (glass or plastic); diffractive or geometric type; embedded in or laminated to lens; couples projector light to eye | 1 |
| 2.2 | Waveguide lens — right | Same as 2.1 | 1 |
| 2.3 | Micro-projector module — left | Micro-OLED or LCoS projector; green monochrome; min 2000 nit output; 640×480 capable; 60Hz; seated at inner lens edge / temple junction [INFERRED] | 1 |
| 2.4 | Micro-projector module — right | Same as 2.3 | 1 |
| 2.5 | Display driver IC | Drives projector at 640×480 @ 60Hz; receives display data from MCU via SPI or MIPI [INFERRED] | 1–2 |
| 2.6 | Projector flex PCB | Flexible PCB connecting projector module to main PCB; routes power and signal [INFERRED] | 2 |
| 2.7 | Optical coupling element | Lens / prism element at projector output to collimate and couple light into waveguide [INFERRED] | 2 |
| 2.8 | AR + AF lens coating | Anti-reflective and anti-fingerprint coating applied to outer lens surfaces (non-waveguide areas) | 1 process |

---

## 3. Audio System

| # | Component | Spec / Notes | Qty per Unit |
|---|-----------|--------------|--------------|
| 3.1 | MEMS microphone — left | Digital MEMS microphone; PDM or I2S output; always-on low-power mode; positioned in left temple arm | 1 |
| 3.2 | MEMS microphone — right | Same as 3.1; positioned in right temple arm | 1 |
| 3.3 | Microphone port cover / mesh | Acoustic mesh over mic port opening; provides IPX2 ingress protection while maintaining acoustic transparency | 2 |
| 3.4 | Audio DSP / codec IC | On-device audio pre-processing: noise reduction, voice activity detection (VAD), beamforming; may be integrated into main SoC [INFERRED] | 1 |
| 3.5 | Speaker driver — left | Open-ear directional micro-speaker; angled toward ear canal; positioned in left temple arm near ear | 1 |
| 3.6 | Speaker driver — right | Same as 3.5; right temple arm | 1 |
| 3.7 | Speaker amplifier IC | Class D audio amplifier for speaker drivers; may be integrated into SoC [INFERRED] | 1 |
| 3.8 | Speaker port cover / mesh | Acoustic mesh over speaker port opening; IPX2 protection | 2 |

---

## 4. Sensors

| # | Component | Spec / Notes | Qty per Unit |
|---|-----------|--------------|--------------|
| 4.1 | IMU — accelerometer + gyroscope | 6-axis IMU (combined accel + gyro); I2C or SPI interface; low-power; e.g. Bosch BMI270 or equivalent [INFERRED] | 1 |
| 4.2 | Ambient light sensor (ALS) | Environmental light sensor for adaptive display brightness; I2C interface [INFERRED] | 1 |
| 4.3 | Wear detection sensor | Infrared (IR) proximity sensor or capacitive sensor detecting on-head/off-head state; triggers auto-pause of recording [INFERRED] | 1 |

---

## 5. Compute & Connectivity

| # | Component | Spec / Notes | Qty per Unit |
|---|-----------|--------------|--------------|
| 5.1 | Main SoC / MCU | Low-power MCU or SoC with integrated BLE 5.2; handles audio I/O, display driving, sensor management, power management, BT stack, OTA DFU; e.g. Nordic nRF5340 or equivalent [INFERRED] | 1 |
| 5.2 | BLE antenna | Chip antenna or PCB trace antenna for 2.4GHz BLE 5.2; must be positioned to meet FCC/CE conducted + radiated emission requirements [INFERRED] | 1 |
| 5.3 | RF matching network | Passive components (inductors, capacitors) to tune antenna impedance to 50Ω [INFERRED] | 1 set |
| 5.4 | Crystal oscillator | 32MHz (or 32.768kHz RTC) oscillator for SoC clock reference [INFERRED] | 1–2 |
| 5.5 | Flash memory | External NOR flash for firmware storage, if not sufficient on-chip; e.g. 4–8MB SPI NOR [INFERRED] | 1 |
| 5.6 | Main PCB | Rigid PCB (or rigid-flex) housing SoC, power management, audio codec, sensors; designed to fit within temple arm dimensions [INFERRED] | 1 |
| 5.7 | Flex PCB interconnects | Flex PCB ribbons connecting main PCB in one temple to display modules, mic, and speaker in both temples [INFERRED] | 1 set |
| 5.8 | EMI shielding can | Metal shielding over SoC and BLE radio to meet FCC Part 15B / EN 55032 conducted and radiated emission limits [INFERRED] | 1 |
| 5.9 | Passive components | Resistors, capacitors, inductors, ferrite beads for decoupling, filtering, and matching [INFERRED] | 1 set |

---

## 6. Power System

| # | Component | Spec / Notes | Qty per Unit |
|---|-----------|--------------|--------------|
| 6.1 | Li-Po battery cell — left temple | Thin lithium polymer cell; sized to fit temple arm; combined capacity with right cell must support 10hr runtime; IEC 62133-2 and UN 38.3 certified [INFERRED] | 1 |
| 6.2 | Li-Po battery cell — right temple | Same as 6.1 [INFERRED] | 1 |
| 6.3 | Battery management IC (BMS) | Overcharge, over-discharge, short-circuit, and thermal protection; cell balancing if dual-cell in series/parallel [INFERRED] | 1 |
| 6.4 | Power management IC (PMIC) | Regulates battery voltage to supply rails for SoC, display, audio, sensors; provides sleep/wake power gating [INFERRED] | 1 |
| 6.5 | Magnetic charging contacts | Spring-loaded pogo pins or magnetic contact pads on temple arm for mating with magnetic charger cable | 2–4 contacts |
| 6.6 | Charging IC | USB-PD or constant-current/constant-voltage charger IC enabling 40-minute charge time [INFERRED] | 1 |
| 6.7 | NTC thermistor | Temperature sensing for battery thermal protection during charge/discharge [INFERRED] | 1 |

---

## 7. Optical Lenses

| # | Component | Spec / Notes | Qty per Unit |
|---|-----------|--------------|--------------|
| 7.1 | Non-prescription lens (L + R) | Clear lens substrate with waveguide integrated; standard clear optic; anti-reflective and anti-fingerprint coated | 2 |
| 7.2 | Prescription lens — 1.74 high-index (L + R) | Custom-ground to patient Rx; 1.74 index (thinnest/lightest available); waveguide integrated; AR + AF coated; non-refundable once ordered | 2 (Rx variant) |

---

## 8. Firmware & Software (On-Device)

| # | Component | Spec / Notes |
|---|-----------|--------------|
| 8.1 | Bootloader | Secure bootloader with signature verification; required for authenticated OTA DFU; prevents unauthorized firmware |
| 8.2 | BLE firmware stack | BLE 5.2 host + controller stack (e.g. Zephyr BLE or Nordic SoftDevice); must be Bluetooth SIG qualified |
| 8.3 | Audio firmware | Microphone capture, VAD, beamforming DSP routines, speaker playback pipeline |
| 8.4 | Display firmware | Display driver, frame buffer management, brightness control |
| 8.5 | Sensor firmware | IMU, ALS, and wear-detection polling and interrupt handling |
| 8.6 | Power management firmware | Sleep/wake state machine, battery monitoring, thermal management |
| 8.7 | OTA DFU module | BLE-based device firmware update; encrypted and authenticated update packages |

---

## 9. Regulatory & Compliance Components

These are not functional hardware but are required by regulation and must be accounted for in production.

| # | Component | Required By |
|---|-----------|------------|
| 9.1 | FCC ID label (US units) | FCC Part 15 |
| 9.2 | IC certification label (Canada units) | ISED RSS-247 |
| 9.3 | CE mark label (EU units) | RED 2014/53/EU |
| 9.4 | UKCA mark label (UK units) | UK RED |
| 9.5 | WEEE symbol label (EU units) | WEEE Directive 2012/19/EU |
| 9.6 | Battery disposal symbol | EU Battery Regulation 2023/1542 |
| 9.7 | RoHS compliance marking | EU RoHS 2011/65/EU |
| 9.8 | Serial number / lot code label | Traceability; GPSR |
| 9.9 | Prop 65 warning label (CA units, if applicable) | California Prop 65 |
| 9.10 | China RoHS hazardous substance table | SJ/T 11364 (CN units) |

---

## 10. In-Box Accessories

| # | Component | Spec / Notes | Qty per Unit |
|---|-----------|--------------|--------------|
| 10.1 | Magnetic charging cable | Magnetic connector mates with charging contacts on temple; USB-C on opposite end | 1 |
| 10.2 | USB-C power adapter | USB-C wall adapter; compatible with magnetic charging cable; regional plug variant per market | 1 |
| 10.3 | Glasses case | Rigid protective case; sleek design (not a charging case — separate SKU) | 1 |
| 10.4 | Microfiber cleaning cloth | Lens-safe cloth | 1 |
| 10.5 | Replacement nosepads | Silicone; same spec as installed nosepads; 3 total in box (2 installed + 1 spare per side implied, or 3 extra) | 3 |
| 10.6 | Quick start guide / user manual | Printed; includes recording consent guidance, warranty info, regulatory notices; language set per market | 1 |
| 10.7 | Regulatory insert card | FCC/IC/CE statements, SAR information, safety warnings | 1 |

---

## 11. Packaging

| # | Component | Spec / Notes |
|---|-----------|--------------|
| 11.1 | Outer box | 100% recyclable cardboard; branded; SKU/variant label on exterior |
| 11.2 | Inner tray / insert | Molded pulp or EVA foam to securely seat glasses and accessories; prevents movement during shipping |
| 11.3 | Plastic-free wrapping | No single-use plastic per sustainability commitment (recyclable cardboard only) |

---

## Key Component Risk Notes

| Component | Risk | Mitigation |
|-----------|------|------------|
| Waveguide lens modules (2.1–2.2) | Highest complexity and cost; limited supplier base globally | Qualify 2+ waveguide suppliers; maintain safety stock |
| Micro-projector modules (2.3–2.4) | Specialized optical component; long lead times | Early PO placement; NPI qualification with supplier |
| Main SoC with BLE 5.2 (5.1) | Requires Bluetooth SIG QDID certification; supply chain risk for specific ICs | Certify early; identify pin-compatible alternates |
| Li-Po battery cells (6.1–6.2) | Must carry IEC 62133-2 + UN 38.3 certs; air shipment restrictions | Source cells with certs pre-qualified; buffer stock |
| 1.74 high-index Rx lenses (7.2) | Custom-grind per patient Rx; non-refundable; long lead time | Clear ordering and Rx verification workflow before grinding |
| MEMS microphones (3.1–3.2) | Always-on audio use case requires very low power spec | Validate power draw against 10hr battery target |
