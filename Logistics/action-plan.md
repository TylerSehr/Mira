# Logistics Action Plan — Mira

**Product:** Mira Glasses + MiraCase (charging case, Li-ion) + Mira Ring
**Production cost:** ~\$500/unit (current) — targeting \$150-200 for viability
**Retail price:** \$650
**Monthly volume:** 200-1,000 units (estimated)
**Origin:** Shenzhen → US (DTC ecommerce)

---

## Strategy: Three Phases

### Phase 1: Samples & Early Production
**Self-managed QC operation in Shenzhen**

- Hire a part-time QC contractor in Shenzhen (~\$400-800/mo)
- They receive units from the factory, inspect 100%, and coordinate with the manufacturer on defects
- Ship approved units via DDP freight forwarder (YunExpress/4PX) direct to US customers
- No US inventory, no 3PL — ship per order as orders come in
- Use this phase to establish your QC checklist: pogo pin alignment, charging function, hinge feel, lens protection, ring dock fit, battery function, LED indicators, cosmetic finish

**Upfront cost:** ~\$0 (no inventory pre-purchase, no 3PL contracts)
**Per-order cost:** ~\$155 (duties + DDP shipping)
**Timeline:** Runs 1-3 (~3-6 months)

### Phase 2: Early Mass Production
**Self-managed QC + Flexport (FF + US 3PL)**

- Keep your SZ QC person inspecting 100% of units
- QC-approved units are bulk-shipped via Flexport (air freight) to their US warehouse
- Flexport handles customs, duties, warehousing, pick/pack, and Shopify fulfillment
- Customers receive orders in 2-5 days via USPS/UPS
- US return address through Flexport

**Upfront cost:** \$95K-145K (bulk inventory + duties for first shipment of 500 units)
**Per-order cost:** ~\$153 (duties + Flexport freight + fulfillment + \$5K/mo min)
**Timeline:** Runs 4-8 (~6-12 months)
**Graduation criteria to Phase 3:** 3 consecutive production runs with <2% defect rate

### Phase 3: Mature Mass Production
**Third-party QC inspection firm + Flexport**

- Replace your SZ QC person with a pre-shipment inspection firm (HQTS, Pro QC International)
- Sampling-based inspection: firm visits factory 1 in 3-5 shipments, pulls random units, runs your checklist, sends pass/fail report with photos
- Flexport continues to handle everything from SZ pickup to US customer delivery
- Monitor for quality fade: material substitution, component downgrade, dimensional drift

**QC cost:** ~\$200-400 per inspection (not per month)
**Per-order cost:** ~\$150 (duties + Flexport)
**Timeline:** Run 9+ (ongoing)

---

## Immediate Action Items

### Now
- [ ] **Get HS code classification** — consult a customs broker to classify Mira Glasses (likely 8517.62), MiraCase (likely 8504.40), and Mira Ring (8517.62 or 9031.80). This determines your exact duty rate and is the biggest variable in your cost model.
- [ ] **Request quotes from Flexport, ShipBob/FreightBob, and Floship** — provide: 0.2kg, lithium battery (Class 9 DG), 200-1,000 units/mo, Shenzhen origin, US destination, Shopify integration needed.
- [ ] **Identify a QC contractor in Shenzhen** — part-time, ideally with electronics inspection experience. Can source through personal network, LinkedIn, or agencies.
- [ ] **Get DDP carrier quotes** — contact YunExpress, 4PX, and CNE for Phase 1 per-parcel rates with sensitive goods (lithium battery) surcharge.

### Before Phase 2
- [ ] **Finalize QC checklist** — document every inspection point from Phase 1 learnings
- [ ] **Set up Flexport account and Shopify integration** — do this before you need it so the transition isn't rushed
- [ ] **Model cash flow** — ensure you have \$95K-145K available for first bulk inventory purchase + duty payment
- [ ] **Establish demand forecasting process** — track order patterns from Phase 1 to predict Phase 2 inventory needs

