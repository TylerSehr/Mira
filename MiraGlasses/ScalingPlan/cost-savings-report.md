# Mira Glasses — Cost Savings Investigation Report

*April 2026 | Based on current cost structure and supplier research*

---

## Current Cost Structure

The $649 selling price includes both the Mira Glasses and the Mira Ring. All costs below reflect the true current state.

| Line Item              | Cost              |
| ---------------------- | ----------------- |
| Glasses                | $365.00           |
| Ring (Jstyle, current) | $42.50            |
| Box                    | $3.00             |
| Shipping / Logistics   | $5.00             |
| Last Mile              | $12.00            |
| Glasses Tariff         | $66.00            |
| Ring Tariff            | $14.88            |
| CAC                    | $100.00           |
| **Total**        | **$608.38** |

**Selling price:** $649 (includes glasses + ring)
**True contribution margin (all-in incl. CAC):** **6.3%** (($649 − $608.38) / $649)
**Gross margin (excl. CAC):** **21.7%** (($649 − $508.38) / $649)
**Target:** Cut 20% from glasses cost → from $365 to **$292** (saving $73/unit)
**Volume:** 200–1,000 units/month

### Cost structure breakdown

| Line Item              | Cost              | % of Revenue    |
| ---------------------- | ----------------- | --------------- |
| Glasses                | $365.00           | 56.2%           |
| CAC                    | $100.00           | 15.4%           |
| Ring (incl. tariff)    | $57.38            | 8.8%            |
| Glasses Tariff         | $66.00            | 10.2%           |
| Last Mile              | $12.00            | 1.8%            |
| Shipping / Logistics   | $5.00             | 0.8%            |
| Box                    | $3.00             | 0.5%            |
| **Total costs**  | **$608.38** | **93.7%** |
| **Contribution** | **$40.62**  | **6.3%**  |

### Margin sensitivity table

Tariff figures are calculated proportionally at current effective rates (glasses: 18.1%, ring: 35%).

| Glasses Cost                     | Ring Cost                  | Other Costs | CAC   | Total   | Margin at $649 |
| -------------------------------- | -------------------------- | ----------- | ----- | ------- | -------------- |
| $365 + $66T (current)            | $42.50 + $14.88T (current) | $20.00      | $100  | $608.38 | **6.3%**       |
| $365 + $66T (current)            | $15 + $5.25T (target)      | $20.00      | $100  | $571.25 | **12.0%**      |
| $292 + $52.85T (−20%)           | $42.50 + $14.88T (current) | $20.00      | $100  | $522.23 | **19.5%**      |
| $292 + $52.85T (−20%)           | $15 + $5.25T (target)      | $20.00      | $100  | $485.10 | **25.3%**      |
| $292 + $27T (−20% + HTS ruling) | $15 + $5.25T (target)      | $20.00      | $100  | $459.25 | **29.2%**      |

**Key observation:** CAC at $100 (15.4% of revenue) is the single largest margin compressor after the glasses themselves. Ring sourcing at current Jstyle pricing ($42.50 + $14.88 tariff = $57.38) costs more per unit than last mile, shipping, and box combined. Reducing ring to the $9–16 target range is the fastest near-term margin lever outside of the glasses cost itself.

---

## Estimated Glasses Cost Breakdown

Display optics are the dominant cost driver. Working backward from $365 at 200–1,000 units/month:

| Category                                            | Est. Cost | % of Total |
| --------------------------------------------------- | --------- | ---------- |
| Display optics (waveguides + projectors, binocular) | $220–250 | 60–68%    |
| PCB/PCBA + SoC + passives                           | $35–50   | 10–14%    |
| Power (2x Li-Po, BMS, PMIC, charging)               | $18–22   | 5–6%      |
| Frame + mechanical                                  | $12–18   | 3–5%      |
| Audio (mics, speakers, codec)                       | $10–14   | 3–4%      |
| Assembly labor                                      | $15–20   | 4–5%      |
| Accessories (charger, cable, cloth, manual)         | $6–8     | 2%         |
| Sensors                                             | $4–5     | 1%         |
| Labels                                              | $1        | <1%        |

**Key insight:** Display optics alone represent ~60–68% of total glasses cost. Any meaningful cost reduction strategy must address this component first.

---

## Current Supplier Context

