# 📡 Open RAN (O-RAN) — Curated Research Library 

This repository is a curated, structured research library and mini-survey focused on Open Radio Access Networks (O-RAN), the RAN Intelligent Controller (RIC) ecosystem, and the intersection of AI/ML with next-generation wireless systems (5G → 6G). It is intended for researchers, graduate students, and engineers conducting literature reviews, prototyping xApps/rApps/dApps, or designing experiments on O-RAN testbeds.

---

## 📖 Introduction to O-RAN

Open Radio Access Network (O-RAN) is a movement and set of specifications that disaggregate traditional, vendor-specific base stations into interoperable, modular components connected via open interfaces and controlled using software-defined, cloud-native principles. O-RAN embraces programmable control, virtualization, and native support for AI/ML-driven automation.

Brief overview of O-RAN architecture
- O-RAN decomposes the traditional gNodeB (gNB) into logical components to enable vendor interoperability and flexible deployment:
  - O-CU (Open Centralized Unit): hosts higher RAN protocol layers (PDCP, RRC, SDAP) and is often split into control plane (O-CU-CP) and user plane (O-CU-UP).
  - O-DU (Open Distributed Unit): hosts mid and lower RAN layers (MAC, RLC, high-PHY) and performs near-real-time scheduling and latency-sensitive processing.
  - O-RU (Open Radio Unit): handles radio frequency (RF) and lower-PHY analog/digital front-end functions (DFE/IF conversion, FFT/IFFT).
- Open fronthaul and other open interfaces (e.g., Open Fronthaul, E2, A1, O1) enable multi-vendor deployments and flexible placement of functions across edge and cloud.

Key components: O-CU, O-DU, O-RU, RIC
- O-CU: Centralized control and higher-layer processing; suitable for virtualization in regional clouds.
- O-DU: Edge/near-edge processing with deterministic timing requirements.
- O-RU: Radio front-end and real-time PHY primitives.
- RIC (RAN Intelligent Controller):
  - Non-RT RIC (>1s): Operates in the SMO (Service Management and Orchestration) plane. Hosts rApps for long-term policy, model training, and offline analytics.
  - Near-RT RIC (10ms–1s): Runs xApps for policy enforcement, closed-loop control, and telemetry-driven decisions via the E2 interface.

Importance in 5G and emerging 6G networks
- Enables multi-vendor ecosystems and reduces vendor lock-in through open interfaces.
- Provides a native platform for integrating AI/ML into control loops, enabling intent-based management, adaptive resource allocation, and automated fault recovery.
- Is foundational for 6G trends—edge-native intelligence, extreme heterogeneity (spectrum, hardware), and an emphasis on low-latency, high-assurance control for novel services.

---

## 📚 Curated Literature Review

Below is a categorized, curated list of influential and representative works. For each entry: Title, Authors, Year, 2–3 lines on key contributions, and a direct link to the paper (publisher/arXiv/official page). This list is not exhaustive—use it as a starting point for deeper reading.

O-RAN Architecture & Standards
- Understanding O-RAN: Architecture, Interfaces, Algorithms, Security, and Research Challenges — M. Polese, L. Bonati, S. D’Oro, S. Basagni, T. Melodia (2023)  
  Key contributions: Comprehensive survey covering O-RAN building blocks, interfaces (E2/A1/O1), algorithmic opportunities, and security considerations; synthesizes research directions.  
  Link: https://ieeexplore.ieee.org (search by title)
- Colosseum: The Open RAN Digital Twin — M. Polese, L. Bonati, et al. (2024)  
  Key contributions: Presents Colosseum as a high-fidelity wireless emulator for reproducible O-RAN research and pre-training ML agents using hardware-in-the-loop channel emulation.  
  Link: https://northeastern.edu/colosseum (project page)

