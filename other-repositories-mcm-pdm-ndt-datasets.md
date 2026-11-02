# Other repositories — Machine Condition Monitoring, Predictive Maintenance & NDT datasets

Well-known public benchmark sources beyond UCI and Zenodo. Entries below were confirmed reachable on 2026-11-02 (CWRU verified live); the others are long-standing canonical sources whose landing pages are listed as entry points. Always confirm the current download link and license on the host page.

## Rotating machinery / bearings / gears

| Dataset | Host | Signal / content | Access | Link |
|---------|------|------------------|--------|------|
| CWRU Bearing Data Center | Case Western Reserve University | Drive-end & fan-end accelerometer vibration (12k & 48k samples/s), normal + single-point defects; MATLAB files | Free, research use | https://engineering.case.edu/bearingdatacenter/download-data-file |
| IMS Bearing Dataset (run-to-failure) | NASA Prognostics Data Repository | Full lifetime vibration of bearings to failure; classic RUL/prognostics benchmark | Free (NASA PCoE) | https://www.nasa.gov/intelligent-systems-division/discovery-and-systems-health/pcoe/pcoe-data-set-repository/ |
| Milling / Turbofan (C-MAPSS) / Battery / PHM08 | NASA Prognostics Data Repository | Multiple run-to-failure and degradation sets (tool wear, engine RUL, Li-ion aging) | Free (NASA PCoE) | https://www.nasa.gov/intelligent-systems-division/discovery-and-systems-health/pcoe/pcoe-data-set-repository/ |
| MAFAULDA — Machinery Fault Database | UFRJ (SMT) | Multivariate rotating-machine signals (accelerometers, microphone, tachometer) across fault types | Free, research use | https://www02.smt.ufrj.br/~offshore/mfs/page_01.html |
| Paderborn University bearing dataset | KAt-DataCenter, Uni Paderborn | Motor current + vibration, real and artificially damaged bearings | Free, registration | https://mb.uni-paderborn.de/kat/forschung/kat-datacenter/bearing-datacenter |
| MFPT Bearing Fault Dataset | Society for Machinery Failure Prevention Technology | Baseline + outer/inner-race fault vibration at known loads | Free | https://www.mfpt.org/fault-data-sets/ |

## Structural health monitoring & NDT imaging

| Dataset | Host | Signal / content | Access | Link |
|---------|------|------------------|--------|------|
| GDXray+ (X-ray NDT) | Universidad Católica de Chile | Radiographic images: welds, castings, baggage; defect detection | Free, research use | https://domingomery.ing.puc.cl/material/gdxray/ |
| severstal / NEU surface defect (steel) | NEU / public mirrors | Hot-rolled steel strip surface defect images (6 classes) for visual inspection | Free, research use | https://www.kaggle.com/datasets/kaustubhdikshit/neu-surface-defect-database |
| KolektorSDD / SDD2 | ViCoS Lab, Univ. Ljubljana | Surface-defect images of electrical commutators for segmentation/detection | **CC BY-NC-SA** | https://www.vicos.si/resources/kolektorsdd/ |

## Process / tabular predictive maintenance

| Dataset | Host | Content | Access | Link |
|---------|------|---------|--------|------|
| Bosch CNC Machining (official mirror) | Bosch Research (GitHub) | Tri-axial acceleration from brownfield milling, normal/abnormal, 2-year collection | Open (CC BY) | https://github.com/boschresearch/CNC_Machining |
| Microsoft Azure Predictive Maintenance | Kaggle (community mirror) | Telemetry, errors, maintenance, failures for 100 machines (PdM modeling) | Free | https://www.kaggle.com/datasets/arnabbiswas1/microsoft-azure-predictive-maintenance |

### Notes
- NASA PCoE and CWRU are the most-cited rotating-machinery/prognostics benchmarks; start there for vibration and RUL work.
- Licenses vary widely: CWRU/MAFAULDA/Paderborn are research-use; KolektorSDD is non-commercial (CC BY-NC-SA). Verify before redistribution or commercial use.
- Some of these sites migrate URLs periodically (NASA PCoE reorganized onto nasa.gov; MFPT now under mfpt.org; GDXray moved to the puc.cl domain). If a link 404s, search the host for the dataset name.
