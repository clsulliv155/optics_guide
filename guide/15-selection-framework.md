# 15. Selection framework

Choose an optic by answering four questions in order: what lanes the host drives, what distance and fiber you have, whether the port must break out, and what power and cost you can afford. The first two usually leave only two or three candidates.

## Step 1: the host fixes the form factor and lane rate

The switch or NIC port decides the form factor (QSFP-DD vs OSFP), the host lane rate (50G, 100G or 200G) and the supported power class. Everything later must fit inside that.

## Step 2: reach and fiber narrow the PMD

| Reach | Existing fiber | 100G-lane choice (400G/800G) | 200G-lane choice (800G/1.6T) |
| --- | --- | --- | --- |
| ≤ 3 m, in rack | — | DAC; AEC if longer | DAC to \~1 m; AEC beyond |
| ≤ 30 m | — | AOC or SR | AOC or DR |
| ≤ 100 m | Multimode trunk | SR4 / SR8 / SR4.2 BiDi | Single-mode DR (multimode options thin out) |
| ≤ 500 m | Single-mode parallel (MPO) | DR4 / DR8 | DR4 / DR8 |
| ≤ 2 km | Single-mode duplex | FR4, 2×FR4 | FR4, DR-2 variants |
| ≤ 10 km | Single-mode duplex | LR4 (LR4-6 to 6 km) | LR4; coherent LR1 |
| 10–40 km | Single-mode duplex | ER-class grey or coherent | Coherent ER1-20 / ER1 |
| 40–120 km | DWDM, amplified | 400ZR | 800ZR / 1600ZR |
| ROADM or > 120 km | Shared line system | High-power ZR+ / OpenZR+ | High-power ZR+ |

## Step 3: breakout and topology

- Need to split a port into lower-speed links? Choose parallel optics (DR4, DR8) and confirm the lane-matching rule.
- Running a new plant? Single-mode MPO trunks keep every future option open.
- Fiber scarce or leased? Favor WDM duplex or DWDM.

## Step 4: power, cost and operability

| Priority | Leans toward |
| --- | --- |
| Lowest power per bit | LPO or LRO where host and reach allow; CPO at system level |
| Plug-and-play interoperability | Fully retimed, standards-based PMDs |
| Best diagnostics | Retimed modules with full CMIS VDM; coherent for long links |
| Lowest capex in rack | DAC, then AEC |
| Longest life of fiber plant | Single-mode everywhere |

## The pre-deployment checklist

- [ ] Host supports the module type, power class and required applications in those exact ports
- [ ] Lane rate and modulation match at both ends, including breakout partners
- [ ] FEC mode agreed on both ends
- [ ] Connector type, APC vs UPC and MPO-12 vs MPO-16 match the plant
- [ ] Polarity method verified end to end
- [ ] Loss budget calculated with real connector counts, and attenuators for long-reach optics on short links
- [ ] Telemetry (DOM, VDM, FEC counters) collected and baselined at turn-up
- [ ] Spares and firmware versions tracked


---

[← 14. Link budgets made intuitive](14-link-budgets-made-intuitive.md) · [Contents](../README.md#contents) · [16. Fiber plant design →](16-fiber-plant-design.md)
