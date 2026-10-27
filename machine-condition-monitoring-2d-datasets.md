# Public 2D / Image / Video Datasets for Machine Condition Monitoring & NDT

Companion to `machine-condition-monitoring-datasets.md` (the 1D-signal list). This list covers publicly available datasets of **two-dimensional data** — optical images, X-ray radiographs, infrared thermograms, and videos — used for **machine condition monitoring (MCM)**, visual/automated **non-destructive testing (NDT)**, surface-inspection quality control, and camera-based fault detection.

All URLs were checked live in October 2026. Licenses vary — several datasets are explicitly **non-commercial** (flagged per entry).

---

## Overview table

| # | Dataset | Modality | Application | Typical task | URL |
|---|---------|----------|-------------|--------------|-----|
| 1 | GDXray | X-ray images (+ sequences) | NDT of castings & welds, security | Defect detection/classification | https://github.com/computervision-xray-testing/GDXray |
| 2 | CXR-AD | Industrial X-ray images | Component X-ray inspection | Anomaly detection + segmentation | https://arxiv.org/abs/2505.03412 |
| 3 | NEU-DET (steel surfaces) | Grayscale images | Hot-rolled steel strip defects | Classification + detection | https://github.com/siddhartamukherjee/NEU-DET-Steel-Surface-Defect-Detection (mirror) |
| 4 | Severstal Steel Defect | Images + RLE masks | Steel strip surface defects | Segmentation | https://www.kaggle.com/competitions/severstal-steel-defect-detection |
| 5 | KolektorSDD | Images + pixel masks | Commutator surfaces (production) | Defect segmentation | https://www.vicos.si/resources/kolektorsdd/ |
| 6 | KolektorSDD2 | Images + pixel masks | Plastic embeds (production) | Defect segmentation | https://www.vicos.si/resources/kolektorsdd2/ |
| 7 | Casting Product Images | Grayscale images | Submersible pump impellers | Defect classification | https://www.kaggle.com/datasets/ravirajsinh45/real-life-industrial-dataset-of-casting-product |
| 8 | DeepPCB | Binary image pairs | PCB defect inspection | Detection (6 defect types) | https://github.com/tangsanli5201/DeepPCB |
| 9 | MVTec AD | High-res images | 15 industrial object/texture classes | Unsupervised anomaly detection | https://www.mvtec.com/company/research/datasets/mvtec-ad |
| 10 | MVTec LOCO AD | High-res images | Structural + logical anomalies | Anomaly detection | https://www.mvtec.com/research-teaching/datasets/mvtec-loco-ad |
| 11 | DAGM 2007 (HCI) | Texture images | Simulated surface inspection | Weakly-supervised defect detection | https://hci.iwr.uni-heidelberg.de/content/weakly-supervised-learning-industrial-optical-inspection (see note) |
| 12 | InfraredSolarModules | Infrared images | PV module thermographic inspection | Anomaly classification (12 classes) | https://github.com/RaptorMaps/InfraredSolarModules |
| 13 | AeBAD-S / AeBAD-V | Images + videos | Aero-engine blade surfaces | Anomaly detection under domain shift | https://github.com/zhangzilongc/MMR |
| 14 | IndustReal | Egocentric videos | Maintenance/assembly procedures | Procedure-step recognition | https://github.com/TimSchoonbeek/IndustReal |
| 15 | Concrete Crack Images | RGB images | Civil structure inspection (VT) | Crack classification | https://data.mendeley.com/datasets/5y9wdsg2zt |

---

## A. Radiography / X-ray NDT

### 1. GDXray (Grayscale X-rays for X-ray Testing)
The standard public X-ray test dataset accompanying the book *Computer Vision for X-Ray Testing* (D. Mery et al.). ~20,000 X-ray images in five groups: **castings** (aluminum wheels with blow holes, cracks — the NDT core), **welds** (lack of penetration, porosity), baggage, nature and security objects; several groups are image **sequences** usable like video. Organizers' GitHub also hosts related X-ray testing code and papers.
- URL: https://github.com/computervision-xray-testing/GDXray
- Author's page: https://domingomery.ing.uc.cl/ (the old gdxray.net domain is no longer reachable)

### 2. CXR-AD (2025)
Industrial-component X-ray anomaly-detection benchmark: 653 normal and 561 anomalous X-ray images across 5 component categories, with pixel-level defect masks; normal-only training setting for NDT-style unsupervised inspection.
- Paper & data pointer: https://arxiv.org/abs/2505.03412
- Also listed at: https://www.indatlas.com/datasets/

