# Public 1D Signal Datasets for Machine Condition Monitoring & NDT

Curated list of publicly available datasets containing **one-dimensional signals** (vibration, acoustic, current, acoustic emission, Lamb waves, process time series) related to **machine condition monitoring (MCM)**, fault diagnosis, prognostics, and **non-destructive testing (NDT)**.

Excluded by design: image/video/point-cloud datasets (X-ray, CT, thermography, surface-defect photo collections).

All URLs were checked live in October 2026. Many datasets ask for a citation when used — the original paper is named in each entry.

---

## Overview table

| # | Dataset | Machine / component | Signals | Typical task | URL |
|---|---------|--------------------|---------|--------------|-----|
| 1 | CWRU Bearing Data Center | Motor ball bearings | Vibration (12 & 48 kHz), motor current | Fault classification | https://engineering.case.edu/bearingdatacenter |
| 2 | Paderborn (KAt) Bearing Datacenter | E-mach. drive test rig bearings | Vibration (64 kHz) + motor current | Fault classification (real vs. artificial damage) | https://mb.uni-paderborn.de/en/kat/research/bearing-datacenter/data-sets-and-download |
| 3 | MFPT Bearing Dataset | Test-rig + real-world bearings | Vibration (48–98 kHz) | Fault classification | https://figshare.com/articles/dataset/MFPT_zip/27966912 (mirror) |
| 4 | Univ. of Ottawa UORED-VAFCLS | Rolling-element bearings | Vibration + acoustic + tacho | Fault classification, acoustic vs. vibration | https://data.mendeley.com/datasets/y2px5tg92h |
| 5 | HUST Bearing | 5 ball-bearing types | Vibration (51.2 kHz) | Fault classification, incl. compound faults | https://data.mendeley.com/datasets/cbv7jyx4p9 |
| 6 | MAFAULDA (UFRJ) | Rotor kit (SpectraQuest MFS) | Vibration (6 ch) + tacho + microphone, 50 kHz | Multi-fault classification (vibration or sound) | http://www02.smt.ufrj.br/~offshore/mfs/page_01.html |
| 7 | SEU Gearbox & Bearing | Drivetrain Dynamics Simulator (planetary + parallel gearbox) | Vibration (8 ch) + torque | Gear/bearing fault classification | https://github.com/cathysiyu/Mechanical-datasets |
| 8 | IMS Bearings (NASA PCoE) | 4 double-row bearings, run-to-failure | Vibration (20 kHz), 3 test sets | Degradation monitoring, RUL | https://phm-datasets.s3.amazonaws.com/NASA/4.+Bearings.zip |
| 9 | FEMTO / PRONOSTIA (PHM 2012) | 17 bearings, run-to-failure | Vibration (25.6 kHz) | RUL / prognostics | https://phm-datasets.s3.amazonaws.com/NASA/10.+FEMTO+Bearing.zip |
| 10 | XJTU-SY Bearing Datasets | 15 bearings, run-to-failure | Vibration 2 ch (25.6 kHz) | RUL / prognostics | https://biaowang.tech/xjtu-sy-bearing-datasets/ |
| 11 | UNSW Run-to-Failure Bearings | Ball bearings, natural defects | Vibration | Degradation tracking, severity | https://data.mendeley.com/datasets/h4df4mgrfb |
| 12 | LDM-UPB Run-to-Failure | 17 bearings, time-varying speed/load | Vibration | Prognostics under variable conditions | https://zenodo.org/records/10805043 |
| 13 | DCASE 2020 Task 2 (MIMII + ToyADMOS) | Valves, pumps, fans, slide rails, toy machines | Sound (16 kHz, single channel) | Unsupervised anomalous-sound detection | https://dcase.community/challenge2020/task-unsupervised-detection-of-anomalous-sounds |
| 14 | UCI Hydraulic Condition Monitoring | Hydraulic test rig (pump, valve, cooler, accumulator) | Pressure, flow, temperature, power, vibration (raw sensor cycles) | Condition classification | https://archive.ics.uci.edu/dataset/447/condition+monitoring+of+hydraulic+systems |
| 15 | NASA Milling / PHM 2010 Challenge | CNC milling cutters | Cutting force, vibration, acoustic emission | Tool wear / RUL | https://phm-datasets.s3.amazonaws.com/NASA/3.+Milling.zip |
| 16 | NASA C-MAPSS Turbofan | Simulated jet engines | 26 sensor channels, run-to-failure | RUL / prognostics (simulated) | https://phm-datasets.s3.amazonaws.com/NASA/6.+Turbofan+Engine+Degradation+Simulation+Data+Set.zip |
| 17 | Pump Sensor Data | Water pumping station | 50+ process sensor channels | Anomaly detection | https://www.kaggle.com/datasets/nphantawee/pump-sensor-data |
| 18 | NASA CFRP Composites | Composite panels under fatigue | Lamb waves (16 PZT sensors) + strain gauges | SHM / damage growth prognosis | https://phm-datasets.s3.amazonaws.com/NASA/2.+Composites.zip |
| 19 | Aluminum Lap-Joint Fatigue (PHM 2019) | Riveted lap joints | Guided (Lamb) waves vs. crack length | NDT / crack-length prognosis | https://www.nasa.gov/intelligent-systems-division/discovery-and-systems-health/pcoe/pcoe-data-set-repository/ (entry #18; email request) |

