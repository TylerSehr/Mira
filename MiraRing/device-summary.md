# Mira Ring — Device Summary
**Prepared for:** Supplier Sourcing & Manufacturing
**Date:** April 2026
**Source data:** StartingData/ folder (miradump.txt, product-description-scraped.txt, hardware-description.txt, scrapedmirawebsite.txt, product images, hardware cost screenshot)

> **Data confidence notation used throughout:**
> - No tag = confirmed from official product page, press, or App Store
> - [INFERRED] = derived from industry analogues, visual inspection of product images, or logical extrapolation

---

## 1. Product Overview

The Mira Ring is the dedicated physical input controller for the Mira AI smart glasses system. It is a Bluetooth-connected smart ring worn on the index finger that allows users to interact with the Mira Glasses without touching the glasses frame. It ships bundled with every Mira Glasses purchase and is not sold separately.

The ring is designed to be discreet and professional — it resembles a conventional wide-band fashion ring with no visible buttons, ports, or indicator lights on the exterior surface. Its primary design constraint is invisibility: users should be able to control their glasses in meetings or social settings without drawing attention.

---

## 2. System Role

The Mira Ring sits at the top of the input chain in the Mira hardware ecosystem:

```
[Mira Ring] — BLE → [Mira Glasses] — BLE → [iPhone / Mira App] — HTTPS → [Cloud AI]
```

Touch gestures on the ring translate to commands relayed through the glasses to the iPhone app and AI backend. The ring eliminates the need to physically touch the glasses frame for any control input.

---

## 3. Physical Form Factor

### 3.1 Overall Design
- **Type:** Wide flat-band finger ring
- **Finger:** Index finger (confirmed — sizing is collected at checkout)
- **Color:** Matte black (sole color option)
- **Profile:** Wide, flat, cylindrical band with smooth rounded outer edges — no visible buttons, seams, ports, or LEDs on the exterior surface
- **Aesthetic intent:** Resembles a conventional fashion/statement ring; electronics are fully concealed

### 3.2 Construction (from visual inspection of product images)
- **Outer shell:** Smooth matte black material — consistent with injection-molded polycarbonate (PC) or a hard resin/epoxy over-mold [INFERRED]
- **Inner bore:** Bright silver/chrome metallic ring visible on the inner diameter — likely a stainless steel or aluminum structural inner band [INFERRED]
- **Inner surface contacts:** Small raised circular elements visible on the inner bore surface — consistent with magnetic charging contacts (2–3 pin pogo-style or magnetic pad contacts) [INFERRED from images]
- **Band width:** Visually estimated ~8–10mm wide [INFERRED from images; not officially disclosed]
- **Band thickness (wall):** Appears ~3–5mm radial wall thickness to accommodate electronics [INFERRED from images]
- **Sealing:** 5ATM (50 meters) water resistance implies full-perimeter hermetic seal between outer shell and inner band

### 3.3 Sizing
- Available in multiple sizes corresponding to standard ring sizes
- Customers select index finger ring size at checkout — option to "send it later" (measure post-purchase) or enter size at time of order
- Exact size range not publicly disclosed

---

## 4. Technical Specifications

### 4.1 Input / Sensing
| Parameter | Value | Confidence |
|-----------|-------|------------|
| Sensing technology | Touch-sensitive surface | Confirmed |
| Sensing type | Capacitive touch | [INFERRED] |
| Gesture types | Taps, swipes, holds [INFERRED] | Confirmed (gestures exist) |
| Confirmed input actions | Answer/end calls, activate AI, navigate menus, skip/control media | Confirmed |

No physical buttons are visible on any product imagery. All input is through the touch-sensitive outer surface.

### 4.2 Connectivity
| Parameter | Value | Confidence |
|-----------|-------|------------|
| Protocol | Bluetooth Low Energy | Confirmed |
| BLE version | 5.2 [INFERRED — matches glasses spec] | [INFERRED] |
| Pairing | Pairs with Mira Glasses (and/or iPhone directly) | Confirmed (seamless pairing) |

### 4.3 Power & Charging
| Parameter | Value | Confidence |
|-----------|-------|------------|
| Battery type | Lithium-polymer (LiPo) | [INFERRED] |
| Battery capacity | Not disclosed | Unknown |
| Battery life | Not disclosed | Unknown |
| Charging method | Magnetic charging cradle | Confirmed |
| Charger included | Yes — magnetic ring charger in box | Confirmed |
| Charging connector (cradle) | USB-C (visible in product image) | [INFERRED from images] |
| Charging cradle form | Circular disc with raised center post; ring sits over post | [INFERRED from images] |

### 4.4 Durability
| Parameter | Value | Confidence |
|-----------|-------|------------|
| Water resistance | 5ATM (50 meters) | Confirmed |
| IP rating equivalent | ~IP68 | [INFERRED] |

### 4.5 On-Device Electronics (Inferred)
| Component | Description |
|-----------|-------------|
| MCU | Low-power embedded microcontroller (e.g., Nordic nRF52 series or equivalent BLE SoC) [INFERRED] |
| Touch controller | Capacitive touch sensing IC integrated with or separate from MCU [INFERRED] |
| Battery | Small LiPo cell sized to fit within ring band wall [INFERRED] |
| Charging circuit | Magnetic/inductive or pogo-pin charging management IC [INFERRED] |
| Antenna | PCB trace antenna for BLE, integrated within ring structure [INFERRED] |