RIC & Intelligent Control (AI/ML in O-RAN)
- ORION: Intent-Aware Orchestration in Open RAN for SLA-Driven Network Management — G. S. Machado, et al. (Preprint / 2026)  
  Key contributions: Proposes hierarchical agents and LLM-aided intent translation to map operator intents into RIC policies for SLA assurance.  
  Link: publisher / preprint server (search by title)
- ColO-RAN: Developing Machine Learning-Based xApps for Open RAN Closed-loop Control — M. Polese, L. Bonati, et al. (2023)  
  Key contributions: Framework and examples for training and deploying ML-based xApps on the Near-RT RIC; benchmark scenarios and design patterns.  
  Link: search by title / arXiv

xApps and rApps (Control, Coordination, Conflict Mitigation)
- Experimental evaluation of xApp Conflict Mitigation Framework in O-RAN — A. Sultana, et al. (2024)  
  Key contributions: Introduces conflict detection and mitigation methods when multiple xApps with competing objectives act on the same RAN resources; experimental validation on SDR testbeds.  
  Link: search by title
- dApps: Enabling Real-Time AI-Based Open RAN Control — A. Lacava, L. Bonati, et al. (2025)  
  Key contributions: Describes very-low-latency microservices (dApps) embedded near the DU/CU to meet sub-10ms control demands and complement xApps.  
  Link: search by title

Network Slicing & Resource Optimization
- DORA: Dynamic O-RAN Resource Allocation for Multi-Slice 5G Networks — J. Moore, A. S. Abdalla, et al. (2025)  
  Key contributions: Demonstrates adaptive PRB allocation across slices using DRL; extensive simulation and emulation results show improved slice-level SLA satisfaction.  
  Link: search by title
- Enhancing AI Transparency: XRL-Based Resource Management and RAN Slicing — S. Mhatre, F. Adelantado, et al. (2024)  
  Key contributions: Proposes Explainable Reinforcement Learning (XRL) for resource management to provide operator-understandable policies while retaining performance.  
  Link: search by title

Security in O-RAN
- Implementing and Evaluating Security in O-RAN: Interfaces, Intelligence, and Platforms — J. Groen, S. D’Oro, et al. (2023)  
  Key contributions: Analyzes attack surfaces across A1/E2/O1 and O-RAN components; quantifies cryptographic and processing overheads and proposes mitigations.  
  Link: search by title

Integration with 6G / Future Networks
- Proactive AI-and-RAN Workload Orchestration in O-RAN Architectures for 6G Networks — S. D. A. Shah, et al. (2025)  
  Key contributions: Explores transposition of O-RAN automation for 6G use-cases, dynamic workload placement across edge-cloud continuum, and SAC-based orchestration.  
  Link: search by title

Notes
- The above selection combines canonical surveys, system papers, and applied research demonstrating O-RAN’s potential and open challenges. For a focused literature review, expand each category with domain-specific queries (e.g., “O-RAN E2 security”, “xApp conflict mitigation”, “DRL for PRB allocation”).

---

## 🔗 Standards and Official Documentation

Authoritative standards and documentation are essential for interoperability and reproducibility:
- O-RAN Alliance Specifications — https://www.o-ran.org/specifications  
  (E2, A1, O1, Open Fronthaul, Near-RT RIC, Non-RT RIC)
- 3GPP Releases & Technical Specifications — https://www.3gpp.org/  
  (Relevant specs: NG-RAN split documents, TS 38.401, 38.300-series for NR)
- ETSI (relevant transpositions and technical reports) — https://www.etsi.org/  
- Telecom Infra Project (TIP) — OpenRAN resources and deployment blueprints — https://telecominfraproject.com/openran/

---

## 📊 Datasets and Testbeds

Public datasets and large-scale testbeds accelerate reproducible research and ML training.

Public Datasets (examples and starting points)
- Colosseum RF & Protocol Datasets — large-scale channel and protocol traces from high-fidelity emulation (useful for DRL pre-training). Project page: https://www.northeastern.edu/colosseum/  
- RAN telemetry / performance datasets — look for datasets published alongside xApp/rApp papers and in OpenRAN Gym / SCOPE repositories.  
- Traffic and UE-level traces — datasets for modelling mobility, application-level demand, and handover events are available from community-driven archives and supplemental materials of published papers.

