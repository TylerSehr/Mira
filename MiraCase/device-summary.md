# MiraCase — Device Summary
*Compiled from StartingData folder — April 2026*

---

## Overview

The MiraCase is a premium charging case designed to house, protect, and charge the full Mira smart glasses system: the Mira Glasses and the Mira Ring. It consolidates the currently separate magnetic glasses charger and magnetic ring charger into a single carry case that can be topped up via USB-C. The case is a core part of the Mira product experience and must reflect the brand's premium positioning.

---

## Devices the Case Must Accommodate

### Mira Glasses
| Parameter | Value |
|-----------|-------|
| Dimensions | 140mm (W) × 45mm (H) × 150mm (D) |
| Frame width | 145.6mm (5.73 in) |
| Weight | 39g |
| Charging method (device side) | Magnetic |
| Full charge time | 40 minutes |
| Water resistance | IPX2 |
| Frame color | Matte Black |

### Mira Ring
| Parameter | Value |
|-----------|-------|
| Type | Index finger ring controller |
| Sizes | 7–14 (size 14 optional) |
| Charging method (device side) | Magnetic ring charger |
| Water resistance | 5ATM (50 meters) |
| Battery | Small Li-Po (capacity not disclosed) |

---

## MiraCase Requirements

### Functional
- **Dual charging:** Must charge both the Mira Glasses and the Mira Ring simultaneously
- **Glasses charging interface:** Pogo pin contacts built into the case shell (preferred) OR integrated magnetic wire charger
- **Ring charging interface:** Magnetic ring charger dock integrated into the case interior
- **Input port:** USB-C (for charging the case battery from external power)
- **LED indicator:** At least one LED to indicate charging status / battery level
- **Battery capacity:** Minimum 500mAh internal battery (passthrough charging acceptable if battery is included)
- **Protection:** Must adequately protect the glasses (lenses and frame) during transport and storage

### Physical / Industrial Design
- **Material preference:** Leather (soft/premium) or polished silver/chrome metal shell — as shown in reference images
- **Design references:**
  - Organic sculptural silver hard shell (pebble/blob form factor) — reference image (2).webp
  - Black leather envelope-style soft case — reference image (3).webp
  - Gentle Monster-style silver metallic hard case — reference image (1).webp
  - Pogo pin internal charging rail mounted to inner shell — reference IMG_3112.webp
- **Interior:** Soft-lined (microfiber or velvet) to prevent lens scratching
- **Ring compartment:** Dedicated recessed dock or slot for the ring within the case interior

### Production
| Parameter | Value |
|-----------|-------|
| Target volume | 2,000 units total |
| Monthly run rate | 500 units/month (up to 2,000/month potential) |
| Target lead time | Within 2 months |

---

## Electrical Architecture (Inferred)

```
[USB-C Input Port]
        |
        v
[Internal Battery (≥500mAh) + Charge Controller IC]
        |
        +---> [Glasses Charging Output]
        |       Pogo pin contacts OR magnetic connector
        |       aligned to glasses temple charging point
        |
        +---> [Ring Charging Output]
                Magnetic ring charger dock
                (coil or contact-based)
```

- USB-C input charges the internal battery
- Internal battery simultaneously or sequentially charges glasses and ring when placed in case
- LED(s) indicate: charging in progress / full charge / internal battery level

---

## Key Design Constraints

| Constraint | Detail |
|-----------|--------|
| Glasses are delicate optical devices | Interior must be fully soft-lined; waveguide lenses must not contact hard surfaces |
| Glasses charge magnetically | Pogo pin or magnetic contact must align precisely to charging contacts on temple arm |
| Ring sizes vary (7–14) | Ring dock must accommodate variable ring diameter or use a universal magnetic surface |
| Matte Black frame | Interior case color / lining should complement black hardware |
| Premium positioning | Case is included in a $649+ product — material and finish quality must match |
| Lead time constraint | 2-month target requires supplier with existing tooling or semi-custom capability |

---

## Reference: Current In-Box Charging Accessories (to be replaced/integrated)

Per the existing Mira product box contents:
- Magnetic charger (for glasses) + USB-C adapter
- Magnetic ring charger (separate accessory)

The MiraCase consolidates these into a single charging case, removing the need for loose cable accessories.

---

## Manufacturing Notes

- Case shell (if hard): Likely injection-molded ABS or zinc alloy (for silver/chrome finish), or aluminum die-cast for premium feel
- Case exterior (if leather): PU leather or genuine leather wrap over rigid inner shell
- Pogo pin charging rail: Standard spring-loaded brass pogo pins; requires precise positional alignment to glasses temple charging contacts — alignment fixtures or magnetic guidance recommended
- LED driver: Simple single-cell LiPo management IC (e.g., TP4056 class) with LED status output
- USB-C port: Standard USB-C 5V/1A or 5V/2A input sufficient for ≥500mAh battery
- Ring charging dock: Magnetic contact ring or small Qi coil inset into a ring-shaped recess