---

## 5. In-Box Contents (Ring-Related)

From the confirmed in-box listing:
- Mira Ring (control ring)
- Magnetic ring charger (charging cradle with USB-C connection)

The ring ships alongside: Mira Glasses, glasses case, 3 replaceable nosepads, microfiber cloth, and magnetic glasses charger + USB-C adapter.

---

## 6. Cost & Manufacturing Data

The following data was sourced from an internal hardware cost breakdown (Hardware Phase I, 2000-unit production run):

| Line Item | Cost (USD) |
|-----------|-----------|
| Ring ex-factory cost | $42.50 |
| Ring import tariff | $14.875 (35% tariff rate) |
| **Ring landed cost (est.)** | **~$57.38** |

**Notes:**
- The 35% tariff rate confirms the ring is manufactured in China and imported into the US
- Phase I volume: 2000 units (noted as "2000 units + 2000" in cost sheet)
- NRE (non-recurring engineering) costs are noted as separate and not counted in per-unit cost
- The glasses ex-factory cost at Phase I is $365; the ring at $42.50 represents ~10% of the glasses cost, suggesting it is a less complex device
- Shared shipping/logistics line of $5/unit covers the full kit (glasses + ring)
- Total per-unit cost (glasses + ring + shipping + tariffs): **$493**

**Supplier sourcing target:** Reducing the $42.50 ex-factory ring cost and/or the 35% tariff impact is a primary lever for margin improvement. Alternative: sourcing from a country with lower tariff exposure.

---

## 7. Design Constraints & Requirements Summary

| Constraint | Requirement |
|-----------|------------|
| Aesthetics | Must resemble a conventional fashion ring — no visible electronics, buttons, or ports |
| Water resistance | 5ATM (50 meters) minimum — full hermetic sealing required |
| Input | Capacitive touch surface covering outer shell |
| Connectivity | BLE 5.x; must pair reliably with Mira Glasses |
| Charging | Magnetic charging (no exposed port) |
| Sizing | Multiple standard index finger sizes required |
| Color | Matte black (current single SKU) |
| Weight | Must feel comfortable for all-day wear; ring form factor naturally constrains to low weight |
| Discreetness | Minimal visual profile in professional settings |
| Battery life | Not specified — must support all-day use relative to glasses (10hr glasses battery sets the bar) |

---

## 8. Comparable Market Devices

The Mira Ring is functionally similar to the following smart ring product categories:

| Device | Relevance |
|--------|-----------|
| Oura Ring Gen 3/4 | Smart ring form factor, BLE, LiPo, magnetic charging, multi-size — well-established OEM supply chain |
| Samsung Galaxy Ring | BLE smart ring with touch/gesture input, magnetic charging cradle, titanium body |
| RingConn Smart Ring | Budget smart ring — demonstrates low-cost Chinese OEM supply chain for this form factor |
| Ultrahuman Ring Air | Lightweight smart ring, capacitive touch, BLE — design reference for minimal form factor |
| Various Alibaba "smart ring" OEM platforms | Base hardware platforms that could be customized for Mira's specific gesture-control use case |

The Mira Ring is simpler than health-tracking smart rings (no PPG/SpO2/temperature sensors) — its electronics payload is lighter: BLE SoC + capacitive touch + battery + charging circuit only. This should make it easier and cheaper to source or build on an existing OEM platform.

---

## 9. Key Open Questions for Supplier Engagement

The following specifications are not publicly disclosed and will need to be confirmed or defined with the supplier:

1. **Band width and diameter range** — exact dimensions for each size SKU
2. **Battery capacity (mAh)** — needed for BOM costing and compliance docs
3. **Battery life target** — hours of active use per charge
4. **Gesture vocabulary** — full list of gestures (tap count, swipe direction, hold duration) needed for touch controller firmware spec
5. **MCU / BLE SoC** — whether Mira specifies the chip or defers to the manufacturer
6. **Charging contact type** — pogo pin vs. inductive coil (affects charger cradle design)
7. **Shell material** — polycarbonate, resin, or metal outer shell
8. **Inner structural band material** — stainless steel vs. aluminum vs. resin
9. **OTA firmware update** — whether the ring supports BLE DFU (over-the-air updates)
10. **Regulatory certifications required** — FCC, CE, RoHS, REACH for target markets
11. **Size range** — minimum and maximum ring sizes offered, number of SKUs
12. **Current manufacturer** — understanding the existing supply relationship and any tooling already in place

---

## 10. Summary Table

| Attribute | Value |
|-----------|-------|
| Product type | Smart ring controller |
| Finger | Index finger |
| Color | Matte black |
| Outer surface | Touch-sensitive (capacitive) |
| Connectivity | Bluetooth BLE 5.2 [INFERRED] |
| Water resistance | 5ATM (50 meters) |
| Charging | Magnetic cradle (USB-C cradle) |
| Battery | LiPo [INFERRED], capacity unknown |
| Battery life | Not disclosed |
| Size options | Multiple (index finger ring sizes) |
| Sold separately | No — bundled with Mira Glasses |
| Ex-factory cost (Phase I, 2000 units) | $42.50 |
| Import tariff (US, from China) | 35% (~$14.88) |
| Landed cost estimate | ~$57.38 |
| Current production stage | Phase I (2000-unit batches) |
| Manufacturing origin | China (confirmed by tariff structure) |
