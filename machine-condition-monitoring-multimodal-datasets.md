# Public Multimodal Datasets for Machine Condition Monitoring & NDT

Third part of the series:
- Part 1: `machine-condition-monitoring-datasets.md` (1D signals)
- Part 2: `machine-condition-monitoring-2d-datasets.md` (images/videos)
- **Part 3 (this file): multimodal datasets**

"Multimodal" here means datasets that provide **two or more heterogeneous sensor families for the same machine or inspection event** — e.g., vibration + motor current, vibration + acoustic, force + acoustic emission, process + NDT data, RGB + depth — enabling sensor-fusion and cross-modal diagnosis studies. All URLs were checked live in October 2026.

Entries marked **[cross-list]** also appear in Part 1 or Part 2; they are repeated here because their defining feature is multimodality.

---

## Overview table

| # | Dataset | Modalities combined | Machine / asset | Task | URL |
|---|---------|--------------------|-----------------|------|-----|
| 1 | Paderborn (KAt) Bearing Datacenter | Vibration + motor current (+ torque, speed, force, temperature) | Drive test-rig bearings | Fault classification | https://mb.uni-paderborn.de/en/kat/research/bearing-datacenter/data-sets-and-download |
| 2 | MAFAULDA | Vibration (6 acc.) + tachometer + microphone | Rotor kit | Multi-fault classification (vibration/audio) | http://www02.smt.ufrj.br/~offshore/mfs/page_01.html |
| 3 | uOttawa UORED-VAFCLS | Accelerometer + microphone + load cell + Hall sensor | Rolling bearings | Fault classification (vib vs. acoustic) | https://data.mendeley.com/datasets/y2px5tg92h |
| 4 | UCI Hydraulic Condition Monitoring | Pressure ×6 + motor power + flow ×2 + temperature ×4 + vibration + efficiencies | Hydraulic test rig | Component condition classification | https://archive.ics.uci.edu/dataset/447/condition+monitoring+of+hydraulic+systems |
| 5 | NASA Milling / PHM 2010 | Cutting force + vibration + acoustic emission + wear labels | CNC milling cutters | Tool-wear monitoring / RUL | https://phm-datasets.s3.amazonaws.com/NASA/3.+Milling.zip |
| 6 | SEU Gearbox & Bearing | 8-channel vibration + motor torque | Drivetrain simulator (planetary + parallel gearbox) | Gear/bearing fault classification | https://github.com/cathysiyu/Mechanical-datasets |
| 7 | IMAD-DS | Audio + 3-axis accelerometer + 3-axis gyroscope | Robotic arm + brushless motor | Anomaly detection / fault diagnosis | https://zenodo.org/records/12665499 |
| 8 | Submerged Arc Welding Open Repository | Process data + bead photos + profilometry + RT/UT/PAUT NDT + defect maps | SAW weld coupons | Weld-quality / process-NDT fusion | https://zenodo.org/records/15083865 |
| 9 | CARE to Compare (wind SCADA) | Multi-channel SCADA (up to 957 features) + fault labels | 36 wind turbines, 3 farms | Early fault / anomaly detection | https://zenodo.org/records/15846963 |
| 10 | Aventa AV-7 Research Turbine SCADA | 15 SCADA channels @ 1 Hz + status metadata | 6 kW research wind turbine | Operational analysis / CM | https://zenodo.org/records/15700928 |
| 11 | MVTec 3D-AD | RGB image + 3D point cloud + pixel/point masks | 15 industrial objects | Multimodal anomaly detection | https://www.mvtec.com/research-teaching/datasets/mvtec-3d-ad |
| 12 | Eyecandies | RGB (multi-lighting) + depth + surface normals | 10 conveyor-belt object classes | Multimodal anomaly detection | https://eyecan-ai.github.io/eyecandies/ |

---

## A. Synchronized multi-sensor machine testbeds

### 1. Paderborn (KAt) Bearing Datacenter [cross-list]
The reference dataset for **vibration + motor-current fusion**: both measured synchronously at 64 kHz for 26 damaged and 6 healthy bearings under 20 operating conditions, plus supporting speed, load-torque, radial-force and temperature channels. Real run-in and artificial damages. The same group's datacenter also offers a **production-related drivetrain (gearbox) dataset** with gear damages.
- URL: https://mb.uni-paderborn.de/en/kat/research/bearing-datacenter/data-sets-and-download

### 2. MAFAULDA [cross-list]
1,951 five-second records at 50 kHz with **simultaneous tachometer, six accelerometers (under-/overhang, axial/radial/tangential) and a microphone** — the classic public dataset for vibration-vs-audio fusion on imbalance, misalignment and bearing faults.
- URL: http://www02.smt.ufrj.br/~offshore/mfs/page_01.html

### 3. uOttawa UORED-VAFCLS [cross-list]
Per record: **accelerometer + microphone + load cell + Hall-effect speed sensor** for 20 bearings (inner/outer/ball/cage faults) in healthy, developing-fault and faulty states — supports acoustic-vs-vibration and load-conditioned fusion studies.
- URL: https://data.mendeley.com/datasets/y2px5tg92h
- Companion electric-motor set (UOEMD, vibration + acoustic + temperature, constant & variable speed): data paper https://www.sciencedirect.com/science/article/pii/S235234092400115X

### 4. UCI Hydraulic Condition Monitoring [cross-list]
2,205 sixty-second cycles with **raw process sensors across modalities**: 6 pressures + motor power (100 Hz), 2 flows (10 Hz), 4 temperatures + vibration + virtual efficiency channels (1 Hz); targets quantify cooler, valve, pump-leakage and accumulator condition.
- URL: https://archive.ics.uci.edu/dataset/447/condition+monitoring+of+hydraulic+systems (CC BY 4.0)