## B. Visual surface inspection — metals, castings, PCB

### 3. NEU Surface Defect Database (NEU-DET) — Northeastern University, China
The classic hot-rolled steel-strip dataset: 6 defect classes (crazing, inclusion, patches, pitted surface, rolled-in scale, scratches), ~1,800 grayscale images (200×300) with bounding-box annotations, each class captured under multiple illumination/contrast variants. The official NEU faculty page has moved several times over the years — use community mirrors:
- Verified mirror (dataset + code): https://github.com/siddhartamukherjee/NEU-DET-Steel-Surface-Defect-Detection
- Additional mirrors: search "NEU-DET" or "NEU surface defect database" on Kaggle.

### 4. Severstal: Steel Defect Detection (Kaggle)
Competition dataset: ~12,500 training images of steel strip surfaces (1600×256) with 4 defect classes and run-length-encoded pixel masks; large unlabeled test set. Good for segmentation and scarce-defect (class imbalance) experiments.
- URL: https://www.kaggle.com/competitions/severstal-steel-defect-detection (Kaggle account required)

### 5. KolektorSDD (KSDD)
Real production images of defective electrical commutators (399 images, 52 with visible defects) with fine **pixel-level annotations**; captured in a controlled industrial environment. Landmark paper for segmentation-based surface-defect detection (Journal of Intelligent Manufacturing 2019).
- URL: https://www.vicos.si/resources/kolektorsdd/ (CC BY-NC-SA 4.0)

### 6. KolektorSDD2 (KSDD2)
Follow-up production dataset: 3,335 images (356 defective) of plastic embeds with diverse defect types (scratches, spots, surface imperfections); train/test split predefined. Used in mixed-supervision learning research (Computers in Industry 2021).
- URL: https://www.vicos.si/resources/kolektorsdd2/ (CC BY-NC-SA 4.0)

### 7. Casting Product Image Data for Quality Inspection
7,348 grayscale images (300×300) of submersible pump impellers, top view under stable lighting, split into ok_front / def_front classes (a smaller unaugmented 512×512 set included). Practical binary casting-defect classification task.
- URL: https://www.kaggle.com/datasets/ravirajsinh45/real-life-industrial-dataset-of-casting-product (Kaggle account required)

### 8. DeepPCB
1,500 template/test image pairs of printed-circuit boards (640×640 binary images from linear-scan CCD) with bounding-box annotations of 6 common PCB defect types: open, short, mousebite, spur, pin hole, spurious copper. ~7,000 defects total; standard train/test split with evaluation scripts. Data for research use only.
- URL: https://github.com/tangsanli5201/DeepPCB

## C. General industrial anomaly-detection benchmarks

### 9. MVTec AD
The de-facto benchmark for unsupervised industrial anomaly detection: 5,000+ high-resolution images across 15 object and texture categories (screws, metal nuts, transistors, capsules, leather, wood, ...), defect-free training sets, test sets with various defect types, and **pixel-precise anomaly masks**.
- URL: https://www.mvtec.com/company/research/datasets/mvtec-ad (CC BY-NC-SA 4.0 — non-commercial)
- Family page (all MVTec datasets): https://www.mvtec.com/research-teaching/datasets — includes **MVTec AD 2** (2025), **MVTec LOCO AD** (logical/structural anomalies), **MVTec 3D-AD**, **MVTec ITODD**, **MVTec Screws**.

### 10. MVTec LOCO AD
Extension of MVTec AD focusing on **logical anomalies** (missing/misplaced components, wrong counts) alongside structural ones — closer to real assembly inspection.
- URL: https://www.mvtec.com/research-teaching/datasets/mvtec-loco-ad

### 11. DAGM 2007 (HCI Industrial Optical Inspection)
Classic weakly-supervised defect-detection dataset: 10 synthetic texture classes resembling surface inspections (wood, carpet, leather...), 1,000 images per class, 6 typical defect types per class with pixel masks for defective images, global "defective/ok" labels only for training. Note: the official Heidelberg page was intermittently unreachable (HTTP 500) in Oct 2026 — the dataset is widely mirrored.
- Official page: https://hci.iwr.uni-heidelberg.de/content/weakly-supervised-learning-industrial-optical-inspection
- Verified community mirror: https://github.com/wisteken/dagm2007 ; further mirrors: search "DAGM 2007" on Kaggle.

