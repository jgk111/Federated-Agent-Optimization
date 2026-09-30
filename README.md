# Federated Agent Optimization

**Qiang Yang¹ · Zhiqiang Kou¹ · Xueyi Zhang³ · Dongdong Wu⁴ · Hanlin Gu⁵ · Jing Guo⁶ · Di Jiang¹ · Qian Xu²**

¹ The Hong Kong Polytechnic University &nbsp;·&nbsp; ² Tengen AI &nbsp;·&nbsp; ³ National University of Singapore  
⁴ The University of Tokyo &nbsp;·&nbsp; ⁵ E Fund Management Co., Ltd. &nbsp;·&nbsp; ⁶ Yunnan University

## Abstract

Large language model agents are increasingly deployed in enterprise environments to execute tasks through planning, tool use, memory, and interaction with local knowledge and business workflows. During operation, these agents accumulate valuable execution trajectories, tool-use records, and success or failure feedback. However, such experience is often distributed across isolated private environments and cannot be directly shared because it may contain sensitive user data, proprietary knowledge, business rules, and operational traces. Federated learning offers a natural foundation for privacy-preserving collaboration, but conventional parameter aggregation is insufficient for agent systems whose capabilities depend on policies, memory, tools, rewards, and local execution contexts. In this paper, we formulate Federated Agent Optimization (FAO), a problem setting in which multiple agents collaboratively improve through controlled information exchange while keeping raw data, complete trajectories, and private local knowledge decentralized. We define FAO around three core objectives: improving local task utility, reducing privacy leakage risk, and controlling communication and system overhead. We further clarify the sharing boundaries of federated agent systems and organize possible collaborative optimization mechanisms across policies, memory, tool use, rewards, skills, and knowledge. Finally, we discuss key challenges and research directions for building practical, privacy-preserving, and communication-efficient federated agent systems.