### 5. NASA Milling / PHM 2010 [cross-list]
Each of 315 milling cuts carries **three physical modalities** — dynamometer cutting force, vibration and acoustic emission — plus periodic flank-wear (VB) ground truth for tool-condition and RUL work.
- Direct download: https://phm-datasets.s3.amazonaws.com/NASA/3.+Milling.zip
- Challenge page: https://phmsociety.org/phm_competition/2010-phm-society-conference-data-challenge/

### 6. SEU Gearbox & Bearing Dataset [cross-list]
Eight synchronized channels per record on a Drivetrain Dynamics Simulator: **motor vibration, planetary-gearbox vibration (x/y/z), motor torque, parallel-gearbox vibration (x/y/z)**; gear faults (crack, root fracture, missing teeth) and bearing faults under two speed-load conditions.
- URL: https://github.com/cathysiyu/Mechanical-datasets

## B. Audio + inertial fusion (robotics & drives)

### 7. IMAD-DS
Multi-sensor industrial anomaly dataset (2024) from a **robotic arm and a brushless motor**, each equipped with an **analog microphone, a 3-axis accelerometer and a 3-axis gyroscope**; labels include sample, fault-type and event/time labels; designed for domain-shift anomaly detection and cross-sensor fusion.
- URL: https://zenodo.org/records/12665499

## C. Process data + NDT fusion

### 8. Submerged Arc Welding (SAW) Open Repository — AIMEN / PENELOPE project
Full manufacturing-to-inspection chain per weld coupon: **welding process data (HDF5)**, bead **photographs**, 3D **profilometer** scans, design/parameter PDFs, and **NDT results — radiographic (RT) and ultrasonic (UT) reports, phased-array UT data (.nde), defect-location spreadsheets**. A rare public pairing of process signals with NDT ground truth (12.7 GB).
- URL: https://zenodo.org/records/15083865 (CC BY 4.0)

### 9. CARE to Compare — Wind Turbine SCADA for Early Fault Detection (Fraunhofer IEE)
95 datasets covering **89 turbine-years across 36 turbines** in three wind farms, with **86 / 257 / 957 SCADA features** per farm; 45 datasets contain a **labeled anomaly event leading to a documented turbine fault**, the other 50 are normal-behavior series; turbine-status point labels included. Published with the CARE-score benchmark paper (Data 9(12):138, 2024). 5.5 GB. Known Min/Max/Std quality issues are documented — use the Avg channels.
- URL: https://zenodo.org/records/15846963 (CC BY-SA 4.0)
- Paper: https://doi.org/10.3390/data9120138

### 10. Aventa AV-7 (6 kW) Research Wind Turbine SCADA — IET/OST
1.5 years of **15 SCADA channels at 1 Hz** (rotor/generator speeds, stator temperature, wind speed, converter power, pitch angle, nacelle wind direction, supply voltage, turbine status) from an instrumented open research turbine, with structured JSON/CSV metadata; intended for operational and condition-monitoring analysis.
- URL: https://zenodo.org/records/15700928 (CC BY 4.0)

## D. Multimodal imaging (RGB + depth/3D)

### 11. MVTec 3D-AD
Multimodal industrial anomaly benchmark: for each of 15 object categories every scene contains an **RGB image together with an organized 3D point cloud**, plus **pixel-precise and point-level anomaly annotations** — the standard benchmark for fusing appearance and geometry.
- URL: https://www.mvtec.com/research-teaching/datasets/mvtec-3d-ad (CC BY-NC-SA 4.0)

### 12. Eyecandies
Synthetic multimodal anomaly-detection benchmark (ACCV 2022) simulating conveyor inspection: 10 object classes, each sample with **RGB under multiple lighting conditions + 16-bit depth map + surface-normal map**, pixel-wise anomaly masks, normal-only training protocol; public/private test split.
- Project page & data: https://eyecan-ai.github.io/eyecandies/ (code: https://github.com/eyecan-ai/eyecandies)

---

## Meta-resources

- **Awesome Industrial Datasets** — filter by Modality = "Multimodal" to find more (e.g., 3D-ADAM for additive manufacturing with RGB-D + point cloud): https://github.com/jonathanwvd/awesome-industrial-datasets (HTML: https://www.indatlas.com/datasets/)
- **Zenodo search** — good source for newly published multi-sensor monitoring sets: https://zenodo.org/search?q=condition+monitoring+multimodal
- **NASA Prognostics Data Repository** — several multi-sensor sets (milling: force + vib + AE): https://www.nasa.gov/intelligent-systems-division/discovery-and-systems-health/pcoe/pcoe-data-set-repository/

## Practical notes

1. **Synchronization**: Paderborn (vib + current), MAFAULDA and uOttawa record modalities synchronously — ideal for fusion. UCI hydraulics is cycle-sliced, CARE2C SCADA is windowed/averaged process data — treat as late-fusion problems.
2. **Fusion level**: same-physics pairs (vibration + current, force + AE) support early fusion; heterogeneous pairs (vibration + audio, RGB + depth, process + NDT) usually need feature-level or decision-level fusion.
3. **Licensing**: Zenodo entries here are CC BY 4.0 / CC BY-SA 4.0; MVTec 3D-AD is CC BY-NC-SA (non-commercial); check Eyecandies terms before commercial use.
4. **Where to start**: Paderborn for current+vibration fusion, IMAD-DS for audio+inertial, SAW repository for process+NDT pairing, CARE to Compare for large-scale multi-channel fleet monitoring, MVTec 3D-AD for RGB+geometry.
