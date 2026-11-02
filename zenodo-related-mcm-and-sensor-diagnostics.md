# Zenodo — Machine Condition Monitoring, Predictive Maintenance & NDT datasets

Verified live via the Zenodo REST API (`https://zenodo.org/api/records/<id>`) on 2026-11-02. Every row is an **open** `dataset`-type record (except where noted). Click the landing page to download files. Licenses are flagged per row — most are **CC BY 4.0**; three exceptions noted.

## Rotating machinery — bearings & motors

| Record | Dataset | Signal / content | License | Files / ~size | Landing |
|--------|---------|------------------|---------|---------------|---------|
| 22109737 | Taper roller bearing dataset @ 12800 Hz | Vibration from a bearing test rig; healthy, roller, inner-wedge, wear and cage faults across speeds | CC BY 4.0 | 40 / ~295 MB | https://zenodo.org/records/22109737 |
| 22705165 | SpectraQuest dataset @ 12.8 kHz (REB fault diagnosis) | Dual-housing rig, deep-groove ball bearings; ball/outer/inner/combined faults; triaxial accelerometer | CC BY 4.0 | 20 / ~106 MB | https://zenodo.org/records/22705165 |
| 15743425 | NOVIC+ Motor compound fault dataset (part 1; parts 2 & 3 linked) | Motor compound-fault vibration/temperature; domain-adaptation, partially labeled | CC BY 4.0 | 18 / ~28 GB | https://zenodo.org/records/15743425 |
| 8203070 | Squirrel-Cage Induction Motor Fault Diagnosis Dataset | Thermal images + multi-sensor; non-invasive fault diagnosis / PdM | **CC BY-NC-ND 4.0** | 2 / ~1.78 GB | https://zenodo.org/records/8203070 |
| 17048028 | Induction motor fault detection — startup currents | Startup currents of 4 motors (healthy + broken bar/ring); raw .dat + CSV + scripts | CC BY 4.0 | 1 / ~11 MB | https://zenodo.org/records/17048028 |
| 18907022 | Early detection of rotor core breakage via phase-current harmonics (MCSA) | Motor Current Signature Analysis of stator phase-current spectra, low-power async motors | CC BY 4.0 | 1 / ~1.6 MB | https://zenodo.org/records/18907022 |
| 23367145 | PMSM Drive Fault Dataset Under Constant Speed Operation | Simulink PMSM-drive time-domain signals; healthy + 9 fault classes (3 types × 3 phases) | CC BY 4.0 | 2 / ~17 MB | https://zenodo.org/records/23367145 |
| 23686441 | Large-to-Small Transfer Learning for Early Bearing Fault Diagnosis | Bearing fault data supporting transfer-learning benchmark | CC BY 4.0 | — | https://zenodo.org/records/23686441 |

## Tooling, machining & gearboxes

| Record | Dataset | Signal / content | License | Files / ~size | Landing |
|--------|---------|------------------|---------|---------------|---------|
| 21845441 | End-mill wear monitoring on a desktop CNC @ 64 kHz | Vibration from 3 carbide end mills on 6061 Al; two ADXL1002 MEMS at 64 kHz; raw + features + code | CC BY 4.0 | 7 / ~2.4 GB | https://zenodo.org/records/21845441 |
| 8238653 | Mudestreda Multimodal Device State Recognition | Milling machine time series + images; classification, regression, anomaly, RUL, flank wear | **GPL-3.0-or-later** | 8 / ~2.8 GB | https://zenodo.org/records/8238653 |
| 4975259 | Non-contact incipient fault diagnosis of fixed-axis gearbox (CEEMDAN) | Sound signals of simulated local gear defects; features for severity (Dryad DOI 10.5061/dryad.s4g56) | **CC0** | 1 / ~11 MB | https://zenodo.org/records/4975259 |

## Wind turbines & drivetrains

