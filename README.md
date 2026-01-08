# VeloroLABS

Building the decentralized deployment ecosystem for the edge.

VeloroLABS creates high-performance tools for IoT, cyberdecks, and distributed systems. We combine open-source agents with enterprise-grade orchestration.

## Our Ecosystem

### ⚡ [Spark](https://github.com/VeloroLABS/spark) (Open Source)
**The Deployment Agent & CLI**
A completely free and open-source toolchain to replace Ansible/Docker on edge devices.
- **Universal:** Works with GitHub, GitLab, and Forge.
- **Lightweight:** Single Rust binary, zero dependencies.
- **Gateway:** Built-in reverse proxy for instant web hosting.
- **License:** MIT

### 🛡️ Forge (Platform)
**Advanced Git & Orchestration Server**
Our Open-Core solution for secure, high-performance source code management and deployment coordination.
- **Smart HTTP:** High-performance Git server implementation.
- **Security:** Advanced authentication and repository protection.
- **Integration:** Deep native integration with Spark agents.
- *Enterprise / Proprietary*

## Architecture

```mermaid
graph LR
    User[Developer] -->|git push| Forge[Forge Platform]
    User -->|spark deploy| Daemon[Spark Agent]
    
    subgraph Open Source
    Daemon -->|run| App[Application]
    end
    
    subgraph Enterprise Core
    Forge -->|secure delivery| Daemon
    end
