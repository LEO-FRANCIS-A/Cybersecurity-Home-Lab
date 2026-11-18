# 👋 Welcome to Experiment 02!

# 🔐 SSH Remote Access, Unauthorized Access & Incident Investigation

> **One remote connection. One suspicious activity. One investigation. Can you uncover what happened and secure the system?**

![Domain](https://img.shields.io/badge/Domain-Network%20%7C%20Host%20Security-blue)
![Difficulty](https://img.shields.io/badge/Difficulty-Beginner%20to%20Intermediate-orange)
![Environment](https://img.shields.io/badge/Environment-Kali%20Linux%20%7C%20Windows%2011-informational)
![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)

---

## 🎯 The Mission

What happens when an attacker gains remote access to a Windows machine through SSH?

How can a defender identify the source of the connection, investigate suspicious activities, reconstruct what happened, and prevent similar incidents?

In this experiment, we'll simulate a series of security events using Kali Linux and Windows 11 virtual machines.

We'll establish legitimate remote access, simulate suspicious activity, investigate endpoint and network evidence, and implement defensive controls.

**Our objective is not simply to gain remote access. It's to understand the security implications of that access and learn how to investigate and defend against its misuse.**

---

## 🕵️ The Investigation

We'll follow an incident-driven approach:

- Establish legitimate SSH access.
- Create a baseline of normal system activity.
- Simulate suspicious remote operations.
- Investigate Windows authentication and filesystem evidence.
- Analyze SSH traffic using Wireshark.
- Examine failed authentication attempts.
- Implement defensive security controls.
- Validate our defenses through retesting.

---

## 🖥️ Lab Architecture

| Component | Configuration |
|---|---|
| Attacker Machine | Kali Linux |
| Target Machine | Windows 11 |
| Virtualization | Oracle VirtualBox |
| Primary Protocol | SSH |
| Transport Protocol | TCP |
| SSH Port | `22` |
| Network | Host-Only + NAT |
| Lab Subnet | `192.168.56.0/24` |

### Network Communication

```text
       KALI LINUX
    192.168.56.102
     (SSH Client)
           |
           |
       SSH / TCP 22
           |
           |
     WINDOWS 11
    192.168.56.101
     (SSH Server)
```

The Host-Only network will be used for isolated lab communication. NAT will provide temporary internet access when required for software installation.

---

## 🧪 Scenario Navigation

The experiment is divided into eight scenarios. Each scenario focuses on a different stage of the investigation.

| Scenario | Investigation | Status |
|---|---|---|
| 01 | [Establishing the SSH Environment](Scenario-01-SSH-Environment/) | 🟡 In Progress |
| 02 | [Normal Activity & Monitoring Baseline](Scenario-02-Normal-Activity-Baseline/) | ⬜ Not Started |
| 03 | [Simulating Suspicious Remote Activity](Scenario-03-Suspicious-Remote-Activity/) | ⬜ Not Started |
| 04 | [Windows Endpoint Investigation](Scenario-04-Windows-Investigation/) | ⬜ Not Started |
| 05 | [Network Traffic Investigation — Wireshark](Scenario-05-Wireshark-Traffic-Analysis/) | ⬜ Not Started |
| 06 | [Failed Authentication Attempts](Scenario-06-Failed-Authentication/) | ⬜ Not Started |
| 07 | [Defensive Hardening](Scenario-07-Defensive-Hardening/) | ⬜ Not Started |
| 08 | [Validation & Retesting](Scenario-08-Validation/) | ⬜ Not Started |

---

## 🛠️ Tools & Technologies

| Tool / Technology | Purpose |
|---|---|
| Kali Linux | Controlled attack simulation |
| Windows OpenSSH | Remote access service |
| Nmap | Network and service discovery |
| Wireshark | Network traffic analysis |
| PowerShell | Windows administration and investigation |
| Event Viewer | Windows event investigation |
| Windows Defender Firewall | Network access control |
| Windows Filesystem | File activity investigation |

Additional tools may be introduced as the investigation progresses.

---

## 🔍 Areas of Learning

- SSH architecture and remote authentication.
- TCP connection establishment.
- Windows user accounts and access permissions.
- Windows OpenSSH Server configuration.
- Firewall configuration and network restrictions.
- Authentication monitoring and event logging.
- Filesystem investigation and evidence collection.
- Network traffic analysis and encrypted communication.
- Failed authentication and password guessing.
- Incident timeline reconstruction.
- Least privilege and defensive hardening.
- Security validation and retesting.

---

## 🛡️ Lab Safety

All experiments are performed within an isolated VirtualBox environment.

- Only personally controlled virtual machines are used.
- Dedicated lab accounts and fictional dummy files are used.
- Authentication testing is limited and controlled.
- SSH is not intentionally exposed to the public internet.
- VM snapshots are taken before significant configuration changes.

---

## 📈 Experiment Progress

**Current Stage:** Scenario 01 — Establishing the SSH Environment.

Each scenario will have its own README documenting the objective, activities performed, observations, evidence, technical findings, and conclusions.

The final experiment report will bring together the findings from all scenarios and reconstruct the simulated incident.

---

## 🏁 Final Objective

By the end of this experiment, we aim to understand not only how remote access works, but also how suspicious remote activity can be detected, investigated, and prevented.

**Connect. Investigate. Detect. Defend. Verify.**

---

*Cybersecurity Home Lab | Learning Defensive Security Through Hands-On Experiments.*