---

## A. Bearing fault classification (vibration)

### 1. CWRU Bearing Data Center — Case Western Reserve University
The classic benchmark, used in thousands of papers. 2 hp Reliance Electric motor with faults seeded by electro-discharge machining (0.007–0.040 in diameter) at the inner raceway, rolling element (ball) and outer raceway. Records at motor loads 0–3 hp (1797–1720 rpm), accelerometers at the drive end and fan end, sampling at 12 kHz and 48 kHz; also motor vibration/current under normal baseline conditions.
- URL: https://engineering.case.edu/bearingdatacenter (data files: https://engineering.case.edu/bearingdatacenter/download-data-file)

### 2. Paderborn University (KAt) Bearing Datacenter
Distinguishes **real run-in bearing damages** from **artificial damages** — the key dataset for realistic generalization studies. Test rig with dismountable modules; 26 damaged (real + artificial, various severities) and 6 healthy bearing states, 20 operating conditions (speed, load torque, radial force). Synchronously sampled vibration (64 kHz) and motor phase current, plus speed, torque, load and temperature.
- URL: https://mb.uni-paderborn.de/en/kat/research/bearing-datacenter/data-sets-and-download
- Raw-file index: https://groups.uni-paderborn.de/kat/BearingDataCenter/ ; community Zenodo mirror: https://zenodo.org/records/15845309
- The same group also publishes a **production-related drivetrain (gearbox) dataset** from the same datacenter pages.

### 3. MFPT Bearing Dataset (Society for Machinery Failure Prevention Technology)
3 baseline (healthy) records; 3 outer-race fault records at constant load; extended sets of outer- and inner-race faults across seven load levels (25–300 lbs, 25 Hz shaft rate, up to ~97.7 kHz sampling, 6 s); plus 3 **real-world failure** recordings (wind turbine and hoist bearings). Note: the society is now an ASNT affiliate and the original mfpt.org download page is gone — use the mirrors below.
- Mirror (figshare): https://figshare.com/articles/dataset/MFPT_zip/27966912
- Mirror (Kaggle): https://www.kaggle.com/datasets/emperorpein/mfpt-fault-datasets

### 4. University of Ottawa Rolling-element Dataset (UORED-VAFCLS)
Vibration **and acoustic** fault signatures of rolling-element bearings under constant load and speed. 20 DEKA bearings: inner-race, outer-race, ball and cage faults (5 bearings per fault type), each recorded in healthy, developing-fault and faulty state (60 sets total). Channels: accelerometer, microphone, load cell, Hall-effect speed sensor.
- URL: https://data.mendeley.com/datasets/y2px5tg92h
- Companion dataset (electric motor faults, constant & variable speed, UOEMD): data paper at https://www.sciencedirect.com/science/article/pii/S235234092400115X

