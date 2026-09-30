## Abstract

Large language model agents are increasingly deployed in enterprise environments to execute tasks through planning, tool use, memory, and interaction with local knowledge and business workflows. During operation, these agents accumulate valuable execution trajectories, tool-use records, and success or failure feedback. However, such experience is often distributed across isolated private environments and cannot be directly shared because it may contain sensitive user data, proprietary knowledge, business rules, and operational traces. Federated learning offers a natural foundation for privacy-preserving collaboration, but conventional parameter aggregation is insufficient for agent systems whose capabilities depend on policies, memory, tools, rewards, and local execution contexts. In this paper, we formulate Federated Agent Optimization (FAO), a problem setting in which multiple agents collaboratively improve through controlled information exchange while keeping raw data, complete trajectories, and private local knowledge decentralized. We define FAO around three core objectives: improving local task utility, reducing privacy leakage risk, and controlling communication and system overhead. We further clarify the sharing boundaries of federated agent systems and organize possible collaborative optimization mechanisms across policies, memory, tool use, rewards, skills, and knowledge. Finally, we discuss key challenges and research directions for building practical, privacy-preserving, and communication-efficient federated agent systems.

---


## Core Objectives

| Local utility | Privacy | Efficiency |
|:---:|:---:|:---:|
| Improve each agent on its own task distribution | Limit leakage from shared updates | Control communication and system overhead |

FAO treats these goals as a joint optimization problem rather than optimizing agent performance in isolation.

## Optimization Space

An agent is represented through five interacting components:

| Component | What can be collaboratively optimized |
|---|---|
| **Policy** | Model weights, adapters, prompts, and workflow graphs |
| **Memory** | Reusable experience, insights, and retrieval knowledge |
| **Tools** | Tool descriptions, routing knowledge, compositions, and failure patterns |
| **Reward** | Evaluators, preference signals, rubrics, and feedback models |
| **Structured knowledge** | Ontologies, rules, and reusable skills |

Shared artifacts can take the form of **experience, skills, rules, rewards, or ontologies**. Each client validates and adapts these artifacts locally instead of exposing its underlying records.


## Key Takeaways

- **Beyond parameter aggregation:** federating an agent requires coordinating more than the underlying language model.
- **Typed and controlled sharing:** only explicitly defined update blocks leave each client; raw private data stays local.
- **Personalized collaboration:** aggregated knowledge can be adapted to each client's tasks, tools, and environment.
- **Measurable trade-offs:** performance gains must be evaluated together with privacy leakage and communication cost.

---

<div align="center">
  <sub>Federated agents that learn together while keeping private experience local.</sub>
</div>
