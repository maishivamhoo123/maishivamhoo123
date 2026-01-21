# 👋 Hi, I’m Shivam Kumar

**Software Developer | Open Source Contributor | Go Enthusiast**

I am a software developer driven by **Problem Solving** and systems reliability. I specialize in building robust backend tools using **Go** and contributing to world-class open-source infrastructure.

---

### 🛠️ Proof of Work (Open Source Contributions)

#### 🚀 Core Logic & Features (Golang focus)
* **Google ([go-github #3891](https://github.com/google/go-github/pull/3891))**: Implemented `omitzero` support for `BypassActors`. Demonstrated expertise in Go 1.24+ features and efficient API data handling.
* **Gogs ([gogs #8091](https://github.com/gogs/gogs/pull/8091))**: **Data Integrity:** Engineered safety checks to prevent data loss by verifying directory existence before repository initialization.
* **Apache ([answer #1464](https://github.com/apache/answer/pull/1464))**: Added optional `.env` support for dynamic, environment-specific configurations in enterprise applications.
* **Gogs ([gogs #8089](https://github.com/gogs/gogs/pull/8089))**: Developed custom post-sign-out redirection logic to improve authentication workflows.

#### 🐛 Bug Fixes & Optimization
* **ChainSafe ([lodestar #8298](https://github.com/ChainSafe/lodestar/pull/8298))**: Optimized Ethereum consensus client logging using `prettyPrintIndices` for higher performance and cleaner telemetry.
* **Termix-SSH ([Termix #182](https://github.com/Termix-SSH/Termix/pull/182))**: Integrated dynamic versioning for CLI profile menus using environment variables.
* **OHC Network ([care_fe #12197](https://github.com/ohcnetwork/care_fe/pull/12197))**: Resolved critical mobile responsiveness issues for clinical healthcare modules.
* **Memos ([memos #5323](https://github.com/usememos/memos/pull/5323))**: Enhanced accessibility and dark-mode contrast for better UX.

---

### 🧰 Tech Stack
* **Languages:** Go (Golang), TypeScript, JavaScript, C++
* **Tools:** Git, Docker, Kubernetes, Linux/Bash, PostgreSQL
* **Interests:** Distributed Systems, Cloud-Native Tooling, API Design


  ---
  ### ⚖️ [Go-LoadBalancer](https://github.com/maishivamhoo123/loadBalancer) | Go, Networking, Concurrency
**A production-ready Layer 7 Load Balancer with dynamic failover and health monitoring.**

* **The Problem:** Single points of failure in backend architectures lead to downtime and poor scalability.
* **My Solution:** Developed a Go-based proxy that distributes incoming HTTP traffic across a pool of backends using a **Round-Robin** algorithm.
* **Key Features:**
    * **Active Health Probing:** A background goroutine periodically "pings" backends; if a node fails, it is automatically removed from the rotation to prevent "502 Bad Gateway" errors.
    * **Thread-Safe State:** Leveraged `sync.RWMutex` to manage the server pool, ensuring high-performance reads for routing while maintaining data integrity during updates.
    * **Reverse Proxy Integration:** Utilized `httputil.ReverseProxy` to manage director functions and header propagation.
* **Impact:** Demonstrates deep understanding of Go's `net/http` package and concurrency primitives (`sync`, `atomic`).


### 🤝 Connect with me
* **GitHub:** [@maishivamhoo123](https://github.com/maishivamhoo123)
* **LinkedIn:**[ [Shivam Kumar](https://www.linkedin.com/in/shivam-kumar-559417290/)

---
*I am currently seeking a **Software Engineering Internship** (Backend/DevOps/Go). If you like my work, let's talk!*
