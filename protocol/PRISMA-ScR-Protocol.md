# Scoping Review Protocol (PRISMA-ScR)

**Project ID:** P001  
**Title:** AI-BIM Integration for Early-Stage Building Energy Performance Prediction: A Scoping Review  
**Principal Investigator:** Hadjer Bessai (Built Environment AI Initiative)  
**Registration Date:** November 2026  
**Contact:** `contact@built-environment-ai.org`

---

## 1. Rationale and Objective

Early-stage architectural decisions—such as building massing, orientation, window-to-wall ratio, and envelope thermal properties—lock in the majority of operational building energy demand. While Building Information Modelling (BIM) provides rich geometric and semantic data, coupling BIM directly with dynamic physics-based Building Performance Simulation (BPS) engines (e.g., EnergyPlus) remains computationally expensive and prone to interoperability bottlenecks during rapid design iteration.

Data-driven surrogate models and machine learning workflows offer rapid energy performance feedback directly from BIM parameters, yet the literature spans fragmented BIM schemas, simulation engines, ML algorithms, and validation practices. This scoping review maps the methodological landscape, identifies interoperability and interpretability gaps, and establishes a structured taxonomy for AI-BIM energy prediction frameworks.

## 2. Research Questions

1. **RQ1 (BIM-to-BPS Interoperability & Data Extraction):** What BIM authoring tools, open exchange schemas (e.g., IFC, gbXML), and automated extraction pipelines (e.g., Dynamo, Revit API, pyRevit) are used to generate training features and simulation inputs?
2. **RQ2 (Machine Learning & Surrogate Architectures):** Which supervised, ensemble, or deep learning algorithms are applied for early-stage energy prediction, and how are synthetic training datasets generated and sized?
3. **RQ3 (Interpretability & Uncertainty):** To what extent do existing AI-BIM workflows incorporate explainable AI (XAI) techniques (e.g., SHAP, LIME, permutation importance) and uncertainty quantification to support architectural decision-making?
4. **RQ4 (Scope, Typologies & Practical Deployment):** Which building typologies, climate zones, design stages (LOD 100–300), and user-facing deployment interfaces are represented, and what key barriers limit real-world adoption?

## 3. Eligibility Criteria (PCC Framework)

| Dimension | Inclusion Criteria | Exclusion Criteria |
| :--- | :--- | :--- |
| **Population** | Residential, commercial, educational, or mixed-use buildings evaluated at early architectural design or early retrofit planning stages. | District/urban grid load forecasting without building-level BIM parameters; post-occupancy HVAC fault detection only. |
| **Concept** | Workflows integrating BIM parameters/models with AI/ML algorithms to predict building energy performance (heating, cooling, lighting, EUI, or thermal load). | Pure physics-based BIM-to-BPS workflows without AI/ML; AI energy prediction models lacking BIM data integration. |
| **Context** | Peer-reviewed journal articles and full conference papers published between **2016 and 2026** in **English or French**. | Editorials, abstracts without full papers, non-peer-reviewed blog posts, and duplicate records. |

## 4. Information Sources and Search Strategy

Structured boolean searches will be executed across five primary databases:
- **Scopus**
- **Web of Science Core Collection**
- **IEEE Xplore**
- **ScienceDirect**
- **CumInCAD** (Cumulative Index about Publications in Computer Aided Architectural Design)

### Core Boolean Concept String
```text
("Building Information Modeling" OR "Building Information Modelling" OR "BIM" OR "IFC" OR "gbXML")
AND
("Artificial Intelligence" OR "Machine Learning" OR "Deep Learning" OR "Surrogate Model" OR "Neural Network" OR "Random Forest" OR "XGBoost" OR "Gradient Boosting")
AND
("Energy Performance" OR "Energy Consumption" OR "Energy Prediction" OR "Thermal Load" OR "Heating Load" OR "Cooling Load" OR "Building Performance Simulation" OR "EnergyPlus")
```

## 5. Study Selection and Data Charting Schema

All retrieved records will be deduplicated and screened in two stages: (1) Title and Abstract screening against PCC criteria, and (2) Full-Text eligibility assessment, documented via a PRISMA-ScR flow diagram.

Each included study will be charted into a structured CSV dataset (`data/p001_extracted_studies.csv`) capturing:
- `study_id`, `authors`, `year`, `venue`, `country_case_study`, `climate_zone`
- `building_typology`, `design_stage_lod`, `sample_size_runs`
- `bim_platform`, `exchange_schema`, `extraction_tool`, `bps_engine`
- `ml_algorithms`, `target_metrics` (e.g., EUI, heating/cooling demand), `validation_method`, `reported_accuracy`
- `xai_method`, `deployment_interface`, `open_code_or_data_available`
```

---

Once you commit these five files, would you like to connect your custom domain `built-environment-ai.org` to a free GitHub Pages landing site so visitors opening `[https://built-environment-ai.org](https://built-environment-ai.org)` see an official homepage for the initiative?
