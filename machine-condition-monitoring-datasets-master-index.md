# Master Index — Public Datasets for Machine Condition Monitoring & NDT

Single entry point for the three-part dataset series. All URLs verified live in **October 2026**. Detailed per-dataset notes, mirrors, and caveats live in the part files:

| Part | File | Scope |
|------|------|-------|
| 1 | `machine-condition-monitoring-datasets.md` | 1D signals — vibration, acoustic, current, AE, guided waves, process time series |
| 2 | `machine-condition-monitoring-2d-datasets.md` | 2D data — X-ray, optical surface images, infrared, videos |
| 3 | `machine-condition-monitoring-multimodal-datasets.md` | Multimodal — two or more sensor families per machine/inspection event |

**How to use:** scan the combined lookup table below, then use the quick-pick indexes (by modality, by machine/component, by task) to shortlist. Cross-listed datasets that appear in several parts are listed **once** here; the `Part` column tells you where the detailed notes are (1D / 2D / MM).

---

## Combined lookup table (40 unique datasets)

| # | Dataset | Part | Modality | Machine / asset | Task | License | URL |
|---|---------|------|----------|-----------------|------|---------|-----|
| 1 | CWRU Bearing Data Center | 1D | Vibration (12/48 kHz), motor data | Motor ball bearings (EDM-seeded faults) | Fault classification | Free / research | https://engineering.case.edu/bearingdatacenter |
| 2 | Paderborn (KAt) Bearing Datacenter | 1D + MM | Vibration + motor current (synchronous, 64 kHz) + torque/force/temp | Drive-test-rig bearings (real + artificial damage) | Fault classification | Research | https://mb.uni-paderborn.de/en/kat/research/bearing-datacenter/data-sets-and-download |
| 3 | MFPT Bearing Dataset | 1D | Vibration (up to 97.7 kHz) | Test-rig + real-world bearings (wind turbine, hoist) | Fault classification | Research (mirrors) | https://figshare.com/articles/dataset/MFPT_zip/27966912 |
| 4 | uOttawa UORED-VAFCLS | 1D + MM | Accelerometer + microphone + load cell + Hall sensor | Rolling-element bearings (4 fault types × 3 states) | Fault classification (vib vs. acoustic) | CC BY 4.0 | https://data.mendeley.com/datasets/y2px5tg92h |
| 5 | HUST Bearing | 1D | Vibration (51.2 kHz) | 5 ball-bearing types (incl. compound faults) | Fault classification | CC BY 4.0 | https://data.mendeley.com/datasets/cbv7jyx4p9 |
| 6 | MAFAULDA | 1D + MM | 6 accelerometers + tachometer + microphone | Rotor kit (imbalance, misalignment, bearing faults) | Multi-fault classification | Free / research | http://www02.smt.ufrj.br/~offshore/mfs/page_01.html |
| 7 | SEU Gearbox & Bearing | 1D + MM | 8-channel vibration + motor torque | Drivetrain simulator (planetary + parallel gearbox) | Gear/bearing fault classification | Free (GitHub) | https://github.com/cathysiyu/Mechanical-datasets |
| 8 | IMS Bearings (NASA PCoE) | 1D | Vibration (20 kHz, snapshots) | 4 double-row bearings, run-to-failure | Degradation monitoring / prognostics | Free (NASA) | https://phm-datasets.s3.amazonaws.com/NASA/4.+Bearings.zip |
| 9 | FEMTO / PRONOSTIA (PHM 2012) | 1D | Vibration (25.6 kHz) | 17 bearings, run-to-failure | RUL / prognostics | Free (NASA) | https://phm-datasets.s3.amazonaws.com/NASA/10.+FEMTO+Bearing.zip |
| 10 | XJTU-SY Bearing Datasets | 1D | Vibration, 2 channels (25.6 kHz) | 15 bearings, run-to-failure (failure modes documented) | RUL / prognostics | Free | https://biaowang.tech/xjtu-sy-bearing-datasets/ |
| 11 | UNSW Run-to-Failure Bearings | 1D | Vibration | Ball bearings, natural defect progression | Degradation tracking / severity | CC BY 4.0 | https://data.mendeley.com/datasets/h4df4mgrfb |
| 12 | LDM-UPB Run-to-Failure | 1D | Vibration | 17 bearings, time-varying speed/load, natural faults | Prognostics | CC BY 4.0 | https://zenodo.org/records/10805043 |
| 13 | DCASE 2020 Task 2 (MIMII + ToyADMOS) | 1D | Sound, single channel (16 kHz) | Valves, pumps, fans, slide rails, toy machines | Unsupervised anomalous-sound detection | CC BY (Zenodo) | https://dcase.community/challenge2020/task-unsupervised-detection-of-anomalous-sounds |
| 14 | UCI Hydraulic Condition Monitoring | 1D + MM | Pressure ×6 + power + flow ×2 + temperature ×4 + vibration | Hydraulic test rig (pump, valve, cooler, accumulator) | Component condition classification | CC BY 4.0 | https://archive.ics.uci.edu/dataset/447/condition+monitoring+of+hydraulic+systems |
| 15 | NASA Milling / PHM 2010 | 1D + MM | Cutting force + vibration + acoustic emission + wear labels | CNC milling cutters | Tool-wear monitoring / RUL | Research | https://phm-datasets.s3.amazonaws.com/NASA/3.+Milling.zip |
| 16 | NASA C-MAPSS Turbofan (simulated) | 1D | 26 simulated sensor channels | Jet engines, run-to-failure trajectories | RUL / prognostics (simulated) | Free (NASA) | https://phm-datasets.s3.amazonaws.com/NASA/6.+Turbofan+Engine+Degradation+Simulation+Data+Set.zip |
| 17 | Pump Sensor Data | 1D | 50+ process channels | Water pumping station | Anomaly detection | Kaggle terms | https://www.kaggle.com/datasets/nphantawee/pump-sensor-data |
| 18 | NASA CFRP Composites | 1D | Lamb waves (16 PZT) + strain gauges | Composite panels under fatigue (X-ray ground truth) | SHM / damage-growth prognosis | Free (NASA) | https://phm-datasets.s3.amazonaws.com/NASA/2.+Composites.zip |
| 19 | Aluminum Lap-Joint Fatigue (PHM 2019) | 1D | Lamb waves + measured crack lengths | Riveted aluminum lap joints | Crack-length prognosis | Email request (NASA) | NASA PCoE repository, entry #18 |
| 20 | GDXray | 2D | X-ray images + sequences | Castings, welds (+ baggage/security) | Defect detection / classification | Free / research | https://github.com/computervision-xray-testing/GDXray |
| 21 | CXR-AD | 2D | Industrial X-ray images + masks | Components (5 categories) | Anomaly detection / segmentation | Not stated | https://arxiv.org/abs/2505.03412 |
| 22 | NEU-DET (steel surfaces) | 2D | Grayscale images + boxes | Hot-rolled steel strip (6 defect classes) | Classification + detection | Research (mirror) | https://github.com/siddhartamukherjee/NEU-DET-Steel-Surface-Defect-Detection |
| 23 | Severstal Steel Defect | 2D | Images + RLE masks | Steel strip (4 defect classes) | Segmentation | Kaggle terms | https://www.kaggle.com/competitions/severstal-steel-defect-detection |
| 24 | KolektorSDD | 2D | Images + pixel masks | Commutator surfaces (production) | Defect segmentation | CC BY-NC-SA 4.0 | https://www.vicos.si/resources/kolektorsdd/ |
| 25 | KolektorSDD2 | 2D | Images + pixel masks | Plastic embeds (production) | Defect segmentation | CC BY-NC-SA 4.0 | https://www.vicos.si/resources/kolektorsdd2/ |
| 26 | Casting Product Images | 2D | Grayscale images | Submersible pump impellers | Defect classification | Not stated (Kaggle) | https://www.kaggle.com/datasets/ravirajsinh45/real-life-industrial-dataset-of-casting-product |
| 27 | DeepPCB | 2D | Template/test image pairs + boxes | Printed circuit boards (6 defect types) | Defect detection | Research only (code MIT) | https://github.com/tangsanli5201/DeepPCB |
| 28 | MVTec AD | 2D | High-res images + anomaly masks | 15 industrial object/texture classes | Unsupervised anomaly detection | CC BY-NC-SA 4.0 | https://www.mvtec.com/company/research/datasets/mvtec-ad |
| 29 | MVTec LOCO AD | 2D | High-res images + masks | Structural + logical anomalies | Anomaly detection | CC BY-NC-SA 4.0 | https://www.mvtec.com/research-teaching/datasets/mvtec-loco-ad |
| 30 | DAGM 2007 (HCI) | 2D | Texture images + masks | Simulated surface inspection (10 classes) | Weakly-supervised defect detection | Academic | https://hci.iwr.uni-heidelberg.de/content/weakly-supervised-learning-industrial-optical-inspection (official page flaky; mirrors exist) |
| 31 | InfraredSolarModules | 2D | Infrared (thermographic) images | PV modules (12 anomaly classes) | Anomaly classification | MIT | https://github.com/RaptorMaps/InfraredSolarModules |
| 32 | AeBAD-S / AeBAD-V | 2D | Blade images + videos + masks | Aero-engine blades (domain shift) | Anomaly detection | CC BY 4.0 | https://github.com/zhangzilongc/MMR |
| 33 | IndustReal | 2D | Egocentric videos + step labels | Maintenance/assembly procedures | Procedure-step recognition | Apache-2.0 | https://github.com/TimSchoonbeek/IndustReal |
| 34 | Concrete Crack Images | 2D | RGB images | Concrete structures (METU campus) | Crack classification | CC BY 4.0 | https://data.mendeley.com/datasets/5y9wdsg2zt |
| 35 | IMAD-DS | MM | Audio + 3-axis accelerometer + 3-axis gyroscope | Robotic arm + brushless motor | Anomaly detection / fault diagnosis | Check record | https://zenodo.org/records/12665499 |
| 36 | Submerged Arc Welding Open Repository | MM | Welding process data + photos + profilometry + RT/UT/PAUT + defect maps | SAW weld coupons | Process–NDT fusion | CC BY 4.0 | https://zenodo.org/records/15083865 |
| 37 | CARE to Compare (wind SCADA) | MM | SCADA (86/257/957 features) + fault/status labels | 36 wind turbines, 3 farms | Early fault / anomaly detection | CC BY-SA 4.0 | https://zenodo.org/records/15846963 |
| 38 | Aventa AV-7 Research Turbine SCADA | MM | 15 SCADA channels @ 1 Hz + metadata | 6 kW research wind turbine | Operational analysis / CM | CC BY 4.0 | https://zenodo.org/records/15700928 |
| 39 | MVTec 3D-AD | MM | RGB + 3D point cloud + pixel/point masks | 15 industrial objects | Multimodal anomaly detection | CC BY-NC-SA 4.0 | https://www.mvtec.com/research-teaching/datasets/mvtec-3d-ad |
| 40 | Eyecandies | MM | RGB (multi-lighting) + depth + surface normals | 10 conveyor object classes (synthetic) | Multimodal anomaly detection | Confirm with authors | https://eyecan-ai.github.io/eyecandies/ |