**Current display optics supplier: Meta-Bounds (Zhuhai Mojie Technology Co., Ltd.)**

- Founded 2021, Zhuhai, Guangdong
- Real, legitimate supplier with design wins: OPPO Air Glass 2, ZTE, Lenovo, Baidu, SoftBank
- CES 2026 Innovation Award winner for 25g monocular and **38g full-color binocular** glasses — directly comparable to Mira's 39g spec
- Also works with Amazon — Mira is currently one of their **smaller customers**

**Estimated Meta-Bounds margin on Mira order:**

| Scenario              | Est. COGS | Gross Margin at $365 |
| --------------------- | --------- | -------------------- |
| Conservative          | $290      | ~21%                 |
| Mid (most likely)     | $245      | ~33%                 |
| Optimistic (for them) | $205      | ~44%                 |

Mid-case: Meta-Bounds is running approximately **30–35% gross margin** on the $365 price.

**Current payment terms:** 100% upfront — eliminates Meta-Bounds' working capital risk entirely. This is not currently reflected in pricing and represents unused leverage.

---

## Path 1: Display Optics — Competitive RFQ

**Potential saving: $30–40/unit**
**Effort: Medium | Timeline: 4–8 weeks**

This is the single highest-impact lever available at current volumes. The display optics are ~65% of glasses cost and Meta-Bounds knows Mira has no alternative quotes on the table.

### Recommended suppliers to RFQ:

**Optiark (光舟半导体) — Shenzhen**

