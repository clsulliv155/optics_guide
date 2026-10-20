# 29. Glossary

| Term | Meaning |
| --- | --- |
| ACC | Active copper cable: twinax with linear redrivers |
| ADC / DAC | Analog-to-digital / digital-to-analog converter (also: direct-attach copper cable, by context) |
| AEC | Active electrical cable: twinax with a retiming DSP in each end |
| ALS / APR | Automatic laser shutdown / automatic power reduction (ITU-T G.664): an amplified line system drops its output on loss of the return signal so that a cut fiber or open connector is eye-safe, then probes for restoration |
| AOC | Active optical cable: transceivers permanently attached to fiber |
| APC / UPC | Angled / ultra-polished physical-contact connector end faces; they do not mate |
| APD | Avalanche photodiode: a detector with internal gain |
| AppSel | CMIS application selection: which host and media interface pair a data path runs |
| ASE | Amplified spontaneous emission: the noise optical amplifiers add |
| AUI | Attachment unit interface: IEEE's name for the host-to-module electrical interface |
| Bathtub curve | Two meanings: BER plotted against the sampling point across one unit interval, where the opening at a target BER is the usable eye width; and failure rate against time (infant mortality, useful life, wear-out), the curve that burn-in and GR-468 qualification are built around |
| Baud (GBd) | Symbols per second |
| BER | Bit error ratio; pre-FEC (raw) vs post-FEC (delivered) |
| BERT | Bit error ratio tester: pattern generator plus error detector |
| BiDi | Two wavelengths in opposite directions on one fiber |
| BTO | Barium titanate: a Pockels-effect film on silicon, a 400G-per-lane modulator candidate |
| C2M / C2C | Chip-to-module / chip-to-chip electrical links |
| CD | Chromatic dispersion |
| CDB | CMIS command data block, used for firmware upgrades |
| CDC ROADM | Colorless, directionless, contentionless ROADM: any wavelength to any direction from any add/drop port, without blocking |
| CDR | Clock and data recovery |
| CEI | OIF Common Electrical I/O specifications |
| CER / FLR | Codeword error ratio (codewords FEC could not correct) / frame loss ratio; FLR 6.2 × 10⁻¹¹ is treated as equivalent to a 10⁻¹³ BER |
| CFEC / oFEC | Coherent FEC codes used by 400ZR / OpenZR+ and 800ZR |
| Class 1 / Class 1M | IEC 60825-1 laser classes: safe to view under reasonable conditions / safe to the naked eye but not through magnifying optics; hazard level 1 in single-mode fiber is about +22 dBm at 1310 nm and +10 dBm at 1550 nm under IEC 60825-2:2021 (the 2004 table gave +12 dBm at 1310 nm) |
| CMIS | Common Management Interface Specification for 400G+ modules |
| CMIS-LT | OIF CMIS out-of-band link training (2026): per-lane, per-direction tuning of host and module through the management interface, for linear modules that have no electrical link training |
| Coherent | Detection that recovers phase and polarization using a local laser |
| CPC | Co-packaged copper: twinax that plugs into a socket on or beside the ASIC package, bypassing board traces |
| CPO / NPO | Co-packaged / near-packaged optics |
| COBO | On-board optics on the main board near the chip; a precursor to NPO |
| COM | Channel operating margin: IEEE's simulated pass/fail margin for an electrical channel, in dB |
| Comb laser | A source that emits many evenly spaced wavelengths at once, for dense WDM |
| CTLE / FFE / DFE | Linear, feed-forward and decision-feedback equalizers |
| Cutoff wavelength | Wavelength above which a fiber carries a single mode; at most 1260 nm for cabled G.652, which is why the O-band starts there |
| CW-WDM MSA | Defines 8-, 16- and 32-wavelength O-band laser grids for dense-WDM optical I/O |
| CWDM / LAN-WDM / DWDM | Coarse (20 nm: CWDM4 at 1271/1291/1311/1331 nm), LAN (800 GHz: 1295.56/1300.05/1304.58/1309.14 nm) and dense (≤ 100 GHz) wavelength grids |
| DCO / ACO | Digital / analog coherent optics (DSP inside / outside the module) |
| DGD / PDL | Differential group delay (PMD at one instant) / polarization-dependent loss; the DSP tracks DGD, while PDL costs SNR |
| DML / EML | Directly modulated laser / electro-absorption modulated laser |
| DOM / DDM | Digital optical monitoring: temperature, voltage, bias, Tx and Rx power |
| EAM | Electro-absorption modulator: an electric field shifts the absorption edge (GeSi or III-V) |
| EDFA | Erbium-doped fiber amplifier (C-band; L-band variants use longer erbium fiber) |
| Edge / grating coupler | Fiber coupler at the chip's edge (lower loss, broadband) or on its surface (testable on the wafer) |
| EIC / PIC | Electronic IC (drivers, TIAs, control loops) / photonic IC (modulators, detectors, couplers) |
| ELSFP | External laser small form-factor pluggable, for CPO |
| Engineered link | A pairing outside any spec, qualified as a specific combination of hosts and modules; LPO facing a retimed module is one today |
| ER (extinction ratio) | Ratio of the highest to the lowest optical level, P3/P0 for PAM4 or P1/P0 for NRZ, in dB; IEEE minimum 3.5 dB for PAM4; a low ER wastes average power through OMA |
| ERL | Effective return loss: reflections weighted by how much they hurt after equalization |
| ESNR | Electrical SNR the coherent DSP measures after equalization; unlike OSNR it includes nonlinear, filtering and transceiver penalties |
| Fast and narrow / slow and wide | Few lanes at the highest rate with DSP and FEC, or many lanes at modest NRZ rates via WDM, parallel fibers or wide packaging |
| FAU | Fiber array unit: a V-groove fiber array bonded to a photonic chip |
| FIT / MTTF | Failures per billion device-hours / mean time to failure (10⁹ ÷ FIT hours) |
| Flexgrid | ITU-T G.694.1 DWDM grid: channel centers at 193.1 THz + n × 6.25 GHz, slot widths in 12.5 GHz steps |
| Flyover cable | Twinax routed above the board from the ASIC package to a port or engine, bypassing lossy board traces |
| FRO | Fully retimed optics: the conventional module, with a DSP on transmit and on receive |
| G.654.E | ITU-T terrestrial fiber with a large effective area (about 125 µm²) and low loss, for longer coherent spans |
| G.657 | ITU-T bend-insensitive single-mode fiber (A1, A2, B2, B3) |
| Ge photodiode | Germanium-on-silicon detector: about 1 A/W at 1310 nm, 50–70 GHz in foundry kits |
| Gearbox | Changes lane count and rate between host and media sides |
| GN model / NLI | Gaussian-noise model: treats fiber nonlinear interference (NLI) as extra Gaussian noise that grows with the cube of launch power |
| gNMI | gRPC Network Management Interface: streams OpenConfig telemetry (SAMPLE or ON\_CHANGE) |
| GR-468 | Telcordia reliability qualification for optoelectronic devices |
| Grey optics | Fixed-wavelength, non-DWDM optics |
| GSNR | Generalized SNR: amplifier noise and nonlinear noise combined into one figure that predicts coherent performance |
| Hazard level | IEC 60825-2 rating of a location in a fiber system (1, 1M, 2, 2M, 3R, 3B, 4) by the power accessible there, rather than of a product; decides labeling and whether ALS is required |
| HCF | Hollow-core fiber: light guided in an air core by antiresonant glass membranes (NANF, DNANF) |
| Heterogeneous / hybrid integration | III-V bonded onto the silicon wafer, then processed / a finished laser die attached to the chip |
| Hybrid bonding | Direct copper-to-copper bonding at micrometer pitch, used to stack an EIC on a PIC |
| IM-DD | Intensity modulation, direct detection |
| Imaging fiber | A fiber with thousands of cores that carries a picture; micro-emitter cables send hundreds of slow light channels through one |
| IPoDWDM | IP over DWDM: coherent pluggables in router or switch ports in place of transponders, driving the line system directly |
| IQ modulator | Modulates in-phase and quadrature field components |
| ITLA | Integrable tunable laser assembly |
| Kerr effects (SPM / XPM / FWM) | Intensity-dependent refractive index: self- and cross-phase modulation and four-wave mixing, the nonlinear noise the GN model sums; grows with launch power × effective length ÷ effective area |
| KGD | Known-good die: tested before assembly, so one bad part does not scrap an engine |
| KP4 / KR4 | RS(544,514) / RS(528,514) Reed-Solomon FEC; KP4 corrects up to 15 symbol errors per 5,440-bit codeword, KR4 up to 7 |
| LACC | Linear active copper cable: another name for ACC |
| Launch power | Optical power per channel entering a span: too low and amplifier noise dominates, too high and nonlinear noise does |
| LPO / LRO / RTLR | Linear pluggable optics / linear receive optics / retimed transmitter, linear receiver |
| MACsec / MKA | IEEE 802.1AE hop-by-hop Ethernet encryption / its key agreement protocol |
| MCF | Multi-core fiber: several cores in one cladding, uncoupled or coupled |
| MFD / Aeff | Mode field diameter (about 9.2 µm at 1310 nm and 10.4 µm at 1550 nm in G.652) / effective area (about 80 µm² in G.652, 110–130 µm² in terrestrial G.654.E, up to 150 µm² in submarine G.654.D); sets coupling loss and the nonlinear threshold |
| MicroLED | A micrometer-scale LED; arrays of them carry slow-and-wide optical links without lasers |
| MLSE | Maximum-likelihood sequence estimation |
| MMC | VSFF multi-fiber connector on a TMT ferrule: 12, 16 or 24 fibers, up to 3× MPO density |
| MMF / SMF | Multimode / single-mode fiber |
| MPI | Multipath interference from reflections |
| MPO | Multi-fiber push-on connector (12 or 16 fibers common) |
| MRM / MZM | Micro-ring modulator (resonant, one wavelength) / Mach-Zehnder modulator (interferometric, broadband) |
| MSA | Multi-source agreement |
| Noise figure (NF) | An amplifier’s SNR degradation in dB, about 4–6 dB for an EDFA; enters the OSNR rule 58 + P − L − NF − 10·log N |
| NRZ / PAM4 / PAM6 | 2-, 4- and 6-level pulse amplitude modulation |
| OCI MSA | Optical Compute Interconnect MSA: an open optical PHY for AI scale-up links, starting at 200G per direction on one fiber |
| OCS | Optical circuit switch: steers light between fibers with mirrors or liquid crystals |
| OLTS | Optical loss test set: a light source and a power meter, the tier-1 certification instrument; the OTDR is tier 2 |
| OM3 / OM4 / OM5 (EMB) | Laser-optimized 50 µm multimode grades by effective modal bandwidth at 850 nm: 2,000 / 4,700 / 4,700 MHz·km; OM5 adds 2,470 MHz·km at 953 nm for SWDM |
| OMA | Optical modulation amplitude: P1 − P0 for NRZ or P3 − P0 for PAM4, the swing the receiver sees; OMA = 2 · P avg · (ER − 1) / (ER + 1), so a low ER wastes average power |
| Open CPX MSA | Socketed optical engine for NPO and CPO: 6.4T and 7.2T sockets at 200G per lane (specification published September 2026), with a roadmap to 12.8T and 448G lanes |
| OpenConfig | Vendor-neutral YANG models for configuration and telemetry |
| Optical I/O | Optical engines inside an accelerator package for scale-up links, often ring-based dense WDM |
| ORL / return loss | Optical return loss: total power reflected back toward the transmitter; APC connectors give 60 dB and more, UPC about 50 dB; poor ORL destabilizes lasers and causes MPI |
| OS2 / G.652.D | Low-water-peak single-mode fiber, the default data-center and campus fiber, usable from the O-band to the L-band |
| OSNR | Optical signal-to-noise ratio |
| OTDR | Optical time-domain reflectometer: maps loss and reflections along a fiber |
| OTN / OTUCn / FlexO | ITU-T G.709 optical transport framing (OTU4 = 100G, OTUCn = n × 100G) and its flexible, pluggable-friendly variant FlexO; the framing inside 400ZR and ZR+ |
| P2MP coherent | Point-to-multipoint coherent: one hub split into routable digital subcarriers |
| PCS | Probabilistic constellation shaping (also: physical coding sublayer, by context) |
| PDK | Process design kit: a foundry's characterized device library and design rules |
| PID (Cisco) | Product ID, the orderable part number: form factor, speed, PMD and suffix for grey optics (QDD-400G-DR4-S); checked per platform in Cisco's TMG compatibility matrix |
| PM fiber | Polarization-maintaining fiber: carries external laser light to polarization-sensitive silicon modulators |
| PMD | Physical medium dependent sublayer, the optical spec (e.g. DR4); also polarization mode dispersion |
| PMD coefficient | Growth of polarization mode dispersion with length, in ps/√km (0.2 link design value for G.652.D, 0.1 or better in modern cable); DGD is its value at one instant |
| Pockels effect | Linear electro-optic effect: absent in silicon, present in lithium niobate and BTO |
| PRBS | Pseudo-random bit sequence, a test pattern |
| Precoding (1/(1+D)) | PAM4 coding option that turns a typical DFE error burst into two errored symbols, at the cost of doubling each random error |
| PTP / SyncE | IEEE 1588 time synchronization / synchronous Ethernet frequency distribution |
| Q-factor | Pre-FEC BER expressed in dB, Q = 20·log₁₀(√2·erfc⁻¹(2·BER)); operators track Q margin above the FEC threshold |
| QAM / QPSK | Quadrature amplitude modulation / quadrature phase-shift keying |
| QKD | Quantum key distribution: keys sent with single photons so eavesdropping is detectable |
| Quantum limit | Fewest photons per bit at which an ideal detector reaches a target BER, about 10 per bit at 10⁻⁹ for on-off keying; real IM-DD receivers sit 25–35 dB above it |
| Raman amplification | Gain created in the transmission fiber itself by a strong pump about 13 THz above the signal; lowers the span's effective noise figure |
| Redriver | A linear amplifier and equalizer that boosts a signal without recovering its clock |
| Responsivity | Photodiode current per watt of light (A/W): about 0.8–1.0 for InGaAs and germanium at 1310–1550 nm, 0.5 for GaAs at 850 nm; the theoretical maximum is 1.06 A/W at 1310 nm |
| Retimer | Recovers and re-launches lanes at the same rate |
| RF over waveguide | A cable that carries a millimeter-wave or terahertz radio carrier through plastic (dielectric) cores instead of light or baseband copper |
| RIN | Relative intensity noise: a laser’s power fluctuation per hertz of bandwidth, in dB/Hz; it scales with signal power, so it sets an error floor that more receive power cannot fix |
| RJ / DJ / TJ | Random, deterministic and total jitter; TJ at a target BER is what the timing bathtub measures |
| ROADM / WSS | Reconfigurable optical add-drop multiplexer / wavelength-selective switch |
| SBS / SRS | Stimulated Brillouin scattering (reflects a narrow-linewidth launch above roughly +5 to +10 dBm on a long span; raised by dithering the laser) / stimulated Raman scattering (moves power toward longer wavelengths, tilting the band) |
| SDM | Space-division multiplexing: more cores or modes rather than more wavelengths |
| SECQ | Stressed eye closure quaternary: the eye closure of the deliberately impaired signal used in a stressed receiver sensitivity test, set equal to the TDECQ limit |
| Sensitivity | Lowest OMA (or average power) at which a receiver meets the target BER; stressed sensitivity is measured with a worst-case transmitter signal |
| SER | Symbol error ratio; with Gray-coded PAM4, BER is about half the SER |
| SerDes | Serializer/deserializer: high-speed I/O on an ASIC |
| Shoreline density | Bandwidth per millimeter of chip edge (Tb/s/mm); also called beachfront density |
| Shot noise / thermal noise | Noise from the photon arrival statistics (grows as √P) / from the TIA’s resistance (independent of P); PIN receivers are thermal-limited, APD and coherent receivers approach the shot limit |
| SLTE | Submarine line terminal equipment: the transponders and line gear at each cable landing station |
| SMSR | Side-mode suppression ratio: how single-wavelength a DFB or EML is, at least 30 dB; poor SMSR shows up as dispersion penalty and MPI |
| SN-MT | 8-, 16- or 32-fiber MT-style ferrule in the SN duplex footprint; roughly 2.7–3× MPO-16 density depending on panel layout |
| SOA | Semiconductor optical amplifier: compact and O-band capable; a receiver preamplifier in ER4 and ER8 optics and a booster in some ZR modules; its gain is pattern-dependent |
| SOI | Silicon-on-insulator: the silicon photonics wafer, typically 220 nm of silicon on buried oxide |
| SRMO | Short-Reach Micro-Emitter Optics: an OCP workstream, started October 2026, to standardize micro-emitter (microLED) links |
| SSPRQ / PRBS31Q | PAM4 test patterns for transmitter (TDECQ) and BER testing |
| Super C / Super L | Extended C and L bands of about 6 THz each; together they roughly double the spectrum per fiber |
| TDECQ | Transmitter and dispersion eye closure quaternary: PAM4 transmitter quality |
| TDP | Transmitter and dispersion penalty: the NRZ-era sensitivity penalty of a real transmitter over the target fiber; TDECQ is its PAM4 successor |
| TEC | Thermoelectric cooler: holds a LAN-WDM or DWDM laser within about ±1 nm; why LR4 and coherent modules draw more power than CWDM4 |
| TFLN | Thin-film lithium niobate modulators |
| Thermo-optic tuning | Heaters that shift a waveguide's index slowly, to bias MZMs, lock rings and trim filters |
| TIA | Transimpedance amplifier after the photodiode |
| TOSA / ROSA / BOSA | Transmit / receive / bidirectional optical sub-assembly: the packaged laser with its driver, or photodiode with its TIA, inside a module |
| TP (test points) | IEEE compliance points: TP1a (host output at the connector), TP2 (optical output), TP3 (optical input), TP4 (module electrical output), TP4a (host input); each a contract boundary between host and module |
| Transponder / muxponder | Line-system cards that map one / several client signals onto a coherent wavelength; what IPoDWDM removes |
| TRO | Transmit-retimed optics: another name for LRO, with a DSP on transmit only |
| Twinax | Shielded twin-axial copper pairs: the medium inside DAC, ACC and AEC cables |
| UCIe | Universal Chiplet Interconnect Express: the die-to-die interface optical I/O chiplets use |
| UI | Unit interval: one symbol period, 18.8 ps at 53.125 GBd and 9.4 ps at 106.25 GBd; jitter and eye width are quoted in UI |
| VCSEL | Vertical-cavity surface-emitting laser (850 nm for SR, 880–940 nm for SWDM, 1060 nm for some slow-and-wide links; multimode) |
| VDM | CMIS versatile diagnostics monitoring: per-lane SNR, BER and more |
| VOA | Variable optical attenuator; fixed attenuators pad ER and ZR optics on short links, VOAs level power in line systems |
| VSFF | Very-small-form-factor connectors (SN, MDC, CS) |
| Water peak | Hydroxyl absorption near 1383 nm that split the historical windows; suppressed in G.652.D, which opened the E-band |
| XPN | 64-bit MACsec packet numbering (802.1AEbw) so the counter does not wrap within minutes at 40G and above; needs the GCM-AES-XPN cipher suites |
| XPO | eXtra-dense Pluggable Optics: a liquid-cooled 64 × 200G (12.8T) pluggable MSA announced in 2026 |
| XSR / XSR+ | OIF extra-short-reach electrical classes used for CPO and NPO links |
| Zero-dispersion wavelength (λ₀) / slope (S₀) | Where chromatic dispersion crosses zero (1300–1324 nm for G.652) and how fast it grows away from there (at most 0.092 ps/(nm²·km)); D(λ) = S₀/4 · (λ − λ₀⁴/λ³) |
| ZR / ZR+ / OpenZR+ / Bright ZR+ | 400G coherent pluggable classes: OIF 400ZR (16QAM, CFEC, about 120 km amplified), OpenZR+ (oFEC, multi-rate, metro reach) and high-output Bright variants for ROADM networks |


---

[← 28. Roadmap as of October 2026](28-roadmap-as-of-october-2026.md) · [Contents](../README.md#contents) · [30. Mastery checks →](30-mastery-checks.md)