---

## Quick-pick indexes

### By modality

- **Vibration (accelerometer)** — CWRU, Paderborn, MFPT, uOttawa, HUST, MAFAULDA, SEU, IMS, FEMTO, XJTU-SY, UNSW, LDM-UPB, NASA Milling
- **Sound / acoustic** — DCASE 2020 (MIMII + ToyADMOS), MAFAULDA (microphone), uOttawa (microphone), IMAD-DS (microphone)
- **Motor current** — Paderborn
- **Acoustic emission** — NASA Milling
- **Ultrasonic / guided (Lamb) waves** — NASA CFRP Composites, Aluminum Lap-Joint Fatigue, SAW repository (PAUT)
- **Process / SCADA multi-channel** — UCI Hydraulics, Pump Sensor Data, C-MAPSS (sim), CARE to Compare, Aventa AV-7, SAW repository (process data)
- **X-ray radiography** — GDXray, CXR-AD
- **Optical surface images** — NEU-DET, Severstal, KolektorSDD, KolektorSDD2, Casting Images, DeepPCB, MVTec AD, MVTec LOCO, DAGM 2007
- **Infrared / thermal** — InfraredSolarModules
- **RGB-D / 3D** — MVTec 3D-AD, Eyecandies
- **Video** — AeBAD-V, IndustReal, GDXray (sequences)

