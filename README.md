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

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## Sector Overview & Market Dynamics

The global Endpoint Detection and Response (EDR) market is valued between **$5.1B and $7.2B** (projected to reach **$18B to $45B+** by the early 2030s at a 22–26% CAGR). The market is **moderately concentrated** at the top tier—dominated by an oligopoly of enterprise platform heavyweights like Microsoft, CrowdStrike, SentinelOne, and Palo Alto Networks driving vendor consolidation—while remaining **fragmented** across specialized Managed Detection and Response (MDR) providers and regional compliance niches.

## SaaS/Hosted Platforms

| Product | Company Valuation / Revenue | Starting Pricing | Free Tier / Trial Limits | Description & Key Trade-offs |
| :--- | :--- | :--- | :--- | :--- |
| **Microsoft Defender for Endpoint** | **~$3.8T Market Cap** / ~$281.7B FY25 Revenue | **$3.00/user/month** (Plan 1 standalone, annual commit; Plan 2 at $5.20/user/month; up to 5 concurrent devices/user) | **30-day free trial** (up to 25 test licenses across Windows, macOS, Linux with full Plan 2 EDR/AIR features) | Cloud-native EDR integrated natively into Microsoft 365 and Defender XDR. Excellent integration; trade-off is Microsoft ecosystem lock-in and varying cross-OS telemetry parity. |
| **Carbon Black EDR** (Broadcom) | **~$1.3T Market Cap** / ~$63.9B FY25 Revenue | **~$50.00/endpoint/year** (baseline list through authorized enterprise partners; ~$4.15/endpoint/month) | **14 to 30-day proof-of-concept (POC)** (custom provisioned evaluation via partner/sales rep; no automated self-service free tier) | Enterprise behavioral detection and continuous monitoring. Best for Broadcom ecosystem users; trade-off is licensing model complexity post-VMware transition. |
| **Palo Alto Cortex XDR** | **~$120B Market Cap** / ~$9.2B FY25 Revenue | **~$7.00/endpoint/month** (baseline Cortex XDR Prevent/Pro software licensing via certified partner quote) | **14 to 30-day proof-of-concept (POC)** (gated evaluation coordinated via sales engineering; no automated instant free trial) | Extended detection and response marrying endpoint telemetry with network firewalls and cloud events. Trade-off is heavy reliance on Palo Alto infrastructure investment. |
| **CrowdStrike Falcon Insight** | **~$80B Market Cap** / ~$3.95B FY25 Revenue | **$59.99/device/year** (~$4.99/month for Falcon Go entry tier; Falcon Pro starts at ~$95.00/device/year) | **15-day free trial** (Falcon Prevents/Go features on up to 100 endpoints, zero credit card required; no permanent free tier) | Cloud-native EDR with Threat Graph and lightweight kernel agent. Industry-leading intelligence; trade-off is premium pricing and enterprise contract minimums. |
| **SentinelOne Singularity Complete** | **~$6.5B Market Cap** / ~$800M Revenue | **$69.99/endpoint/year** (Singularity Core AV; full Singularity Complete EDR starts at ~$179.99/endpoint/year) | **14 to 30-day proof-of-concept (POC)** (partner/sales-assisted trial with full automated remediation; no instant self-service free tier) | Autonomous AI-driven EDR with Storyline tracking and one-click rollback. Trade-off is local agent resource footprint during high-volume process scanning. |
| **Trend Micro Vision One** | **~$6.0B Market Cap** / ~$1.7B Revenue | **~$25.00/endpoint/year** (core endpoint security/EDR subscription component pricing; ~$2.08/month) | **30-day free trial** (unlimited access to Vision One console and threat hunting modules during evaluation window) | Broad detection across endpoints, email, and cloud workloads. Best for all-in-one vendor environments; trade-off is suite complexity. |
| **Sophos EDR** (Intercept X) | **~$3.9B Enterprise Value** / ~$1.2B Revenue | **~$35.00/user/year** (Intercept X Advanced starting price through authorized MSP partners; ~$2.90/user/month) | **30-day free trial** (fully functional Sophos Central evaluation with unlimited device onboarding during trial) | EDR combined with deep learning anti-exploit tech and optional 24/7 MDR. Trade-off is centralized policy management overhead for large enterprise setups. |
| **Huntress** | **$1.55B Valuation** / ~$150M+ Revenue ($250M ARR run-rate) | **$8.00/endpoint/month** (annual agreement; ~$96.00/endpoint/year with bundled 24/7 human SOC) | **14-day free trial** (unlimited endpoint agents deployed with active human threat-hunting and remediation support) | Managed EDR tailored for SMBs and MSPs with human-backed investigation and isolation. Trade-off is less direct low-level detection rule customization. |
| **Trellix EDR** | **~$1.05B Revenue** (PE-backed STG/Advent) | **~$45.00/endpoint/year** (baseline Endpoint Security / EDR license via partner quote) | **60-day free trial** (official Endpoint Security ePO evaluation provisioned for up to 5 trial nodes via sales) | Enterprise EDR integrating threat intelligence from legacy FireEye and McAfee engines. Trade-off is legacy console migration complexity. |
| **Cybereason** | **~$850M Valuation** (Acquired by LevelBlue) / ~$180M Revenue | **~$40.00/endpoint/year** (entry enterprise tier via authorized distribution quote; ~$3.33/endpoint/month) | **14 to 30-day proof-of-concept (POC)** (custom enterprise evaluation environment provisioned via sales rep) | AI-guided MalOp cross-machine correlation and MITRE ATT&CK visibility. Trade-off is enterprise pricing floor and implementation overhead. |

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
