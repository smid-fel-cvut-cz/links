# UCI ML Repository — Machine Condition Monitoring, Predictive Maintenance & NDT datasets

Verified live via the UCI dataset API on 2026-11-02. Every row is a real dataset page on `https://archive.ics.uci.edu`. Download is offered on each dataset page (and, where noted, as a direct `data.csv`). Unless stated otherwise, UCI hosts these under **CC BY 4.0**.

> Correction note: an earlier version of this file listed guessed dataset IDs (6 "Mechanical Analysis", 102, 463, 483) that resolved to unrelated datasets. Those have been removed. The entries below were confirmed by keyword search against the UCI API.

| ID | Dataset | Domain / signal | Task | Instances | Year | DOI | Page |
|----|---------|-----------------|------|-----------|------|-----|------|
| 447 | Condition monitoring of hydraulic systems | Hydraulic test rig; multi-sensor (pressure, flow, temperature, vibration, power), 4 fault types at several severity grades | Classification, Regression | 2,205 cycles (43,680 attributes) | 2015 | 10.24432/C5CW21 | https://archive.ics.uci.edu/dataset/447/condition+monitoring+of+hydraulic+systems |
| 316 | Condition Based Maintenance of Naval Propulsion Plants | Gas-turbine (CODLAG frigate) simulator; degradation of compressor & turbine | Regression | 11,934 | 2014 | 10.24432/C5K31K | https://archive.ics.uci.edu/dataset/316/condition+based+maintenance+of+naval+propulsion+plants |
| 325 | Dataset for Sensorless Drive Diagnosis | Features from electric motor current; 11 classes of intact/defective components | Classification | 58,509 | 2013 | 10.24432/C5VP5F | https://archive.ics.uci.edu/dataset/325/dataset+for+sensorless+drive+diagnosis |
| 433 | Ultrasonic flowmeter diagnostics | Fault diagnosis of four liquid ultrasonic flowmeters (health-state classification) | Classification | 540 | 2017 | 10.24432/C5B895 | https://archive.ics.uci.edu/dataset/433/ultrasonic+flowmeter+diagnostics |
| 601 | AI4I 2020 Predictive Maintenance Dataset | Synthetic predictive-maintenance data reflecting real industrial machine failure modes | Classification, Regression, Causal-Discovery | 10,000 | 2020 | 10.24432/C5HS5C | https://archive.ics.uci.edu/dataset/601/ai4i+2020+predictive+maintenance+dataset — direct CSV: https://archive.ics.uci.edu/static/public/601/data.csv |
| 752 | Bosch CNC Machining Dataset | Real-world brownfield milling; tri-axial acceleration over a 2-year production run; normal vs. abnormal processes | Classification, Clustering | 2,700 | 2022 | mirror: https://github.com/boschresearch/CNC_Machining | https://archive.ics.uci.edu/dataset/752/bosch+cnc+machining+dataset |
| 198 | Steel Plates Faults | Surface-defect metadata of steel plates classified into 7 fault types (NDT/visual) | Classification | 1,941 | 2010 | 10.24432/C5J88N | https://archive.ics.uci.edu/dataset/198/steel+plates+faults — direct CSV: https://archive.ics.uci.edu/static/public/198/data.csv |
| 551 | Gas Turbine CO and NOx Emission Data Set | 36,733 hourly sensor aggregates from a Turkish gas turbine (emissions/process monitoring) | Regression, Clustering | 36,733 | 2019 | 10.24432/C5WC95 | https://archive.ics.uci.edu/dataset/551/gas+turbine+co+and+nox+emission+data+set — direct CSV: https://archive.ics.uci.edu/static/public/551/data.csv |
| 994 | Micro Gas Turbine Electrical Energy Prediction | Electrical power vs. control-signal time series from a 3 kW commercial micro gas turbine | Regression | 71,225 | 2024 | 10.24432/C58S4T | https://archive.ics.uci.edu/dataset/994/micro+gas+turbine+electrical+energy+prediction |

### Programmatic access (Python)
```python
pip install ucimlrepo
from ucimlrepo import fetch_ucirepo
ds = fetch_ucirepo(id=447)   # e.g. hydraulic systems
X, y = ds.data.features, ds.data.targets
```

**Most relevant "core" MCM/PdM entries:** 447 (hydraulic multi-sensor), 325 (motor current), 433 (ultrasonic flowmeter), 601 (predictive maintenance), 752 (CNC milling vibration), 316 (turbine degradation). Steel Plates Faults (198) is the closest NDT/surface-inspection entry.