- Most directly comparable to Meta-Bounds technically
- Same resin diffractive waveguide approach
- LHASA-5 binocular system uses a single projector to drive both eyes — potentially simpler and cheaper than two separate projector modules
- Co-founded by Tapani Levola (Nokia's waveguide team — genuine IP pedigree)
- Confirmed in Rokid AI Glasses (shipping product)
- Backed by Tencent, ByteDance
- Contact: optiark.com

**Lochn Optics (珑璟光电) — Shenzhen**

- Most immediately accessible for sample orders
- Public price listed on Global Sources: **$180/unit for a waveguide module**
- ISO 9001/14001 certified; 10,000+ units/month capacity
- Active B2B profile on Global Sources — responds to small inquiries
- Contact: search "Lochn Optics" or "珑璟光电" on globalsources.com

**Greatar / Zhige Technology (至格科技) — Beijing**

- Confirmed waveguide supplier for Even Realities G1/G2 (a direct Mira competitor)
- 100,000 units/month automated production capacity
- Investors include Xiaomi, OPPO, SMIC
- Higher volume orientation — harder to engage at current Mira scale
- Contact: via 36Kr or LinkedIn

### Negotiation approach with Meta-Bounds:

Use Optiark and Lochn quotes to negotiate. Meta-Bounds has ~30–35% margin — they can move to $310–330 and still operate at 15–25% margin. They don't want to lose even a small customer to Optiark. Lochn's public $180 module price is a credible anchor.

**Do not lead with volume promises** — at 200–1,000 units/month Mira is a small account and Meta-Bounds knows it. Lead with the competitive quotes and the 100% upfront payment terms.

---

## Path 2: Leverage 100% Upfront Payment Terms

**Potential saving: $15–25/unit (4–7%)**
**Effort: Low | Timeline: Immediate**

Mira currently pays 100% upfront, which:

- Eliminates Meta-Bounds' receivables risk entirely
- Pre-finances their production run
- Represents zero working capital cost to them

Most customers pay net-30 or net-60. Meta-Bounds carries that receivable as a cost of doing business — with Mira they carry nothing. This advantage is real and quantifiable but **is not currently priced in**.

**Action:** In the next pricing discussion, explicitly call out the 100% upfront as a concession deserving a 5–8% price reduction. This is the cleanest, most defensible ask and requires no volume commitment or supplier switching threat.

---

## Path 3: Customer Furnished Materials (CFM)

**Potential saving: $30–50/unit**
**Effort: High | Timeline: 3–6 months**

Mira sources the non-optical components directly — frame, PCB/PCBA, battery, audio components — and provides them to Meta-Bounds (or another assembler) as supplied materials. Meta-Bounds contributes only their waveguide + projector system and final assembly.

**Why this works:**

- Removes Meta-Bounds' markup on commodity components they're currently sourcing and re-selling at margin
- Mira gets direct control over component quality, lead times, and cost
- Meta-Bounds' margin on their core product (the optics) stays intact — making it genuinely win-win
- Aligns with Mira's long-term interest in owning more of the supply chain

**Why this is difficult now:**

- Mira is currently a small customer — Meta-Bounds may not want to manage CFM complexity for a low-priority account
- Requires Mira to build direct supplier relationships for frame, PCB, battery, etc.
- Adds procurement and logistics overhead on Mira's side

**Best path:** Begin direct supplier qualification in parallel (see Path 5), with CFM as the medium-term goal once volume grows.

---

## Path 4: Tariff Optimization

**Potential saving: $27–39/unit**
**Effort: Low–Medium | Timeline: 6–12 weeks for binding ruling**

### Critical development — IEEPA tariffs struck down

On February 20, 2026, the U.S. Supreme Court (*Learning Resources, Inc. v. Trump*) **invalidated all IEEPA-based tariffs**. The 20% fentanyl tariff, 10% baseline reciprocal tariff, and 125% China escalation are all gone. Only Section 301 tariffs remain.

**Current tariff is likely overstated.** The $66 tariff on $365 glasses (~18%) may not reflect the post-ruling environment.

### HTS Classification — the highest-impact lever

| HTS Code               | Classification                                        | Rate           | Tariff on $365 |
| ---------------------- | ----------------------------------------------------- | -------------- | -------------- |
| **8517.62.0090** | Wireless transmission apparatus (Bluetooth-dominant)  | **7.5%** | **$27**  |
| 9031.80.8085           | Measuring/checking instruments NES (display-dominant) | 25%            | $91            |
| 9013.80.90             | Optical appliances/instruments                        | 25%            | $91            |
| 8543.70.9860           | Electrical machines, individual functions             | 25%            | $91            |

**CBP precedent strongly supports arguing 8517.62:**

- Lucyd Loud smart audio glasses (CBP Ruling N307688, Dec 2019) classified under 8517.62 — nearly identical product (Bluetooth glasses, dual mics, dual speakers, no camera)
- CBP has consistently rejected 9004 (spectacles) for smart glasses
- Mira's dominant function argument: Bluetooth 5.2 data transmission, always-on audio capture, wireless connectivity to iPhone

**If 8517.62 is secured:** tariff drops from ~$66 to ~$27 — saving **$39/unit** without touching the glasses cost at all.

### Action: Request CBP Binding Ruling

- File a binding ruling request with CBP arguing for 8517.62
- Cite Lucyd Loud ruling (N307688) as direct precedent
- Emphasize: Bluetooth 5.2, dual MEMS mics, dual speakers, wireless data transmission as dominant function
- Engage a licensed customs broker or trade attorney specializing in consumer electronics

### Section 301 Exclusions — not currently viable

- No active exclusion petition window is open for this product category
- No precedent exists of smart glasses receiving an exclusion
- The 178 exclusions extended through November 2026 cover solar/EV/batteries only
- Monitor USTR for new Section 301 investigation proceedings which would create a new petition window

### Third-country assembly (longer term)

Final assembly in Vietnam or Mexico using Chinese-origin components eliminates Section 301 applicability entirely if substantial transformation rules are satisfied. Several Shenzhen ODMs have Vietnam operations. Not viable at current volume but worth evaluating at 2,000+ units/month.

---

## Path 5: Volume Pricing on Non-Display Components

**Potential saving: $17–26/unit**
**Effort: Medium | Timeline: 2–4 months**

At 200–1,000 units/month, commodity components are still at near-sample pricing. Committing to monthly runs unlocks better rates:

| Component                                                     | Current Est. | Potential Saving |
| ------------------------------------------------------------- | ------------ | ---------------- |
| PCB/PCBA (committed monthly run at JLCPCB/Kinergy)            | $35–50       | $7–10            |
| Li-Po batteries (direct to Grepow or ATL, monthly commitment) | $16–22       | $5–8             |
| Frame (committed run pricing with Dongguan ODM)               | $12–18       | $5–8             |

The key is shifting from ad-hoc orders to committed monthly purchase agreements. At 200–1,000 units/month these suppliers will move from prototype to production pricing.

**Note:** This only applies if Mira is currently buying these components through Meta-Bounds (where Meta-Bounds marks them up). If Meta-Bounds is supplying a complete unit, CFM (Path 3) is required to unlock this saving.

---

## Path 6: Ring Cost Reduction

**Potential saving: $37–45/unit (ring + tariff combined)**
**Effort: Low–Medium | Timeline: 4–8 weeks**

The ring at current Jstyle pricing ($42.50 + $14.88 tariff = $57.38/unit) is the second largest cost line item after the glasses themselves, representing 8.8% of revenue. Reducing ring cost to the $15 target brings all-in ring cost to ~$20.25 ($15 + $5.25 tariff), saving **$37.13/unit**.

### Current ring sourcing

- **Supplier:** Jstyle
- **Current price:** $42.50/unit
- **Target price:** $9–16/unit from alternative Shenzhen suppliers
- **Ring tariff at current price:** $14.88 (35% effective rate)
- **Ring tariff at $15 target:** ~$5.25

### Alternative ring suppliers to RFQ

The Shenzhen smart ring ecosystem is well-developed — dozens of suppliers make touch-sensitive BLE rings comparable to the Mira Ring spec. The ring requires:

- Capacitive touch surface (single tap, swipe up, swipe down)
- BLE connectivity
- Custom GATT profile (gesture events: 0x01, 0x02, 0x03)
- 5ATM water resistance
- Magnetic ring charger
- Sizes 7–14

At 200–1,000 units/month, multiple Shenzhen suppliers can hit $9–16/unit on this spec. Sourcing from an alternative supplier at $12 all-in (product + charger) versus Jstyle at $42.50 saves **$30.50 on product alone** before tariff reduction.


---

## Path 7: Scope Reduction with Meta-Bounds

**Potential saving: $20–40/unit**
**Effort: Medium | Timeline: 2–3 months**

Rather than buying a complete glasses assembly, buy only the **optical module** (waveguide + projector system, integrated) from Meta-Bounds and handle final assembly at a separate Shenzhen CM.

- Meta-Bounds does less work, has lower cost, can charge less
- Their margin on their core IP (the optics) stays strong
- Final assembly at a commodity Shenzhen CM at $15–20/unit
- Mira gains more control over non-optical components

This is a stepping stone toward full CFM without requiring Mira to manage the entire component supply chain immediately.

---

## Summary — Prioritized Action Plan

| Priority | Path | Saving/Unit | Effort | Timeline |
|---|---|---|---|---|
| 1 | CBP Binding Ruling (HTS 8517.62) | $27-39 | Low | 6-12 weeks |
| 2 | Competitive RFQ: Optiark + Lochn (glasses) | $30-40 | Medium | 4-8 weeks |
| 3 | Ring cost reduction to $15 target | $37-45 | Low-Medium | 4-8 weeks |
| 4 | Leverage 100% upfront in negotiation | $15-25 | Low | Immediate |
| 5 | Volume pricing on non-display components | $17-26 | Medium | 2-4 months |
| 6 | Scope reduction (optical module only) | $20-40 | Medium | 2-3 months |
| 7 | Customer Furnished Materials (CFM) | $30-50 | High | 3-6 months |

### Combined impact on contribution margin

Starting from current true contribution margin of 6.3% ($40.62 on $649):

| Actions | Additional Saving | New Total Cost | Contribution Margin |
|---|---|---|---|
| Current state | baseline | $608.38 | 6.3% |
| + Ring to $15 (Path 6) | $37.13 | $571.25 | 12.0% |
| + CBP ruling 8517.62 (Path 4) | $39.00 | $532.25 | 18.1% |
| + Glasses RFQ -$35 (Path 1) | $35.00 | $497.25 | 23.5% |
| + 100% upfront leverage -$20 (Path 2) | $20.00 | $477.25 | 26.5% |

**Recommended immediate actions:**

1. RFQ alternative ring suppliers in Shenzhen — clearest near-term margin win at $37/unit
2. Engage a customs broker to file CBP binding ruling for 8517.62 — $39/unit with no product changes
3. Request RFQs from Optiark and Lochn this week for glasses optics
4. Use all competitive quotes + 100% upfront as explicit leverage with Meta-Bounds and Jstyle

---

*Report compiled April 2026. All cost estimates based on Shenzhen manufacturing context at 200–1,000 units/month. Tariff analysis reflects post-Supreme Court IEEPA ruling environment (February 2026). Supplier contact details in supplier-list.md (pending).*