| Record | Dataset | Signal / content | License | Files / ~size | Landing |
|--------|---------|------------------|---------|---------------|---------|
| 11820598 | Wind turbine condition monitoring dataset (Fraunhofer LBF) | 750 W turbine; accelerometers, tachometer, temperatures, wind; imbalance/aero/bearing damage | CC BY 4.0 | 9 / ~18.7 GB | https://zenodo.org/records/11820598 |
| 7674842 | Bearings damage dataset — 5 MW drivetrain on spar floating turbine | Simulated accelerations, 1-hour runs @ 200 Hz | CC BY 4.0 | 4 / ~504 MB | https://zenodo.org/records/7674842 |
| 10644756 | Bearing damage — 5 MW drivetrain on spar/TLP/land-based | Simulated accelerations; healthy + 2 damage states, 6 environmental conditions | CC BY 4.0 | 2 / ~1.81 GB | https://zenodo.org/records/10644756 |
| 18718184 | Wind turbine fault diagnosis dataset (FAST – NREL 5MW) | 6 fault scenarios + healthy, generated from NREL 5-MW benchmark in FAST | CC BY 4.0 | 1 / ~88 MB | https://zenodo.org/records/18718184 |

## Non-contact / vision-based vibration & non-destructive testing

| Record | Dataset | Signal / content | License | Files / ~size | Landing |
|--------|---------|------------------|---------|---------------|---------|
| 17447083 | XJTU-DV — Dynamic Vision Dataset for non-contact vibration & fault diagnosis | Event-camera / dynamic-vision Beam, Rotor, Pump sub-sets with laser-vibrometer ground truth | CC BY 4.0 | 4 / ~21 GB | https://zenodo.org/records/17447083 |
| 21203159 | Offboard laser Doppler vibrometry — UAV propeller fault diagnosis | Labeled time-domain vibration (Polytec VibroGo LDV) of healthy/faulty propellers | CC BY 4.0 | 2 / ~3.4 MB | https://zenodo.org/records/21203159 |
| 10875042 | Acoustic Emission dataset for impact localization | Simulated ray-tracing AE + experimental impact tests on aluminum plates @ 2 MHz | CC BY 4.0 | 10 / ~64 MB | https://zenodo.org/records/10875042 |

## Hydraulics, power electronics & process systems

| Record | Dataset | Signal / content | License | Files / ~size | Landing |
|--------|---------|------------------|---------|---------------|---------|
| 23831475 | Design-time sensor configuration for single-sensor loss in hydraulic fault diagnosis | Derived data + code over UCI Hydraulic Systems (2,205 cycles, 14 sensors, 4 tasks) | CC BY 4.0 | 1 / ~4 MB | https://zenodo.org/records/23831475 |
| 23719729 | Open DC-DC converter fault-diagnosis benchmark with component-batch shift | Simulated buck/boost/interleaved-boost; 5 fault classes × 3 severities; code + protocol | CC BY 4.0 | 9 / ~8 GB | https://zenodo.org/records/23719729 |
| 22872511 | Explainable fault diagnosis of single-phase bridge rectifiers | Simulink models + XAI scripts; observability-limited fault taxonomy | CC BY 4.0 | 31 / ~1.6 MB | https://zenodo.org/records/22872511 |

### Notes
- Access is **open** for all rows; three non-CC-BY licenses are flagged (8203070 = CC BY-NC-ND, 8238653 = GPL-3.0, 4975259 = CC0). Re-check the license on each landing page before redistribution or commercial use.
- Programmatic listing: `GET https://zenodo.org/api/records?q=<keywords>&type=dataset&size=20&sort=bestmatch` (browser/`webfetch` works; direct server-side calls may be rate-limited with HTTP 403). Useful keywords: `bearing fault vibration`, `milling tool wear`, `gearbox fault`, `acoustic emission`, `motor current fault`, `predictive maintenance`, `ultrasonic testing weld`.