## D. Thermography (infrared NDT / monitoring)

### 12. InfraredSolarModules
20,000 infrared (thermographic) images of photovoltaic modules with 12 annotated anomaly classes (hotspot, diode multihotspot, cell mismatch, open circuit, shadow, soiling, ...) plus a no-anomaly class — thermographic NDT of energy infrastructure in dataset form. MIT-licensed, easy to download.
- URL: https://github.com/RaptorMaps/InfraredSolarModules
- For electrical-equipment IR thermography, additional sets exist on IEEE DataPort / Mendeley (search "infrared thermography electrical equipment fault dataset").

## E. Camera-based machinery monitoring (images & video)

### 13. AeBAD — Aero-engine Blade Anomaly Detection (AeBAD-S + AeBAD-V)
Real aero-engine blade images (AeBAD-S, with pixel-level defect masks) and blade **videos** (AeBAD-V), deliberately recorded with a **domain shift** between train and test normal conditions (illumination, viewpoint, background) — a realistic benchmark for vision-based machine condition monitoring. Computers in Industry 2023 (arXiv:2304.02216).
- Dataset links via official repo: https://github.com/zhangzilongc/MMR (CC BY 4.0)
- Paper: https://arxiv.org/abs/2304.02216

### 14. IndustReal
84 egocentric **videos** of 27 participants performing standardized maintenance and assembly procedures on industrial-like components, with step-level annotations and 3D part geometries (4TU.ResearchData, versioned DOIs). Not machine-surface NDT, but public video data for maintenance-process monitoring and error detection.
- URL: https://github.com/TimSchoonbeek/IndustReal (Apache-2.0 extension)
- Data: https://data.4tu.nl/datasets/611adbc7-7935-43a6-8c3f-b2260a508e73

### 15. Concrete Crack Images for Classification
40,000 RGB images (227×227), 20,000 cracked / 20,000 non-cracked, collected from METU campus buildings — the standard visual-inspection (VT) dataset for structural/civil NDT with CNNs.
- URL: https://data.mendeley.com/datasets/5y9wdsg2zt (DOI 10.17632/5y9wdsg2zt.2, CC BY 4.0)

---

## Meta-resources

- **MVTec dataset family** (AD, AD 2, LOCO, 3D-AD, ITODD, Screws...): https://www.mvtec.com/research-teaching/datasets
- **Awesome Industrial Datasets** — 189 entries, filterable by modality (Image / X-ray / Video) and task: https://github.com/jonathanwvd/awesome-industrial-datasets (HTML: https://www.indatlas.com/datasets/)
- **ViCoS Lab resources** (Kolektor datasets and more surface-inspection research): https://www.vicos.si/resources/
- **Computer Vision X-ray Testing** GitHub organization (GDXray + X-ray testing tools): https://github.com/computervision-xray-testing
- **Further candidates** (verified present in the awesome-industrial-datasets index; fetch their pages for exact sources): GC10-DET (10 metal surface defect classes), BSData (metal surface, instance segmentation, CC BY-SA), BTAD (BeanTech anomaly dataset), Eyecandies (multimodal RGB-D industrial anomalies), 3D-ADAM (additive manufacturing, includes RGB-D).

## Practical notes

1. **Licenses**: MVTec AD/LOCO and KolektorSDD/SDD2 are **CC BY-NC-SA** (non-commercial); InfraredSolarModules and IndustReal are MIT/Apache; DeepPCB data is research-use-only; Mendeley/Kaggle entries vary (concrete cracks: CC BY 4.0). Always check before redistribution or commercial use.
2. **Realism**: KolektorSDD/SDD2, Severstal, casting images, AeBAD and CXR-AD are real production data; DAGM is simulated texture; MVTec AD is staged but real objects.
3. **Videos**: AeBAD-V and GDXray sequences are the most relevant true video sources for machine inspection; IndustReal covers human maintenance procedures.
4. **Where to start**: MVTec AD for anomaly detection methodology; NEU-DET or KolektorSDD for defect segmentation; GDXray for X-ray NDT; InfraredSolarModules for thermography.

_Thinking..._

