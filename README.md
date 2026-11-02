# Awesome-Endpoint-Detection-Response-EDR

# Awesome-Endpoint-Detection-Response-EDR

**Top Endpoint Detection Response EDR (Opensource) 🌟 Star if you like it! 🌟**



**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on Runtime Telemetry, Behavioral Detection, Automated Response & Self-Hosted Endpoint Security*

**Last updated: November 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Endpoint Detection & Response (EDR)**. These tools enable security teams to monitor endpoints for malicious behavior, investigate incidents, and respond to threats in real time—from fully managed enterprise platforms with AI-driven detection and managed hunting to open-source frameworks that give organizations control over their telemetry and response logic.



**Examples** include CrowdStrike Falcon Insight, SentinelOne Singularity Complete, Microsoft Defender for Endpoint, Palo Alto Cortex XDR, Carbon Black EDR, Cybereason, Trend Micro Vision One, Trellix EDR, Sophos EDR, and Huntress (the category leaders in commercial space).



**Open-source emphasis**: This section is expanded with every relevant project for self-hosted endpoint detection, behavioral monitoring, and open response infrastructure. **Critical note**: True open-source EDR is a crowded but fragmented space—**Wazuh** is the most complete SIEM/EDR hybrid, **Velociraptor** dominates DFIR and threat hunting at scale, and **OpenEDR** offers a dedicated EDR codebase from Xcitium. No open-source project matches CrowdStrike's kernel-level prevention or SentinelOne's autonomous response, but for detection and investigation, the options are production-proven.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **CrowdStrike Falcon Insight**

  **Cloud-native EDR** with kernel-level visibility and threat graph. **Pricing**: Quote-only; per-endpoint subscription. **Free tier**: Falcon Go free (100 devices) with limited EDR. **Best for**: enterprises wanting the most mature detection and threat intelligence—**trade-off**: premium pricing; ecosystem lock-in.



- **SentinelOne Singularity Complete**

  **Autonomous EDR** with AI-driven prevention and response. **Pricing**: **Singularity Complete from ~$179.99/endpoint/year** ; quote-based for enterprise. **Free tier**: None. **Best for**: organizations wanting autonomous response without human intervention—**trade-off**: agent resource usage; console complexity.



- **Microsoft Defender for Endpoint**

  **EDR integrated with Microsoft 365** and Defender XDR. **Pricing**: Included with M365 E5; standalone from ~$3/user/month. **Free tier**: Limited trial. **Best for**: Microsoft-centric organizations wanting native integration—**trade-off**: Microsoft ecosystem dependency; cross-platform support varies.



- **Palo Alto Cortex XDR**

  **Extended detection and response** combining endpoint, network, and cloud. **Pricing**: Quote-only. **Free tier**: None. **Best for**: Palo Alto customers wanting unified XDR—**trade-off**: requires Palo Alto ecosystem investment.



- **Carbon Black EDR** (Broadcom)

  **Enterprise EDR** with behavioral detection. **Pricing**: Quote-only. **Free tier**: None. **Best for**: enterprises with existing Broadcom relationships—**trade-off**: product roadmap uncertainty post-VMware acquisition.



- **Cybereason**

  **AI-driven EDR** with autonomous hunting. **Pricing**: Quote-only. **Free tier**: None. **Best for**: SOC teams wanting behavioral detection with MITRE ATT&CK coverage—**trade-off**: enterprise pricing; implementation complexity.



- **Trend Micro Vision One**

  **XDR platform** with endpoint, email, and cloud detection. **Pricing**: Quote-only. **Free tier**: None. **Best for**: enterprises wanting broad coverage from a single vendor.



- **Trellix EDR** (formerly McAfee/FireEye)

  **Enterprise EDR** with threat intelligence integration. **Pricing**: Quote-only. **Free tier**: None. **Best for**: enterprises with existing Trellix investments.



- **Sophos EDR**

  **EDR with managed threat response** option. **Pricing**: Quote-only; tiered by features. **Free tier**: Trial available. **Best for**: mid-market organizations wanting EDR with optional MDR.



- **Huntress**

  **Managed EDR for SMBs** with human threat hunters. **Pricing**: **Starting at ~$8/endpoint/month** (annual); quote-based for higher volumes. **Free tier**: None. **Best for**: SMBs wanting managed detection without enterprise complexity—**trade-off**: managed service; less customizable.



## Open-Source GitHub Projects



- **Wazuh**

  **Open Source Security Platform: Unified XDR and SIEM** (GPLv2) — **the most complete open-source SIEM/EDR hybrid**, with a large community and production deployments at scale . **Features**: **Host intrusion detection** (FIM, rootkit detection, log analysis); **vulnerability detection**; **security configuration assessment** (CIS, PCI DSS, HIPAA, NIST); **active response**—firewall-drop, host-deny, disable-account with configurable timeouts ; **MITRE ATT&CK mapping** for threat hunting; **container security** for Docker and Kubernetes. **Limitations**: **No real-time prevention**—detection is log-based, not kernel instrumentation; **requires significant technical expertise** to deploy and tune; **Indexer (OpenSearch) consumes substantial resources** . **Tech stack**: C, Python, OpenSearch. **Deploy**: Self-hosted (Docker, packages) or Wazuh Cloud. **Trade-off**: **Detection and response, not prevention**—it can block IPs and disable accounts but does not stop process execution like commercial EDR . **Best for**: organizations wanting a free, comprehensive SIEM/EDR with compliance mapping and active response—willing to invest in tuning and infrastructure.



