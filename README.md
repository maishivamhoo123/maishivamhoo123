# 👋 Hi, I'm Shivam Kumar

**Software Developer | HAMi (CNCF) Community Member | Go Enthusiast**

I'm a backend-focused software developer driven by problem solving and systems reliability. I specialize in building robust backend systems in **Go** and contributing to world-class open-source infrastructure — with **50+ merged PRs** across projects like Google, HAMi (CNCF), and the wider Kubernetes ecosystem. I currently serve as a **Community Member** on HAMi's Community Leadership team.

---

## 💼 Experience

** Community Member — [HAMi (CNCF)](https://github.com/Project-HAMi/HAMi)**
*Remote · February 2026 – Present*
- Drive feature development and code reviews as part of HAMi's Community Leadership team, helping steer technical discussions and community initiatives.
- Optimized distributed node-lock scalability with exponential backoff and resolved a Prometheus metrics cardinality explosion to keep AI workloads highly available.
- Hardened Kubernetes scheduler API routes against DoS and fixed kernel-level edge cases in NVIDIA hardware health checks.
- Built a full GPU scheduling test environment (KIND cluster + nvml-mock on WSL2/Linux) that needs no physical GPU hardware; represented HAMi at the KubeCon India booth.

**Open Source Contributor — Google (go-github), Apache, Kubernetes ecosystem**
*Remote · March 2024 – Present*
- 50+ merged pull requests resolving backend and infrastructure issues across high-impact repositories.

**Software Developer Intern — Jijiwisha Society**
*Kanpur, UP · June 2024 – August 2024*
- Built a full-stack MERN website with stakeholders, growing NGO visibility and engagement by 25%.

---

## 🛠️ Proof of Work (Open Source Contributions)

### 🛡️ Security & System Reliability
* **Project-HAMi ([#1620](https://github.com/Project-HAMi/HAMi/pull/1620))**: Implemented DoS protection by introducing `io.LimitReader` to scheduler routes, preventing resource exhaustion from oversized payloads.
* **Project-HAMi ([#1663](https://github.com/Project-HAMi/HAMi/pull/1663))**: Optimized nodelock scalability with exponential backoff and listers, improving high availability for AI workloads under heavy concurrent load.
* **HAMi-core ([#168](https://github.com/Project-HAMi/HAMi-core/pull/168))**: Added retry logic for `nvmlInit` so a transient GPU init failure no longer strands a process in a permanent failure state.
* **Project-HAMi ([#1810](https://github.com/Project-HAMi/HAMi/pull/1810))**: Fixed Kernel 6.17 handshake edge cases in NVIDIA hardware health checks.
* **HAMi-DRA ([#25](https://github.com/Project-HAMi/HAMi-DRA/pull/25))**: Added `OwnerReferences` to `ResourceClaims` so orphaned claims are correctly garbage-collected.
* **Gogs ([#8091](https://github.com/gogs/gogs/pull/8091))**: Engineered safety checks to ensure data integrity by verifying directory existence before repository initialization.
* **Syncthing ([#10541](https://github.com/syncthing/syncthing/pull/10541))**: Enhanced system transparency by ensuring full device ID logging during discovery server startup.

### 🚀 Core Logic & Feature Engineering
* **Google ([go-github #3891](https://github.com/google/go-github/pull/3891))**: Implemented `omitzero` support for `BypassActors`, leveraging new Go 1.24 features for more efficient API data handling.
* **Google ([go-github #3944](https://github.com/google/go-github/pull/3944))**: Added support for organization artifact metadata APIs, including deployment/storage record endpoints with full test coverage.
* **Google ([go-github #4288](https://github.com/google/go-github/pull/4288))**: Added enterprise billing usage endpoints and response types.
* **Google ([go-github #4241](https://github.com/google/go-github/pull/4241))**: Added support for getting Copilot cloud agent configuration.
* **Apache ([answer #1464](https://github.com/apache/answer/pull/1464))**: Added support for `.env` configurations to allow for dynamic, environment-specific application setups.
* **Gogs ([#8089](https://github.com/gogs/gogs/pull/8089))**: Developed custom post-sign-out redirection logic to streamline user authentication workflows.
* **Syncthing ([#10527](https://github.com/syncthing/syncthing/pull/10527))**: Standardized version output logic in the discovery server to improve CLI consistency.

### 🐛 Optimization & User Experience
* **Project-HAMi ([#1628](https://github.com/Project-HAMi/HAMi/pull/1628))**: Fixed Prometheus metric cardinality explosion by optimizing container memory descriptor labels, reducing excessive time-series generation and improving monitoring stability.
* **ChainSafe ([lodestar #8298](https://github.com/ChainSafe/lodestar/pull/8298))**: Optimized Ethereum consensus client logging for higher performance and cleaner telemetry data.
* **Termix-SSH ([#182](https://github.com/Termix-SSH/Termix/pull/182))**: Integrated dynamic versioning for CLI menus using environment variables.
* **OHC Network ([#12197](https://github.com/ohcnetwork/care_fe/pull/12197))**: Resolved critical responsiveness issues in healthcare clinical modules.
* **Memos ([#5323](https://github.com/usememos/memos/pull/5323))**: Enhanced UI accessibility and dark-mode contrast for improved user experience.
* **KAI-Scheduler ([#1854](https://github.com/kai-scheduler/KAI-Scheduler/pull/1854))**: Fixed CI upgrade-version resolution by checking OCI chart availability.

### 📚 Documentation & Community
* **Project-HAMi ([#2064](https://github.com/Project-HAMi/HAMi/pull/2064))**: Authored the design document for init-container GPU resource accounting.
* **HAMi website ([#610](https://github.com/Project-HAMi/website/pull/610))**: Added the Lab 10 GPU topology-aware scheduling tutorial, resolving a version-skew issue found along the way.
* Reviewed 5+ pull requests as part of HAMi's feature working group and regularly attend community meetings.

---

## Projects

# ⚖️ DSA-Powered HTTP Load Balancer (Go)
*Dec 2025*

A high-performance Layer 7 HTTP Load Balancer built in Go.
Implements a Min-Heap (Priority Queue) to efficiently route traffic to the least-loaded backend server.

## 🚀 Features
- Least Connections algorithm using Min-Heap
- O(1) best-server lookup (heap root)
- O(log N) rebalancing on connection updates
- Concurrency-safe with sync.RWMutex
- Active health checking (self-healing nodes)
- Reverse proxy using net/http/httputil
- Config-driven backend registration
- Real-time status dashboard

## 🧠 Core Idea
Instead of scanning all servers (O(N)), the load balancer maintains a Min-Heap
where priority = active connections.

- Peek root → Best server (O(1))
- Increment/Decrement connections → heap.Fix() (O(log N))

This ensures scalable traffic distribution as backend pool grows.

# 🤖 Microservices AIOps Platform
*Feb 2026*

An end-to-end AIOps platform built with microservices architecture.
Detects anomalies, predicts incidents, and performs automated root cause analysis (RCA) in real time.

## 🏗 Architecture
Services:
- API Gateway (Go)
- Auth Service (Go)
- Worker Service (Go)
- Anomaly Detector (Python - Isolation Forest)
- Incident Predictor (XGBoost)
- RCA Service
- Prometheus + Grafana + Loki stack

All services run via Docker Compose.

## ✨ Features
- Real-time anomaly detection (Isolation Forest)
- Incident prediction using XGBoost
- Automated Root Cause Analysis (log + metric correlation)
- Prometheus metrics scraping
- Centralized logging via Loki
- Grafana dashboards
- Synthetic traffic & chaos simulation

---

## 🏆 Achievements
* 🥈 **Runner-up, ABB Accelerator Hackathon 2026** — ranked 2nd among 14,000+ participants nationwide.
* 🥇 **Winner, Open Source Hackathon 2025** — among 500+ participants.
* 💻 **650+ DSA problems solved**; ranked **379th in LeetCode Weekly Contests (top 0.9%)** with a peak rating of **1800+**.
* 🌐 Website developer for TEDx NIT Andhra Pradesh (2024, 2025), Techkriya (2024), and TechFest (2024).

---

## 🎓 Education

**National Institute of Technology, Andhra Pradesh**
B.Tech, Mechanical Engineering · June 2023 – April 2027
Relevant coursework: Data Structures & Algorithms, Object-Oriented Programming, Artificial Intelligence, Distributed Systems.

---

## 🧰 Tech Stack
* **Languages:** Go (Golang), Java, Python, JavaScript, SQL
* **Frameworks & Other:** React, CUDA
* **Cloud & DevOps:** Docker, Kubernetes, AWS (EC2, IAM, S3, VPC, CloudWatch), Git, GitHub, Linux/Bash, WSL

---

## 🤝 Connect with me
* **GitHub:** [@maishivamhoo123](https://github.com/maishivamhoo123)
* **LinkedIn:** [Shivam Kumar](https://www.linkedin.com/in/shivam-kumar-559417290/)
* **Email:** [kumarshivam45226@gmail.com](mailto:kumarshivam45226@gmail.com)

---
*I am currently seeking a **Software Engineering Internship** (Backend/DevOps/Go). If you like my work, let's talk!*