> I now have web search available again, so I should actually try to verify direct dataset links instead of assuming they're inaccessible. Let me search for the key sources: Strathclyde FMC dataset, USimgAIST GitHub, Bristol Pyle data, Virkkunen Zenodo, arim, and the Strathclyde CFRP dataset.
> 
> I need more specific dataset links—things like Strathclyde PURE's FMC weld dataset DOI, USimgAIST and arim GitHub repos, Strathclyde's CFRP dataset, Kaggle/Roboflow PAUT sets, Evident and Zetec sample files, and Bristol's data repository.
> 
> Since I've hit the search limit again, I'll need to rely on my own recollection of the dataset citations, flagging clearly where I'm not fully certain of a URL — I believe the Strathclyde FMC dataset referenced in the CVPRW paper involves a welded stainless steel plate capture.
> 
> I'm also recalling simulation tool homepages like Pogo, k-Wave, SimSonic, and CIVA, plus Evident's OmniPC sample data and NDE file format resources, Zetec UltraVision demo data, and Virkkunen's arXiv work -- flagging that several of these URLs I'm less confident about and should verify before presenting.
> 
> I'm adding other dataset search entry points: Roboflow Universe and Kaggle searches for ultrasonic weld defects, plus Zenodo's BAM community page as another place to look for relevant datasets.
> 
> I'm also noting Gantala & Balasubramaniam's paper DOI and a Mendeley Data search link, plus a Strathclyde paper on GANs for PAUT defect detection whose dataset location I can't confirm — I should flag it as unverified rather than guess a DOI, and avoid inventing any "Open Weld Inspection PAUT Dataset" I can't substantiate.
> 
> I also need to correct myself: arim (the FMC examples repo) is from University of Bristol's NDT group, not Imperial, so I should fix that attribution. I'll also check IEEE DataPort, then compile everything into a table with a verification status column, being honest that my search quota ran out partway through.

I'll verify direct dataset URLs before adding them to the tables.I started verifying URLs but the search quota ran out after the first batch, so I could only confirm a handful. In the tables below, **✅** = link checked this session (or stable paper landing page), **⚠** = from memory / repository search page — please verify before citing. Where I couldn't confirm an exact DOI I give the repository's search URL pre-filled with the right query, which gets you there in one click.

---

## A. Raw phased-array / FMC data (openly downloadable)