### By machine / component

- **Rolling bearings** — CWRU, Paderborn, MFPT, uOttawa, HUST, IMS, FEMTO, XJTU-SY, UNSW, LDM-UPB (+ bearing faults in MAFAULDA)
- **Gears / gearboxes** — SEU (+ Paderborn group's drivetrain dataset)
- **Motors / electric drives** — Paderborn, MAFAULDA, uOttawa (UOEMD companion), IMAD-DS (brushless motor)
- **Cutting tools / machining** — NASA Milling (PHM 2010)
- **Pumps / valves / hydraulics** — UCI Hydraulics, Pump Sensor Data, DCASE 2020 (pump/valve/fan/slider), Casting Images (impellers)
- **Wind turbines** — CARE to Compare, Aventa AV-7, MFPT (real-world failures)
- **Welding / joints** — SAW repository, GDXray (welds), Aluminum Lap-Joint Fatigue
- **Photovoltaic / energy infrastructure** — InfraredSolarModules
- **Civil structures** — Concrete Crack Images
- **Aerospace engines / structures** — AeBAD, C-MAPSS, NASA CFRP, Lap-Joint Fatigue
- **Electronics / PCB** — DeepPCB (+ MVTec AD transistor/capsule classes)
- **Robots** — IMAD-DS, IndustReal
- **Generic objects / textures** — MVTec AD, MVTec LOCO, DAGM 2007, Eyecandies, MVTec 3D-AD

### By task

- **Fault classification (supervised, signal-based)** — CWRU, Paderborn, MFPT, uOttawa, HUST, MAFAULDA, SEU
- **Defect detection / segmentation (image-based)** — NEU-DET, Severstal, KolektorSDD, KolektorSDD2, Casting Images, DeepPCB, GDXray, CXR-AD, Concrete Crack
- **Anomaly detection (unsupervised / normal-only training)** — MVTec AD, MVTec LOCO, DAGM 2007, MVTec 3D-AD, Eyecandies, AeBAD, DCASE 2020, IMAD-DS, CARE to Compare, Pump Sensor Data
- **Degradation / RUL / prognostics** — IMS, FEMTO, XJTU-SY, UNSW, LDM-UPB, C-MAPSS, NASA Milling, NASA CFRP, Lap-Joint Fatigue
- **Process / procedure monitoring** — IndustReal, SAW repository, CARE to Compare, Aventa AV-7, UCI Hydraulics

---

## Meta-resources

| Resource | Scope | URL |
|----------|-------|-----|
| NASA Prognostics Data Repository | All PCoE datasets (bearings, FEMTO, milling, C-MAPSS, composites, ...) | https://www.nasa.gov/intelligent-systems-division/discovery-and-systems-health/pcoe/pcoe-data-set-repository/ |
| — PHM Society mirror | Mirror of the NASA repository | https://data.phmsociety.org/nasa/ |
| MVTec dataset family | AD, AD 2, LOCO, 3D-AD, ITODD, Screws, D2S | https://www.mvtec.com/research-teaching/datasets |
| Awesome Industrial Datasets | 189 entries, filterable by modality/task | https://github.com/jonathanwvd/awesome-industrial-datasets (HTML: https://www.indatlas.com/datasets/) |
| Awesome Bearing Datasets | Bearing list + Python loader library | https://github.com/VictorBauler/awesome-bearing-dataset |
| Rotating-machine-fault-data-set | Community list of open rotating-machine datasets | https://github.com/hustcxl/Rotating-machine-fault-data-set |
| ViCoS Lab resources | Kolektor datasets and surface-inspection research | https://www.vicos.si/resources/ |
| Computer Vision X-ray Testing org | GDXray + X-ray testing tools/literature | https://github.com/computervision-xray-testing |
| DCASE dataset list | Anomalous-sound datasets across challenge years | https://dcase-repo.github.io/dcase_datalist/ |
| Zenodo search | Newly published multi-sensor monitoring sets | https://zenodo.org/search?q=condition+monitoring |

## Practical notes

1. **Licensing snapshot**: Zenodo/Mendeley/UCI entries are mostly **CC BY 4.0** (CARE2C: CC BY-SA); **MVTec and Kolektor sets are CC BY-NC-SA (non-commercial)**; InfraredSolarModules is MIT; IndustReal Apache-2.0; DeepPCB data research-only; Kaggle sets under competition/dataset terms. Verify before redistribution or commercial use.
2. **Damage realism**: seeded/notched faults (CWRU, MFPT, SEU) vs. real run-in damage (Paderborn, HUST) vs. natural progression (UNSW, LDM-UPB, IMS, FEMTO, XJTU-SY, CARE2C). Choose accordingly when claiming field readiness.
3. **Speed conditions**: most classification sets are constant-speed; for variable-speed methods use LDM-UPB, uOttawa UOEMD, or sound-based (DCASE) data.
4. **URLs can drift**: the part files track known moves (Paderborn datacenter, MFPT/ASNT, GDXray domain, DAGM flakiness, NEU-DET mirrors) — consult them before reporting a dead link.
5. **Citations**: nearly every dataset names a required paper — see the per-entry citations in the part files.
