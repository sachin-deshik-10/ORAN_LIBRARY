# 📡 Open RAN (O-RAN) & AI/ML Research Library
![O-RAN Alliance](https://img.shields.io/badge/O--RAN-Compliant-blue) ![5G/6G](https://img.shields.io/badge/Network-5G%20%7C%206G-success) ![AI/ML](https://img.shields.io/badge/Intelligence-AI%20%7C%20ML-orange) ![Open Source](https://img.shields.io/badge/Open_Source-Community-brightgreen)

> A curated, structured research repository and knowledge library exploring the intersection of Open Radio Access Networks (O-RAN), Artificial Intelligence (AI), and Next-Generation (6G) cellular systems.

---

## 📖 Introduction to O-RAN

The Open Radio Access Network (O-RAN) paradigm represents a fundamental shift from traditional, proprietary, and monolithic cellular base stations to an open, disaggregated, and software-defined architecture,. By decoupling hardware from software and standardizing interfaces, O-RAN enables multi-vendor interoperability and paves the way for a highly flexible, cloud-native deployment,.

### Key Architectural Components
The O-RAN architecture disaggregates the 3GPP gNodeB (gNB) into three primary functional blocks,:
*   **O-RU (Open Radio Unit):** Resides at the cell site, handling lower physical layer (PHY-low) processing and Radio Frequency (RF) transmissions,.
*   **O-DU (Open Distributed Unit):** Located at the edge, it executes time-sensitive operations including high-PHY, Medium Access Control (MAC), and Radio Link Control (RLC),.
*   **O-CU (Open Centralized Unit):** Hosted in regional or centralized clouds, it manages higher-layer functions (RRC, PDCP, SDAP) and is further split into Control Plane (O-CU-CP) and User Plane (O-CU-UP),.

### The RAN Intelligent Controllers (RIC)
O-RAN introduces native intelligence through hierarchical controllers:
*   **Non-Real-Time (Non-RT) RIC:** Operating at timescales >1 second within the Service Management and Orchestration (SMO) framework, it utilizes **rApps** for long-term policy generation, data analytics, and AI/ML model training,.
*   **Near-Real-Time (Near-RT) RIC:** Operating between 10 ms and 1 second at the network edge, it hosts **xApps** to enforce policies via the E2 interface for mobility management, traffic steering, and dynamic resource allocation,.

**Importance in 5G and 6G:** O-RAN is foundational for 6G networks, enabling AI-native integration, zero-touch orchestration, and extreme flexibility necessary to support diverse services like eMBB, URLLC, and mMTC,,. 

---

## 📚 Curated Literature Review

### O-RAN Architecture & Standards
| Title | Authors | Year | Key Contributions | Link |
| :--- | :--- | :--- | :--- | :--- |
| **Understanding O-RAN: Architecture, Interfaces, Algorithms, Security, and Research Challenges** | M. Polese, L. Bonati, et al. | 2023 | Provides a comprehensive foundational survey on O-RAN architecture, detailing standard interfaces (E2, A1, O1), algorithmic use cases, and open security challenges. | [IEEE CST](https://ieeexplore.ieee.org/document/10018260) |
| **Colosseum: The Open RAN Digital Twin** | M. Polese, L. Bonati, et al. | 2024 | Introduces a high-fidelity digital twin framework using hardware-in-the-loop channel emulation to safely train and evaluate O-RAN AI/ML solutions before physical deployment,. | [arXiv:2404.17317](https://arxiv.org/abs/2404.17317) |

### RIC & Intelligent Control (AI/ML in O-RAN)
| Title | Authors | Year | Key Contributions | Link |
| :--- | :--- | :--- | :--- | :--- |
| **ORION: Intent-Aware Orchestration in Open RAN for SLA-Driven Network Management** | G. S. Machado, et al. | 2026 | Proposes a hierarchical agent architecture leveraging Large Language Models (LLMs) to translate natural language intents into executable E2-level network policies. | [Preprint] |
| **ColO-RAN: Developing Machine Learning-Based xApps for Open RAN Closed-loop Control** | M. Polese, L. Bonati, et al. | 2023 | Presents the first publicly available large-scale O-RAN testing framework with SDRs-in-the-loop to accelerate Deep Reinforcement Learning (DRL) agent training for xApps,. | [IEEE TMC](https://ieeexplore.ieee.org/document/9814869) |

### xApps and rApps (Conflict Mitigation & Control)
| Title | Authors | Year | Key Contributions | Link |
| :--- | :--- | :--- | :--- | :--- |
| **Experimental evaluation of xApp Conflict Mitigation Framework in O-RAN** | A. Sultana, et al. | 2024 | Proposes and validates a comprehensive conflict mitigation technique for overlapping third-party xApps running concurrently on the Near-RT RIC using a hardware testbed,. | [ResearchGate](https://www.researchgate.net/) |
| **dApps: Enabling Real-Time AI-Based Open RAN Control** | A. Lacava, L. Bonati, et al. | 2025 | Introduces "dApps"—distributed microservices operating below 10ms directly on the DU/CU—to overcome the Near-RT RIC latency bottleneck for PHY/MAC operations,. | [arXiv:2501.16502](https://arxiv.org/abs/2501.16502) |

### Network Slicing & Resource Optimization
| Title | Authors | Year | Key Contributions | Link |
| :--- | :--- | :--- | :--- | :--- |
| **DORA: Dynamic O-RAN Resource Allocation for Multi-Slice 5G Networks** | J. Moore, A. S. Abdalla, et al. | 2025 | Benchmarks an adaptive physical resource block (PRB) allocation framework using Deep Reinforcement Learning (DRL) for dynamic slice-aware resource management,. | [arXiv:2509.07242](https://arxiv.org/abs/2509.07242) |
| **Enhancing AI Transparency: XRL-Based Resource Management and RAN Slicing** | S. Mhatre, F. Adelantado, et al. | 2024 | Proposes an Explainable RL (XRL) framework to demystify black-box DRL xApp decisions, improving transparency and trust in ORAN-based slicing tasks,. | [IEEE ICC](https://ieeexplore.ieee.org/) |

### Security in O-RAN
| Title | Authors | Year | Key Contributions | Link |
| :--- | :--- | :--- | :--- | :--- |
| **Implementing and Evaluating Security in O-RAN: Interfaces, Intelligence, and Platforms** | J. Groen, S. D'Oro, et al. | 2023 | Analyzes encryption overheads on the E2 interface and proposes strategies to secure open interfaces against adversarial attacks in virtualized environments,. | [arXiv:2304.11125](https://arxiv.org/abs/2304.11125) |

### Integration with 6G / Future Networks
| Title | Authors | Year | Key Contributions | Link |
| :--- | :--- | :--- | :--- | :--- |
| **Proactive AI-and-RAN Workload Orchestration in O-RAN Architectures for 6G Networks** | S. D. A. Shah, et al. | 2025 | Investigates dynamic resource allocation and Soft Actor-Critic (SAC) models to coordinate AI inference and RAN signal processing on shared edge infrastructure,. | [arXiv:2503.07420](https://arxiv.org/abs/2503.07420) |

---

## 🔗 Standards and Official Documentation

*   [**O-RAN Alliance Specifications**](https://www.o-ran.org/specifications): Official technical specifications defining the O-RAN architecture, including E2, A1, O1, and Open Fronthaul interfaces,.
*   [**3GPP Releases (Rel-15 to Rel-18)**](https://www.3gpp.org/): Provides the foundational NG-RAN standards (e.g., TS 38.401) defining the CU/DU split and 5G NR physical layer parameters that O-RAN builds upon.
*   [**ETSI O-RAN Transpositions**](https://www.etsi.org/): Endorsed European Telecommunications Standards Institute documents (e.g., ETSI TS 103 859 for Fronthaul Control) mapping O-RAN specs to global standards.
*   [**Telecom Infra Project (TIP) OpenRAN**](https://telecominfraproject.com/openran/): Deployment guidelines, blueprints, and badging certification matrices designed to accelerate the commercialization of open, disaggregated RAN,.

---

## 📊 Datasets and Testbeds

### Public Datasets
*   **Colosseum RF & Protocol Datasets:** Massive datasets encompassing complex radio frequency conditions (path loss, fading, interference) gathered from 128 SDRs used to pre-train DRL agents and xApps offline,,.
*   **ATCLL Network Performance Data:** Contains fine-grained metrics on latency, throughput, and link performance for empirical evaluation of ML-based mobility and handover management.

### O-RAN Testbeds and Simulators
*   [**Colosseum**](https://www.northeastern.edu/colosseum/): The world's largest wireless network emulator equipped with hardware-in-the-loop (128 USRP X310s), functioning as an O-RAN Digital Twin for safe AI/ML training,.
*   [**POWDER-RENEW**](https://powderwireless.net/): An outdoor, city-scale NSF PAWR testbed in Salt Lake City equipped with sub-6GHz and massive MIMO capabilities, highly cited for field-testing O-RAN orchestration,.
*   [**Arena**](https://ece.northeastern.edu/wineslab/arena.php): A 64-antenna SDR-based indoor grid testbed enabling sub-6 GHz spectrum research, frequently linked with Colosseum for digital-to-physical validations.
*   [**ns-O-RAN**](https://apps.nsnam.org/app/ns-o-ran/): An extension for the popular ns-3 discrete-event network simulator that interfaces with real-world O-RAN RICs, permitting large-scale software-only benchmarking,,.

---

## 🛠️ Open-Source Tools and Frameworks

*   [**O-RAN Software Community (OSC)**](https://o-ran-sc.org/): A collaboration between the O-RAN Alliance and the Linux Foundation. Provides reference implementations for the Near-RT RIC, Non-RT RIC, and E2/A1 interfaces,.
*   [**OpenAirInterface (OAI)**](https://openairinterface.org/): Provides a fully open-source, 3GPP-compliant 5G NR protocol stack (CU, DU, RU, and Core). Extensively used for developing dApps and virtualized network slicing solutions,.
*   [**srsRAN**](https://www.srsran.com/): A 4G/5G software radio suite built for general-purpose processors. Frequently wrapped by tools like SCOPE for data-collection and Near-RT RIC integration,,.
*   [**OpenRAN Gym / SCOPE**](https://openrangym.com/): A unified toolbox that provides a programmable environment and data collection APIs to prototype, train, and test xApps across emulated (Colosseum) and OTA (POWDER) platforms,,.
*   [**FlexRIC / µONOS-RIC**](https://opennetworking.org/sd-ran/): Lightweight, highly performant software development kits (SDKs) and Near-RT RIC implementations tailored for academic research and microservices deployment,,.

---

## 🧠 AI/ML in O-RAN

The disaggregation of the RAN transforms network control from heuristic-based static rules to an autonomous, intent-driven ecosystem powered by AI.
*   **Deep Reinforcement Learning (DRL):** Utilized extensively in **xApps** to tackle highly dynamic problems like multi-slice PRB allocation, interference mitigation, and physical layer scheduling. DRL agents interact with the environment via E2 feedback loops to continuously optimize long-term network KPIs without human intervention,,.
*   **Agentic AI & Large Language Models (LLMs):** Emerging frameworks (such as **ORION** and **ORAN-GUIDE**) embed LLMs within the Non-RT RIC to parse natural language operator intents, interpret semantic conditions, and guide lower-level DRL agents. This approach (often using Retrieval-Augmented Generation) resolves the poor generalization capability of traditional DRL in non-stationary traffic,,,.
*   **Distributed Apps (dApps):** To bypass the 10ms+ latency restriction of the E2 interface, extremely lightweight AI microservices (dApps) are embedded directly within the O-CU/O-DU to run sub-1ms predictive models for real-time PHY/MAC control (e.g., dynamic spectrum sharing),. 

---

## 📌 Key Research Gaps

Despite rapid advancements, several open problems hinder commercial, fully autonomous O-RAN deployments:
1.  **Latency in RIC Control Loops:** While the Near-RT RIC handles 10ms-1s loops, true real-time operations (sub-1ms) like beamforming and instantaneous MAC scheduling remain a challenge. The introduction of the E3 interface and dApps is promising but requires further standardization and hardware-acceleration profiling,,.
2.  **xApp/rApp Interoperability & Conflict Mitigation:** As multiple vendors deploy proprietary xApps targeting different objectives (e.g., an energy-saving xApp putting a cell to sleep vs. a load-balancing xApp steering users to it), real-time detection and resolution of policy conflicts remains an NP-hard challenge requiring robust orchestration frameworks,.
3.  **Data Scarcity & Generalization:** Training robust AI models requires massive, diverse, and labeled datasets capturing edge-case RF anomalies. The lack of standard, open-access operator telemetry data forces researchers to rely heavily on Digital Twins, presenting a sim-to-real transfer challenge,,.

---

## 📎 References 

 A. Sultana, F. Bashar, M. R. Chowdhury, and A. P. Da Silva, "A software-defined radio based o-ran platform for xapp conflict detection and mitigation," in *2024 IEEE Military Communications Conference (MILCOM)*, 2024, pp. 686–687.  
 M. Polese, L. Bonati, S. D'Oro, S. Basagni, and T. Melodia, "Understanding O-RAN: Architecture, Interfaces, Algorithms, Security, and Research Challenges," *IEEE Communications Surveys & Tutorials*, vol. 25, no. 2, pp. 1376-1411, 2023.  
 G. S. Machado, et al., "ORION: Intent-Aware Orchestration in Open RAN for SLA-Driven Network Management," *Preprint*, Mar 2026.  
 J. Moore, A. S. Abdalla, et al., "DORA: Dynamic O-RAN Resource Allocation for Multi-Slice 5G Networks," *arXiv preprint arXiv:2509.07242*, 2025.  
 A. Lacava, L. Bonati, et al., "dApps: Enabling Real-Time AI-Based Open RAN Control," *Computer Networks*, vol. 269, p. 111342, 2025.  
 M. Tsampazi, S. D'Oro, M. Polese, L. Bonati, G. Poitau, M. Healy, and T. Melodia, "PandORA: Automated Design and Comprehensive Evaluation of Deep Reinforcement Learning Agents for Open RAN," *IEEE Transactions on Mobile Computing*, 2024.  
 S. D. A. Shah, et al., "Proactive AI-and-RAN Workload Orchestration in O-RAN Architectures for 6G Networks," *arXiv preprint arXiv:2503.07420*, 2025.  
 S. Mhatre, F. Adelantado, K. Ramantas, and C. Verikoukis, "Enhancing AI Transparency: XRL-Based Resource Management and RAN Slicing," *IEEE International Conference on Communications*, 2024.  
 J. Groen, S. D'Oro, U. Demir, L. Bonati, M. Polese, T. Melodia, and K. Chowdhury, "Implementing and Evaluating Security in O-RAN: Interfaces, Intelligence, and Platforms," *arXiv preprint arXiv:2304.11125*, 2023.