O-RAN Testbeds and Simulators
- Colosseum (largest wireless network emulator, hardware-in-the-loop) — https://www.northeastern.edu/colosseum/  
- POWDER-RENEW (PAWR testbed) — https://powderwireless.net/  
- Arena (Northeastern/WINES Lab experimental grid) — https://ece.northeastern.edu/wineslab/arena.php  
- OpenAirInterface (OAI) — full 3GPP-compatible protocol stack usable with SDRs — https://openairinterface.org/  
- ns-3 / ns-O-RAN integrations — ns-3 extensions and bindings allowing O-RAN RIC interfacing and large-scale discrete-event simulations — https://www.nsnam.org/ and ns-O-RAN project pages

Practical tip: Combine emulation (Colosseum) for wireless realism with ns-3 for large-scale control/traffic experiments and OAI/srsRAN for protocol stack-level validation.

---

## 🛠️ Open-Source Tools and Frameworks

A brief description and links to key open-source stacks:

- O-RAN Software Community (OSC) / O-RAN SC — Reference implementations of Near-RT RIC, SMO, and example xApps/rApps.  
  Project: https://o-ran-sc.org/
- srsRAN — Open-source 4G/5G software radio suite (CU/DU/RU elements) commonly used with SDRs.  
  GitHub: https://github.com/srsran/srsRAN
- OpenAirInterface (OAI) — 3GPP-compliant 5G/4G stack used for R&D and testbed integration.  
  Website: https://openairinterface.org/
- OpenRAN Gym / SCOPE — Tooling and APIs for data collection, experimentation, and xApp evaluation across emulators like Colosseum.  
  Project: https://openrangym.com/
- FlexRIC / µONOS-RIC — Lightweight, extendable Near-RT RIC implementations and SDKs used by academia and industry for building xApps.  
  Example: https://github.com/onosproject or FlexRIC project pages

Each project provides SDKs, example xApps/rApps, and integration notes—use them as foundations for reproducible experiments.

---

## 🧠 AI/ML in O-RAN

Role of AI/ML
- AI/ML transforms RAN control from static heuristics to data-driven, adaptive policies:
  - Reinforcement Learning (RL & DRL) for scheduling, PRB allocation, power control, and closed-loop mobility management.
  - Supervised and self-supervised learning for anomaly detection, KPI forecasting, and transfer learning across cells.
  - Large Language Models (LLMs) and agentic AI: emerging use-cases include intent translation in the Non-RT RIC (converting operator-level intents to rApp/xApp policies), assisted troubleshooting, and automated documentation of network changes.
  - Explainable ML (XAI/XRL) to provide operator trust and regulatory explanations for automatic decisions.

Representative research and implementations
- DRL-driven xApps for multi-slice PRB allocation and interference mitigation (see DORA and ColO-RAN papers).
- XRL methods for explainability in slice/resource management (see XRL-based resource management works).
- Practical toolchains: training in Colosseum or OpenRAN Gym, model packaging in Non-RT RIC for offline training, and Near-RT RIC for inference & policy enforcement.

Implementation considerations
- Data pipeline: telemetry ingestion (O1/E2 telemetry), feature engineering, labeling (where applicable), and continuous retraining cycles in the Non-RT RIC.
- Latency/compute trade-offs: move heavy training to cloud/non-RT RIC, place inference close to the edge (Near-RT RIC or even dApps) for stringent latency requirements.
- Safety: staged rollouts, shadow mode evaluation, offline emulation, and conflict mitigation frameworks are essential before live deployment.

---

## 📌 Key Research Gaps and Open Problems

1. Latency in RIC control loops
   - Near-RT RIC targets 10ms–1s; sub-1ms control (instantaneous MAC/beamforming decisions) remains challenging. Co-design of dApps and hardware acceleration near the DU/RU is an open area.