- **Velociraptor**

  **Endpoint visibility and digital forensics platform** (Apache 2.0) — **the most powerful open-source tool for DFIR and threat hunting at scale**, with ~4,000 GitHub stars and active development . **Features**: **VQL (Velociraptor Query Language)** for interrogating endpoints—extremely powerful for custom hunts; **real-time monitoring** for process execution chains, network connections, and bash instrumentation; **hunts across thousands of endpoints** in minutes; **offline collectors** for field forensics; **low resource consumption** compared to full EDR agents. **Limitations**: **Not an EDR**—no continuous detection or prevention; **requires VQL knowledge**—high learning curve; **no native enterprise integrations** . **Tech stack**: Go. **Deploy**: Self-hosted (server + agents). **Trade-off**: **Hunting and forensics tool, not continuous EDR**—it excels at investigation but does not replace round-the-clock monitoring . **Best for**: DFIR teams and threat hunters wanting deep endpoint interrogation without commercial EDR licensing—especially for incident response and proactive hunting.



- **OpenEDR**

  **Open-source endpoint detection and response platform** (open source, Xcitium) — **the most dedicated open-source EDR codebase**, positioned as a full EDR capability . **Features**: **Analytic detection with MITRE ATT&CK visibility**; event correlation and root cause analysis of adversarial activity; real-time detection; **fully open source**—inspect, audit, and improve. **Limitations**: **Limited independent validation**—claims are vendor-reported; **smaller community** than Wazuh or Velociraptor. **Tech stack**: Per repository. **Deploy**: Self-hosted. **Trade-off**: **Early-stage ecosystem**—fewer integrations and less documentation than established alternatives. **Best for**: organizations wanting a dedicated open-source EDR codebase to evaluate or contribute to—willing to accept early-stage maturity.



### Additional Strong Open-Source Options



- **OSSEC** — Host-based intrusion detection system (HIDS) (open source). Foundational log-based detection, FIM, active response. **Note**: **Predecessor to Wazuh**—OSSEC is the original HIDS; Wazuh forked and expanded it. **Best for**: legacy deployments or minimal HIDS needs .

- **Warden** — Open-source EDR for Linux workstations (Rust). YARA scanning, ransomware detection, quarantine, hardened security model with pkexec authentication . **Note**: **Linux-only**; newer project with active security testing. **Best for**: Linux workstation protection with a security-first design .

- **Rustinel** — Cross-platform EDR runtime (Rust). ETW (Windows) and eBPF (Linux) telemetry, Sigma/YARA/IOC detection, ECS-compatible alerts . **Note**: **Early-stage** (~141 stars); less validation than Wazuh or Velociraptor. **Best for**: developers wanting a modern, Rust-based EDR foundation.

- **Vettaiyan** — Open-source EDR for Windows (active development). Real-time detection, response actions, telemetry collection . **Note**: **In progress**—not production-ready. **Best for**: contributors wanting to shape a new Windows EDR project.



**Frameworks for building custom systems**: Combine **Wazuh** for SIEM/EDR detection with **Velociraptor** for DFIR and hunting and **Sigma** for portable detection rules—creating a layered open-source endpoint security stack. **None of these match CrowdStrike's kernel-level prevention or SentinelOne's autonomous response**, but for detection and investigation, the options are production-capable.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, license (for open-source), and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- EDR platforms handling endpoint telemetry must comply with data protection regulations (GDPR, CCPA, etc.) and implement appropriate access controls for security data.

- **The "prevention-focused EDR" vs. "detection/SIEM hybrid" vs. "DFIR/hunting tool" distinction is critical.** **CrowdStrike, SentinelOne, Microsoft Defender, and Cortex XDR** are **prevention-focused EDR**—they block threats at the kernel level and provide autonomous response . **Wazuh** is a **detection/SIEM hybrid**—it detects and responds but does not prevent process execution . **Velociraptor** is a **DFIR/hunting tool**—it excels at investigation but lacks continuous detection . **Choose based on whether you need prevention, detection, or investigation.**

- **Wazuh is the most complete open-source SIEM/EDR**, with compliance mapping, active response, and a large community . **The trade-off**: no real-time prevention; requires significant tuning and infrastructure.

- **Velociraptor is unmatched for DFIR at scale**—VQL enables custom hunts across thousands of endpoints in minutes . **The trade-off**: it is not an EDR—no continuous monitoring or prevention. **Pair it with Wazuh for detection.**

- **OpenEDR is the most dedicated open-source EDR attempt**, but independent validation is limited . **For organizations wanting a full EDR codebase, it is worth evaluating; for proven detection, Wazuh is safer.**

- **Huntress is the most accessible managed EDR for SMBs** at ~$8/endpoint/month with human threat hunters . **For organizations without SOC staff, it is a pragmatic choice.**

- Self-hosted open-source solutions require proper infrastructure (servers for Wazuh, agents on endpoints), security hardening, and ongoing maintenance. **Endpoint agents have deep system visibility**—ensure your deployment meets your organization's security and privacy requirements before installing on production endpoints.



---



**Made for SOC teams, security engineers, and organizations building transparent endpoint security solutions.**

Let's make Endpoint Detection & Response more open, data-driven, and threat-aware.