### 5. HUST Bearing (Hanoi University of Science and Technology)
99 raw vibration records at 51.2 kHz covering 6 defect types (inner crack, outer crack, ball crack and their two-defect combinations) on 5 bearing types at 3 working conditions — useful for compound-fault and cross-bearing-type studies. Defects created by electric spark.
- URL: https://data.mendeley.com/datasets/cbv7jyx4p9
- Data paper: https://link.springer.com/article/10.1186/s13104-023-06400-4
- (Different but similarly named: "HUSTbearing" from Huazhong, 9 health states / 11 operating conditions: https://github.com/CHAOZHAO-1/HUSTbearing-dataset)

### 6. MAFAULDA — Machinery Fault Database (UFRJ, Brazil)
1,951 multivariate time series, 50 kHz, 5 s each, recorded on a SpectraQuest Machinery Fault Simulator: tachometer, 6 accelerometers (underhang/overhang: axial, radial, tangential) and a microphone (8 columns per CSV). Classes: normal, imbalance (6–35 g), horizontal/vertical misalignment (several severities), and bearing faults (cage / outer race / ball) in two mounting positions, cross-combined with speeds and imbalance masses. ~13 GB for the full package.
- URL: http://www02.smt.ufrj.br/~offshore/mfs/page_01.html

## B. Gearboxes and multi-component drivetrains

### 7. SEU Gearbox & Bearing Dataset (Southeast University)
From the paper "Highly-Accurate Machine Fault Diagnosis Using Deep Transfer Learning". Collected on a Drivetrain Dynamics Simulator (planetary + parallel-stage gearbox) under two speed–load conditions (20-0 and 30-2). Gear data: healthy, teeth crack, root fracture, missing teeth. Bearing data: normal, ball fault, inner-race, outer-race, combination fault. 8 channels per file (motor vibration, planetary gearbox x/y/z, motor torque, parallel gearbox x/y/z).
- URL: https://github.com/cathysiyu/Mechanical-datasets

## C. Bearing degradation / run-to-failure (prognostics)

### 8. IMS Bearing Dataset (Univ. of Cincinnati, via NASA PCoE)
Three run-to-failure tests on a 4-bearing (Rexnord ZA-2115, double row) test rig at 2,000 rpm / 6,000 lb. Vibration snapshots of 20,480 samples per channel every 10 min (set 1: ~34 days, set 2: ~7 days, set 3: ~37 days); outer-race and mixed failures documented.
- Direct download: https://phm-datasets.s3.amazonaws.com/NASA/4.+Bearings.zip
- Repository page: https://www.nasa.gov/intelligent-systems-division/discovery-and-systems-health/pcoe/pcoe-data-set-repository/

### 9. FEMTO-ST PRONOSTIA (IEEE PHM 2012 Data Challenge)
17 bearings run to failure under 3 conditions (1800 rpm/4000 N, 1650 rpm/4200 N, 1500 rpm/5000 N); 25.6 kHz vibration, 0.1 s records every 10 s; no failure threshold given — designed for true RUL estimation (actual remaining life unknown at test time).
- Direct download: https://phm-datasets.s3.amazonaws.com/NASA/10.+FEMTO+Bearing.zip
- Reference: Nectoux et al., "PRONOSTIA: An Experimental Platform for Bearings Accelerated Life Test", IEEE PHM 2012.

### 10. XJTU-SY Bearing Datasets (Xi'an Jiaotong University + Sumyoung)
15 LDK UER204 bearings run to failure across 3 conditions (2100/2250/2400 rpm with 12/11/10 kN). Two accelerometers (horizontal + vertical), 25.6 kHz, 32,768-sample records (1.28 s) every minute until failure. Failure modes (inner-race wear, cage fracture, outer-race wear/fracture, combinations) documented per bearing with lifetimes.
- URL (with Google Drive / Dropbox / MEGA / Baidu mirrors): https://biaowang.tech/xjtu-sy-bearing-datasets/
- Cite: Wang, Lei, Li, Li, "A Hybrid Prognostics Approach for Estimating RUL of Rolling Element Bearings", IEEE Trans. Reliability 69(1), 2020.

### 11. UNSW Bearing Run-to-Failure Datasets
Run-to-failure experiments (2019–2020, UNSW) tracking **naturally progressing** defects for fault-severity assessment; benchmark of measurement approaches for natural degradation (Zhang, Borghesani, Randall, Peng).
- URL: https://data.mendeley.com/datasets/h4df4mgrfb

### 12. LDM-UPB Run-to-Failure Dataset (Politehnica University Bucharest)
17 run-to-failure experiments on 61806-2RS ball bearings under **time-varying load and speed** with no seeded defects — realistic degradation data for prognostics under variable operating conditions.
- URL: https://zenodo.org/records/10805043

## D. Sound-based condition monitoring (acoustic)

### 13. DCASE 2020 Task 2 — MIMII + ToyADMOS
Anomalous-sound detection benchmark for machine condition monitoring: valve, pump, fan and slide rail (MIMII, real factory machines) and toy-car, toy-conveyor (ToyADMOS). Single-channel ~10 s clips at 16 kHz, training data normal-only (unsupervised setting), test data with normal/anomaly labels; anomalies include contamination, leakage, unbalance, rail damage. Development set 8.1 GB.
- Task page & data: https://dcase.community/challenge2020/task-unsupervised-detection-of-anomalous-sounds
- Zenodo: dev https://zenodo.org/record/3678171 ; additional training https://zenodo.org/record/3727685 ; evaluation https://zenodo.org/record/3841772
- Full ToyADMOS (48 kHz, 4 mics, >180 h): https://github.com/YumaKoizumi/ToyADMOS-dataset
- Newer editions (domain-shift variants) exist for DCASE 2021–2026 under the same task name.

## E. Process and other machine signals

### 14. UCI — Condition Monitoring of Hydraulic Systems
2,205 cycles (60 s each) from a hydraulic test rig with raw, cycle-sliced sensor matrices: 6 pressures (100 Hz), motor power (100 Hz), 2 flows (10 Hz), 4 temperatures, vibration (mm/s), efficiencies. Targets: cooler condition, valve condition, internal pump leakage, accumulator pressure (with severity grades). Good for multi-sensor diagnosis beyond bearings.
- URL: https://archive.ics.uci.edu/dataset/447/condition+monitoring+of+hydraulic+systems (DOI 10.24432/C5CW21, CC BY 4.0)

### 15. NASA Milling Dataset / PHM 2010 Data Challenge
Milling-machine runs (315 cuts across 7 cases) with force, vibration and acoustic-emission channels plus periodically measured flank wear VB — the standard public dataset for tool-wear monitoring and tool RUL.
- Direct download: https://phm-datasets.s3.amazonaws.com/NASA/3.+Milling.zip
- Challenge page: https://phmsociety.org/phm_competition/2010-phm-society-conference-data-challenge/

### 16. NASA C-MAPSS Turbofan Engine Degradation (simulated)
Four subsets (FD001–FD004) of simulated run-to-failure trajectories with 26 sensor channels under mixed operating conditions and fault modes; the de-facto standard for RUL-algorithm benchmarking. Simulated — pair it with the experimental datasets above.
- Direct download: https://phm-datasets.s3.amazonaws.com/NASA/6.+Turbofan+Engine+Degradation+Simulation+Data+Set.zip
- A newer, more realistic variant ("Turbofan Engine Degradation Simulation-2", flight conditions) is entry #17 of the same NASA repository.

### 17. Pump Sensor Data (Kaggle)
~220,000 rows of 50+ sensor channels (analog + digital) from a water pumping station, including the period leading to a broken pump. Process-level time series for anomaly detection practice (not vibration spectroscopy, but genuinely 1D monitoring signals).
- URL: https://www.kaggle.com/datasets/nphantawee/pump-sensor-data

## F. NDT / SHM 1D wave signals

### 18. NASA CFRP Composites Dataset
Run-to-failure tension–tension fatigue of CFRP panels (3 layups) monitored with **Lamb-wave signals from a network of 16 piezoelectric sensors** plus triaxial strain gauges; periodic X-rays provide damage ground truth. Stanford SACL + NASA PCoE. A rare public ultrasonic/guided-wave SHM dataset.
- Direct download: https://phm-datasets.s3.amazonaws.com/NASA/2.+Composites.zip

### 19. Aluminum Lap-Joint Fatigue (PHM 2019 Data Challenge)
Fatigue experiments on riveted aluminum lap joints: ultrasonic guided (Lamb) wave actuator–receiver signals recorded over fatigue life, with optically measured crack lengths as ground truth. As of Oct 2026 the direct NASA download is temporarily offline — request access by email (christopher.a.teubert@nasa.gov) or look for the PHM Society 2019 challenge mirror.
- Listing: NASA PCoE repository, entry #18 — https://www.nasa.gov/intelligent-systems-division/discovery-and-systems-health/pcoe/pcoe-data-set-repository/

---

## Meta-resources (curated lists & mirrors)

- **NASA Prognostics Data Repository** — all PCoE datasets (bearings, FEMTO, milling, C-MAPSS, composites, ...) with direct S3 zips; mirrored at the PHM Society: https://data.phmsociety.org/nasa/
  https://www.nasa.gov/intelligent-systems-division/discovery-and-systems-health/pcoe/pcoe-data-set-repository/
- **Awesome Bearing Datasets** — curated list + Python loader library: https://github.com/VictorBauler/awesome-bearing-dataset
- **Awesome Industrial Datasets** (189 entries, filterable by modality "Time Series / Vibration / Audio"): https://github.com/jonathanwvd/awesome-industrial-datasets (HTML: https://www.indatlas.com/datasets/)
- **Rotating-machine-fault-data-set** — community list of open rotating-machine datasets (Chinese/English): https://github.com/hustcxl/Rotating-machine-fault-data-set
- **DCASE dataset list** (anomalous-sound tasks across years): https://dcase-repo.github.io/dcase_datalist/

## Practical notes

1. **Licensing / citation**: UCI and Zenodo entries are CC BY 4.0; Mendeley datasets are CC BY 4.0; NASA/PCoE and university datasets usually ask for a specific citation (given per entry). Kaggle mirrors add their own account/download flow.
2. **Seeded vs. real damage**: CWRU (EDM notches) and MFPT/SEU (seeded) are convenient but not realistic; Paderborn, UNSW, LDM-UPB, XJTU-SY, IMS and FEMTO contain real or naturally progressing damage.
3. **Speed variability**: most classification datasets are constant-speed; for variable-speed methods prefer uOttawa UOEMD, LDM-UPB, or the DCASE/MIMII data.
4. **Where to start**: CWRU or MAFAULDA for classification experiments; XJTU-SY or FEMTO for prognostics; DCASE Task 2 for sound; CFRP Composites for guided-wave NDT.