### Before Phase 3
- [ ] **Vet QC inspection firms** — get quotes from HQTS and Pro QC International for pre-shipment inspections
- [ ] **Define quality fade monitoring** — specify which materials/components to spot-check and acceptable tolerance ranges
- [ ] **Review QC data from Phase 2** — confirm 3+ consecutive runs at <2% defect rate before graduating

---

## Key Risks

| Risk | Mitigation |
|------|-----------|
| Duties are higher than estimated | Get binding HS code ruling before committing capital to Phase 2 |
| Section 122 (10%) expires July 2026 | Potential \$50/unit savings — monitor and adjust cost model |
| Production cost stays at \$500 (negative margin) | COGS reduction is existential — prioritize above logistics optimization |
| Flexport \$5K/mo minimum in slow months | Budget for it; the simplicity is worth the premium at your stage |
| Quality fade in mature production | Never drop to zero QC; periodic third-party inspections are cheap insurance |
| Factory changes components without notice | Require written approval for any BOM changes in supplier agreement |

---

## Cost Summary

All costs assume current tariff rates (~28% on transaction value). Actual duty TBD pending HS classification.

| | Phase 1 | Phase 2 | Phase 3 |
|---|---|---|---|
| Per-order cost | ~\$155 | ~\$153 | ~\$150 |
| Delivery speed | 7-15 days | 2-5 days | 2-5 days |
| QC | Your person, 100% | Your person, 100% | Inspection firm, sampling |
| US returns | No (refund & keep) | Yes (Flexport) | Yes (Flexport) |
| Capital required | \$0 | \$95K-145K | \$95K-145K |
| Monthly fixed cost | \$400-800 (QC hire) | \$5,000 (Flexport min) | \$5,000 (Flexport min) |

> **Note:** Per-order costs are dominated by duties (~\$140/unit at current rates). The logistics handling difference between phases is only \$3-5/order. The primary reason to advance through phases is customer experience (faster delivery, returns) and operational scalability — not cost savings.

---

## 5 Key Differentiators to Keep in Mind

- **Delivery speed** — 2-5 days vs 7-15 days. At \$650 retail, slow shipping kills conversion.
- **Quality control** — Someone inspects before the customer opens the box, or nobody does. One bad unit = one devastating review.
- **Upfront capital** — \$0 vs ~\$100K+. Determines which options are even available to you.
- **US returns** — At \$650, "refund and keep" is too expensive and "ship back to China" is a non-starter. You need a US return address.
- **Operational complexity** — Every hour spent coordinating logistics partners is an hour not spent reducing COGS, which is the existential problem.

---

## Integrated FF + US 3PL Providers (Flexport Alternatives)

These companies offer both freight forwarding from China AND US-based warehousing/fulfillment under one roof. Get quotes from all of them.

| Provider | What they do | Monthly minimum | Shopify integration | Notes |
|----------|-------------|-----------------|--------------------|----|
| **Flexport** | FF + customs + own US warehouses + pick/pack/ship | \$5,000/mo fulfillment spend | Yes (+ Amazon, Walmart, SHEIN) | Gold standard for integrated logistics. Best tech/dashboard. Premium pricing. |
| **ShipBob + FreightBob** | US 3PL (60+ warehouses) + freight via Flexport/Maersk partners | ~\$275/mo + volume (no strict order min) | Yes | Best US fulfillment network. FreightBob handles inbound freight from China (min 1 CBM). Freight is partnered, not native — two systems stitched together. |
| **Floship** | FF + US warehouses (CA, TN, IN, NJ) + fulfillment | Custom — request quote | Yes | Purpose-built for Asia-origin DTC brands. Opaque pricing but potentially more flexible on minimums. Worth a quote. |
| **DIDADI Logistics** | China-based FF + US fulfillment | Custom — request quote | Yes | Less established, less tech maturity. Could be competitive on price for smaller brands. |

**When requesting quotes, provide:** 0.2kg product, lithium battery (Class 9 DG), 200-1,000 units/mo, Shenzhen origin, US destination, Shopify integration required.
