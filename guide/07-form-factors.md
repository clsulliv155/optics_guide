# 7. Form factors

A form factor fixes the electrical lane count, the mechanics and the power and thermal envelope, not the optics inside. The same QSFP112 cage can hold a 100 m SR4, a 2 km FR4, a copper DAC or a coherent module. Read every form-factor name as "lanes × lane rate".

## The lanes × rate table

| Form factor | Electrical lanes | Lane rate | Port speed | Notes |
| --- | --- | --- | --- | --- |
| SFP+ | 1 | 10G NRZ | 10G |  |
| SFP28 | 1 | 25G NRZ | 25G |  |
| SFP56 | 1 | 50G PAM4 | 50G |  |
| SFP112 | 1 | 100G PAM4 | 100G |  |
| SFP-DD | 2 | 50G PAM4 | 100G | Double-density SFP |
| QSFP+ | 4 | 10G NRZ | 40G |  |
| QSFP28 | 4 | 25G NRZ | 100G | The workhorse of the 100G era |
| QSFP56 | 4 | 50G PAM4 | 200G |  |
| QSFP112 | 4 | 100G PAM4 | 400G |  |
| QSFP-DD | 8 | 25G / 50G | 200G / 400G | Second row of contacts; accepts QSFP modules |
| QSFP-DD800 | 8 | 100G PAM4 | 800G |  |
| QSFP-DD1600 | 8 | 200G PAM4 | 1.6T |  |
| OSFP | 8 | 50G / 100G / 200G | 400G / 800G / 1.6T | Integrated heat sink; 200G-lane version called OSFP1600 |
| OSFP-RHS | 8 (4 on 400G NICs) | 100G PAM4 | 400G | Flat top cooled by the host's riding heat sink; NIC-side form factor, shipping at 800G (4 × 200G DR4) as well as 400G |
| OSFP-XD | 16 | 100G PAM4 (200G as a future option) | 1.6T (3.2T) | 16 lanes at 100G for 1.6T (200G per lane is a future option), up to 40 W; specified in 2022, no products, overtaken by XPO |
| USFP | 16 (connector scales to 32) | 400G PAM4 (planned) | 6.4T (12.8T) | Ultra-dense SFP, announced October 2026 as an open form factor for 400G-per-lane optics: roughly an OSFP footprint, up to 100 W without an in-module cooling loop; no sampling date |
| CFP2 | 4–8 | Various | 100G–400G+ | Larger, high power; persists for high-performance coherent |

Current MSA specifications: [QSFP-DD rev 7.1](https://www.qsfp-dd.com/specification/) covers QSFP-DD800 and QSFP-DD1600; the [OSFP MSA](https://osfpmsa.org/) covers OSFP, OSFP1600 and OSFP-XD.

## QSFP-DD vs OSFP

|  | QSFP-DD family | OSFP family |
| --- | --- | --- |
| Backward compatibility | Accepts QSFP28/56/112 modules (uses 4 of 8 lanes) | Not QSFP-compatible without an adapter |
| Heat removal | Host-side riding heat sink in the cage | Finned heat sink built into the module |
| Thermal headroom | Tighter | More, which matters at 1.6T and for coherent |
| Size | Slightly smaller | Slightly wider and taller |
| Typical home | Enterprise and service provider, where 100G/400G reuse matters | AI and hyperscale fabrics at 800G and 1.6T |

Both fit 32 ports in one rack unit; the choice is usually made by the switch, not the optic.

## Power and thermal

| Module | Typical power |
| --- | --- |
| 100G QSFP28 (SR4, CWDM4) | \~3.5–4.5 W |
| 400G QSFP-DD / QSFP112 (DR4, FR4) | \~10–12 W |
| 400ZR QSFP-DD | \~17 W typical, 20 W max |
| 800G DSP-based | \~14–18 W |
| 800G LPO | \~7–8.5 W |
| 1.6T DSP-based (DR8, 2×FR4) | \~20–26 W |

Figures above 400G are vendor-listed ([1.6T](https://www.businesswire.com/news/home/20251222728263/en), [800G LPO](https://convergedigest.com/fs-launches-800g-lpo-module/?amp=1), [400ZR datasheet](https://www.juniper.net/documentation/ke-apps/hct/optStdParams/stdHtml/QDD-400G-ZR-M.html)); the 100G and 400G grey rows are approximate.

- **Power classes.** Each MSA defines classes. The module advertises its power class and maximum power in its CMIS memory map (Page 00h bytes 200–201); the host compares that with what the port can supply and cool, and keeps the module in low-power mode if it cannot support it.
- **Ports are not equal.** High-power coherent or 1.6T modules may be supported only in ports with better airflow. Temperature alarms on one port but not its neighbor often point to airflow, not the module.

## Compatibility rules of thumb

- A larger cage usually accepts the smaller module of the same family (QSFP28 in QSFP-DD, SFP28 in SFP56), running at the smaller module's speed if the host supports it.
- The reverse never works mechanically.
- Adapters exist (QSFP-to-SFP for 10G/25G in a QSFP port; OSFP-to-QSFP), but they add a host-support question.
- "400G QSFP-DD" alone does not tell you the host lane rate: 8 × 50G and 4 × 100G hosts both exist, and some modules only support one.


---

[← 6. Grey (IM-DD) optics](06-grey-im-dd-optics.md) · [Contents](../README.md#contents) · [8. Coherent optics and DCI →](08-coherent-optics-and-dci.md)