2. xApp/rApp interoperability & conflict mitigation
   - Multiple third-party xApps can issue competing actions. Standardized arbitration, priority models, explainability, and conflict-resolution policies are understudied in realistic deployments.

3. Data scarcity & generalization
   - Diverse, labeled datasets covering edge-case RF conditions, mobility anomalies, and multi-vendor deployments are limited. Domain adaptation, sim-to-real transfer, and robust offline training are pressing needs.

4. Explainability and trust
   - Operators demand transparent AI behaviors; integrating XAI in RL policies and providing human-in-the-loop controls is an open area.

5. Security & privacy at interfaces
   - E2/A1/O1 and Open Fronthaul introduce new attack surfaces; scalable, low-overhead security mechanisms compatible with real-time constraints are required.

6. Reproducibility and benchmarking
   - Standardized benchmarks, metrics, and reproducible scenarios across emulators (Colosseum), testbeds (POWDER), and protocol stacks (OAI, srsRAN) are needed to compare xApps/rApps fairly.

---

## 📎 References (selected — IEEE style)

[1] M. Polese, L. Bonati, S. D’Oro, S. Basagni, and T. Melodia, “Understanding O‑RAN: Architecture, Interfaces, Algorithms, Security, and Research Challenges,” IEEE Communications Surveys & Tutorials, 2023.  
[2] M. Polese, L. Bonati, et al., “Colosseum: The Open RAN Digital Twin,” Colosseum project publications, 2024.  
[3] A. Sultana, F. Bashar, M. R. Chowdhury, and A. P. Da Silva, “A software‑defined radio based O‑RAN platform for xApp conflict detection and mitigation,” in Proc. 2024 IEEE Military Communications Conference.  
[4] G. S. Machado, et al., “ORION: Intent‑Aware Orchestration in Open RAN for SLA‑Driven Network Management,” preprint, 2026.  
[5] J. Moore, A. S. Abdalla, et al., “DORA: Dynamic O‑RAN Resource Allocation for Multi‑Slice 5G Networks,” arXiv preprint arXiv:2509.07242, 2025.  
[6] A. Lacava, L. Bonati, et al., “dApps: Enabling Real‑Time AI‑Based Open RAN Control,” Computer Networks, vol. 269, p. 111342, 2025.  
[7] S. Mhatre, F. Adelantado, K. Ramantas, and C. Verikoukis, “Enhancing AI Transparency: XRL‑Based Resource Management and RAN Slicing,” in Proc. IEEE ICC, 2024.  
[8] J. Groen, S. D’Oro, U. Demir, L. Bonati, M. Polese, T. Melodia, and K. Chowdhury, “Implementing and Evaluating Security in O‑RAN: Interfaces, Intelligence, and Platforms,” arXiv preprint, 2023.  
[9] S. D. A. Shah, et al., “Proactive AI‑and‑RAN Workload Orchestration in O‑RAN Architectures for 6G Networks,” arXiv preprint, 2025.  

(For a machine-readable BibTeX export or to add direct DOI/arXiv links for each reference, I can expand this list and attach BibTeX entries.)

---

## How to use this library

- Start with the “O-RAN Architecture & Standards” papers to ground yourself in the interfaces and functional splits.  
- Reproduce baseline experiments using OAI/srsRAN and Colosseum or POWDER for wireless realism.  
- Use OpenRAN Gym / SCOPE to accelerate data collection and training pipelines for xApps.  
- When designing xApps/rApps, include conflict-mitigation logic and staged rollout (shadow mode → trial → production).

---

Acknowledgements
- Contributions and community-maintained projects listed above are fundamental to an open O-RAN research ecosystem. Cite original authors and projects when reusing code, datasets, or testbed resources.

License
- This README and the curated content may be redistributed with attribution. Respect the licenses of linked tools, datasets, and papers.