|#|Dataset|Content|Direct link(s)|Notes|
|---|---|---|---|---|
|1|**Strathclyde open FMC weld dataset**|FMC, 5 MHz linear array, 22 mm welded stainless plate, 6 mm lack-of-fusion flaw at ~50°; v_L = 5820 m/s|⚠ Strathclyde dataset portal search: [https://pureportal.strath.ac.uk/en/datasets/?search=full%20matrix%20capture](https://pureportal.strath.ac.uk/en/datasets/?search=full%20matrix%20capture) · ✅ paper that uses it (cites dataset DOI in refs): [https://openaccess.thecvf.com/content/CVPR2023W/DL-UIA/papers/Luiken_A_Deep_Learning-Based_Approach_To_Increase_Efficiency_in_the_Acquisition_CVPRW_2023_paper.pdf](https://openaccess.thecvf.com/content/CVPR2023W/DL-UIA/papers/Luiken_A_Deep_Learning-Based_Approach_To_Increase_Efficiency_in_the_Acquisition_CVPRW_2023_paper.pdf)|Real FMC A-scans; beamform TFM yourself. Single flaw → detection/segmentation or real-noise source rather than multi-class training.|
|2|**Strathclyde CFRP PAUT datasets** (McKnight / Tunukovic et al.)|Robotic PAUT 0° scans of CFRP panels with inserts/machined defects, bounding-box labels; GAN/synthetic-noise variants|⚠ [https://pureportal.strath.ac.uk/en/datasets/?search=ultrasonic%20CFRP](https://pureportal.strath.ac.uk/en/datasets/?search=ultrasonic%20CFRP) · ✅ related Strathclyde open-access papers: [https://strathprints.strath.ac.uk/cgi/search/simple?q=phased+array+CFRP+deep+learning](https://strathprints.strath.ac.uk/cgi/search/simple?q=phased+array+CFRP+deep+learning)|Composite, not weld. Good for domain-adaptation experiments.|
|3|**Bristol (Pyle et al.) crack-characterisation data**|Simulated (25,625 sets) + experimental FMC/plane-wave images of surface-breaking cracks 1–5 mm, ±24°; labels = length, angle, position|⚠ Bristol Research Data Repository search: [https://data.bris.ac.uk/data/search/?q=ultrasonic+crack](https://data.bris.ac.uk/data/search/?q=ultrasonic+crack) · ✅ paper (Table I/II describe the sets): [https://research-information.bris.ac.uk/ws/files/286790774/clean_file_for_Xplore.pdf](https://research-information.bris.ac.uk/ws/files/286790774/clean_file_for_Xplore.pdf) · ✅ follow-up (domain adaptation): [https://strathprints.strath.ac.uk/84057/1/Pyle_etal_IEEE_TUFFC_2022_Domain_adapted_deep_learning_for_improved.pdf](https://strathprints.strath.ac.uk/84057/1/Pyle_etal_IEEE_TUFFC_2022_Domain_adapted_deep_learning_for_improved.pdf)|Regression/characterisation labels; cracks only. Check the "Data availability" paragraph in each paper for the exact data.bris DOI.|
|4|**BAM ultrasonic echo / multistatic datasets**|Phased-array & multistatic ultrasonic data on reference concrete/steel specimens|⚠ Zenodo BAM community: [https://zenodo.org/communities/bam/](https://zenodo.org/communities/bam/) · ⚠ Zenodo query: [https://zenodo.org/search?q=%22full%20matrix%20capture%22%20OR%20%22phased%20array%20ultrasonic%22](https://zenodo.org/search?q=%22full%20matrix%20capture%22%20OR%20%22phased%20array%20ultrasonic%22)|Mostly civil-engineering targets; useful for imaging algorithms.|
|5|**Vendor sample inspection files**|Real PAUT acquisitions (cal blocks, weld mock-ups) in native formats|⚠ Evident/Olympus software & sample data downloads: [https://www.olympus-ims.com/en/service-and-support/downloads/](https://www.olympus-ims.com/en/service-and-support/downloads/) · ⚠ Evident `.nde` open format (HDF5) docs: [https://www.evidentscientific.com/en/ndt/nde-file-format](https://www.evidentscientific.com/en/ndt/nde-file-format) · ⚠ Zetec UltraVision (demo data ships with viewer): [https://www.zetec.com/products/ultrasound/software/ultravision/](https://www.zetec.com/products/ultrasound/software/ultravision/) · ⚠ Eddyfi Capture: [https://www.eddyfi.com/en/product/capture](https://www.eddyfi.com/en/product/capture)|Unlabelled but genuine field data; ideal for building parsers and deployment tests.|

## B. Image-based ultrasonic datasets (public, labelled)

|#|Dataset|Content|Direct link(s)|Notes|
|---|---|---|---|---|
|6|**USimgAIST** (Ye & Toyama, AIST)|7,004 ultrasonic wave-propagation images, 18 steel plates, 17 flaw types (holes 1–5 mm, slits 3–10 mm, 0–90° incidence), 3615 no-defect / 3389 defect|✅ Paper with dataset description and repo pointer: [https://ieeexplore.ieee.org/document/9366507](https://ieeexplore.ieee.org/document/9366507) · ⚠ GitHub search for the repo named in the paper: [https://github.com/search?q=USimgAIST&type=repositories](https://github.com/search?q=USimgAIST&type=repositories) · ✅ earlier Sensors 2018 paper: [https://www.mdpi.com/1424-8220/18/11/3820](https://www.mdpi.com/1424-8220/18/11/3820)|Laser-ultrasonic visualisation, **not** phased array — but the most-cited public ultrasonic NDT benchmark.|
|7|**Virkkunen / Koskinen / Siljama (Aalto, VTT, Trueflaw)**|TRS phased-array (1.8 MHz matrix, Zetec Dynaray) line scans, 316L austenitic butt weld, 3 thermal-fatigue cracks (1.6/4.0/8.6 mm); virtual-flaw augmentation; later multi-channel B-scan work|✅ arXiv 1903.11399: [https://arxiv.org/abs/1903.11399](https://arxiv.org/abs/1903.11399) · ✅ Aalto thesis on multichannel B-scan flaw detection (same specimens): [https://aaltodoc.aalto.fi/bitstreams/6f2323d7-3233-4130-b1f4-e3189ca13732/download](https://aaltodoc.aalto.fi/bitstreams/6f2323d7-3233-4130-b1f4-e3189ca13732/download) · ⚠ Siljama et al. 2021, J. Nondestruct. Eval. (check data-availability statement): [https://doi.org/10.1007/s10921-021-00788-4](https://doi.org/10.1007/s10921-021-00788-4)|Data release was partial/on-request in my recollection; the virtual-flaw method itself is the main takeaway.|
|8|**Roboflow Universe / Kaggle user uploads**|Small S-scan / B-scan screenshot sets with boxes for porosity, LOF, cracks, slag|⚠ [https://universe.roboflow.com/search?q=ultrasonic%20weld](https://universe.roboflow.com/search?q=ultrasonic%20weld) · ⚠ [https://universe.roboflow.com/search?q=phased%20array](https://universe.roboflow.com/search?q=phased%20array) · ⚠ [https://www.kaggle.com/search?q=ultrasonic+weld+defect+in%3Adatasets](https://www.kaggle.com/search?q=ultrasonic+weld+defect+in%3Adatasets) · ⚠ [https://www.kaggle.com/search?q=phased+array+ultrasonic+in%3Adatasets](https://www.kaggle.com/search?q=phased+array+ultrasonic+in%3Adatasets)|Provenance and licensing vary; treat as supplementary/test-only.|

## C. Simulated / synthetic routes

| #   | Resource                                                                                                                  | Direct link(s)                                                                                                                                                                                                                                                                                     | Use                                                                                                        |
| --- | ------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 9   | **CIVA (CEA/Extende)**                                                                                                    | ⚠ [https://www.extende.com/civa-ut](https://www.extende.com/civa-ut)                                                                                                                                                                                                                               | Commercial; unlimited labelled sector scans/FMC of SDH, FBH, notches, LOF, porosity.                       |
| 10  | **Gantala & Balasubramaniam, IIT Madras** — FE-simulated FMC→TFM weld images (porosity/slag) + DCGAN + experimental noise | ✅ Paper: [https://link.springer.com/10.1007/s10921-021-00761-1](https://link.springer.com/10.1007/s10921-021-00761-1) · ⚠ Mendeley Data search: [https://data.mendeley.com/research-data/?search=TFM%20ultrasonic%20weld](https://data.mendeley.com/research-data/?search=TFM%20ultrasonic%20weld) | Six dataset variants described; check paper's data statement or contact authors.                           |
| 11  | **`arim`** — Bristol's open-source Python FMC/TFM toolbox (ships example FMC data)                                        | ⚠ [https://github.com/ndtatbristol/arim](https://github.com/ndtatbristol/arim)                                                                                                                                                                                                                     | Quick real FMC for pipeline tests. (Correction to my earlier message: arim is from Bristol, not Imperial.) |
| 12  | **Pogo** (Imperial, GPU FE)                                                                                               | ⚠ [http://www.pogo.software/](http://www.pogo.software/)                                                                                                                                                                                                                                           | Fast FE generation of FMC with controlled defect classes.                                                  |
| 13  | **k-Wave**                                                                                                                | ✅ [http://www.k-wave.org/](http://www.k-wave.org/)                                                                                                                                                                                                                                                 | Open-source acoustic/elastic simulation.                                                                   |
| 14  | **SimSonic**                                                                                                              | ⚠ [http://www.simsonic.fr/](http://www.simsonic.fr/)                                                                                                                                                                                                                                               | Open-source FDTD elastic solver.                                                                           |
| 15  | **MATLAB Ultrasonic Toolbox** (UT array imaging)                                                                          | ⚠ [https://www.mathworks.com/matlabcentral/fileexchange/?q=ultrasonic+array+imaging](https://www.mathworks.com/matlabcentral/fileexchange/?q=ultrasonic+array+imaging)                                                                                                                             | Community TFM/FMC codes with sample data.                                                                  |

## D. Described in literature but _not_ public (useful for protocol replication / data requests)

|Study|Data|Link|
|---|---|---|
|Oil & gas AUT girth-weld B-scan LOF (87 records, SAM fine-tuning)|Proprietary|✅ [https://www.mdpi.com/1424-8220/25/19/6128](https://www.mdpi.com/1424-8220/25/19/6128) · [https://pmc.ncbi.nlm.nih.gov/articles/PMC12527071/](https://pmc.ncbi.nlm.nih.gov/articles/PMC12527071/)|
|40-specimen butt-weld A-scan set (Normal/Linear/Volumetric, CNN+FiLM)|Proprietary|✅ [https://link.springer.com/article/10.1007/s42405-026-01251-2](https://link.springer.com/article/10.1007/s42405-026-01251-2)|
|800-image girth-weld PAUT (slag/cracks/porosity/LOF, YOLOv8)|In-house|✅ [https://www.mdpi.com/2075-4701/16/5/458](https://www.mdpi.com/2075-4701/16/5/458)|
|HIC steel + Al SDH B-scan segmentation (OmniScan X3)|In-house|✅ [https://www.mdpi.com/2079-9292/15/15/3267](https://www.mdpi.com/2079-9292/15/15/3267)|
|Small-bore nozzle fillet-weld FMC/TFM (YOLO11)|In-house|✅ [https://www.nature.com/articles/s41598-026-62395-5](https://www.nature.com/articles/s41598-026-62395-5)|
|Narrow-gap weld dual-tandem FMC, LOSWF notches (Strathclyde)|Possibly on request|✅ [https://strathprints.strath.ac.uk/88244/1/Nicolson-etal-NDTEI-2024-Towards-an-in-process-ultrasonic-phased-array-inspection-method.pdf](https://strathprints.strath.ac.uk/88244/1/Nicolson-etal-NDTEI-2024-Towards-an-in-process-ultrasonic-phased-array-inspection-method.pdf)|

---

## Repository search shortcuts (for anything new since this list)

|Repository|Pre-filled search|
|---|---|
|Zenodo|[https://zenodo.org/search?q=%22phased%20array%22%20ultrasonic%20dataset](https://zenodo.org/search?q=%22phased%20array%22%20ultrasonic%20dataset)|
|IEEE DataPort|[https://ieee-dataport.org/search?q=ultrasonic%20phased%20array](https://ieee-dataport.org/search?q=ultrasonic%20phased%20array)|
|Mendeley Data|[https://data.mendeley.com/research-data/?search=phased%20array%20ultrasonic](https://data.mendeley.com/research-data/?search=phased%20array%20ultrasonic)|
|data.bris (Bristol)|[https://data.bris.ac.uk/data/search/?q=full+matrix+capture](https://data.bris.ac.uk/data/search/?q=full+matrix+capture)|
|Strathclyde PURE datasets|[https://pureportal.strath.ac.uk/en/datasets/?search=ultrasonic](https://pureportal.strath.ac.uk/en/datasets/?search=ultrasonic)|
|figshare|[https://figshare.com/search?q=phased%20array%20ultrasonic%20NDT](https://figshare.com/search?q=phased%20array%20ultrasonic%20NDT)|
|Papers with Code|[https://paperswithcode.com/search?q=ultrasonic+NDT](https://paperswithcode.com/search?q=ultrasonic+NDT)|

If you'd like, I can run a second verification pass later (when search is available again) to replace the ⚠ repository-search URLs with exact dataset DOIs for items 1, 2, 3, 6 and 7 — those are the five that matter most for your use case.

Learn more:

- [https://strathprints.strath.ac.uk/88244/1/Nicolson-etal-NDTEI-2024-Towards-an-in-process-ultrasonic-phased-array-inspection-method.pdf](https://strathprints.strath.ac.uk/88244/1/Nicolson-etal-NDTEI-2024-Towards-an-in-process-ultrasonic-phased-array-inspection-method.pdf)
- [https://strathclyde-prod2.scu.cdl.cosector.com/downloads/d504rk88r?locale=en](https://strathclyde-prod2.scu.cdl.cosector.com/downloads/d504rk88r?locale=en)
- [https://strathprints.strath.ac.uk/94680/1/Macleod-etal-2025-Real-time-fully-focused-imaging-with-parameter-estimation.pdf](https://strathprints.strath.ac.uk/94680/1/Macleod-etal-2025-Real-time-fully-focused-imaging-with-parameter-estimation.pdf)
- [https://strathprints.strath.ac.uk/78785/1/Zimermann_etal_AM_2021_Multi_layer_ultrasonic_imaging_of_as_built_Wire.pdf](https://strathprints.strath.ac.uk/78785/1/Zimermann_etal_AM_2021_Multi_layer_ultrasonic_imaging_of_as_built_Wire.pdf)
- [http://stax.strath.ac.uk/downloads/s7526c81k](http://stax.strath.ac.uk/downloads/s7526c81k)
- [http://xplorestaging.ieee.org/ielx7/6287639/9312710/09366507.pdf?arnumber=9366507](http://xplorestaging.ieee.org/ielx7/6287639/9312710/09366507.pdf?arnumber=9366507)
- [https://github.com/adamtupper/ultrabench](https://github.com/adamtupper/ultrabench)
- [https://github.com/hugofigueiras/Breast-Cancer-Imaging-Datasets](https://github.com/hugofigueiras/Breast-Cancer-Imaging-Datasets)
- [https://redirect.github.com/Bean-Young/AHU-Database/blob/main/README.md](https://redirect.github.com/Bean-Young/AHU-Database/blob/main/README.md)
- [https://redirect.github.com/Bean-Young/AHU-Database](https://redirect.github.com/Bean-Young/AHU-Database)
- [https://research-information.bris.ac.uk/ws/files/286790774/clean_file_for_Xplore.pdf](https://research-information.bris.ac.uk/ws/files/286790774/clean_file_for_Xplore.pdf)
- [https://strathprints.strath.ac.uk/84582/1/Pyle_etal_IEEE_TUFFC_2021_Deep_learning_for_ultrasonic_crack.pdf](https://strathprints.strath.ac.uk/84582/1/Pyle_etal_IEEE_TUFFC_2021_Deep_learning_for_ultrasonic_crack.pdf)
- [https://strathprints.strath.ac.uk/84057/1/Pyle_etal_IEEE_TUFFC_2022_Domain_adapted_deep_learning_for_improved.pdf](https://strathprints.strath.ac.uk/84057/1/Pyle_etal_IEEE_TUFFC_2022_Domain_adapted_deep_learning_for_improved.pdf)
- [https://www.researchgate.net/publication/347730444_Deep_Learning_for_Ultrasonic_Crack_Characterization_in_NDE](https://www.researchgate.net/publication/347730444_Deep_Learning_for_Ultrasonic_Crack_Characterization_in_NDE)
- [https://pubmed.ncbi.nlm.nih.gov/33338015/](https://pubmed.ncbi.nlm.nih.gov/33338015/)
- [https://aaltodoc.aalto.fi/bitstreams/6f2323d7-3233-4130-b1f4-e3189ca13732/download](https://aaltodoc.aalto.fi/bitstreams/6f2323d7-3233-4130-b1f4-e3189ca13732/download)
- [https://arxiv.org/html/1903.11399v1](https://arxiv.org/html/1903.11399v1)
- [http://arxiv.org/pdf/1903.11399.pdf](http://arxiv.org/pdf/1903.11399.pdf)
- [https://arxiv.org/abs/1903.11399v1](https://arxiv.org/abs/1903.11399v1)
- [https://www.researchgate.net/publication/332035082_Augmented_Ultrasonic_Data_for_Machine_Learning](https://www.researchgate.net/publication/332035082_Augmented_Ultrasonic_Data_for_Machine_Learning)
- [https://strathprints.strath.ac.uk/61667/1/Stratoudaki_etal_QNDE_2017_Full_matrix_capture_and_the_total_focusing_imaging_algorithm_using_laser_induced_ultrasonic.pdf](https://strathprints.strath.ac.uk/61667/1/Stratoudaki_etal_QNDE_2017_Full_matrix_capture_and_the_total_focusing_imaging_algorithm_using_laser_induced_ultrasonic.pdf)
- [https://strathprints.strath.ac.uk/42803/1/Nantes_Published_Paper.pdf](https://strathprints.strath.ac.uk/42803/1/Nantes_Published_Paper.pdf)
- [https://strathprints.strath.ac.uk/62440/1/Stratoudaki_etal_IUS_2017_total_focusing_method_to_laser_ultrasonics_for_remote_non_destructive_testing.pdf](https://strathprints.strath.ac.uk/62440/1/Stratoudaki_etal_IUS_2017_total_focusing_method_to_laser_ultrasonics_for_remote_non_destructive_testing.pdf)
- [https://strathprints.strath.ac.uk/71927/1/Stratoudaki_etal_OE_2016_Laser_induced_ultrasonic_phased_array_using_full_matrix_capture_data_acquisition_and_total_focusing_method.pdf](https://strathprints.strath.ac.uk/71927/1/Stratoudaki_etal_OE_2016_Laser_induced_ultrasonic_phased_array_using_full_matrix_capture_data_acquisition_and_total_focusing_method.pdf)