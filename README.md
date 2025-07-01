# Threat Simulation & SIEM Detection Pipeline (TS-SDP)



**Threat Simulation & SIEM Detection Pipeline (TS-SDP)** is an end-to-end environment that simulates real-world cyberattacks and detects them using a full ELK Stack-based SIEM setup. It empowers security researchers, SOC analysts, and students to build, observe, and understand log telemetry and detection logic.

---

## 🧠 Project Architecture

![image](https://github.com/user-attachments/assets/a071e85e-6f77-4dd0-9d87-c1060f2757ed)

![image](https://github.com/user-attachments/assets/db9a56e2-aa2c-4705-8dc9-275652f8e175)

The architecture includes:

- **Simulated Attacks**: SSH brute-force (via Shodan), credential misuse (e.g., Mimikatz).
- **Custom Python Tooling**: Shodan API + Paramiko brute-forcer for SSH.
- **Telemetry Sources**: Sysmon, Suricata, Filebeat on Linux/Windows.
- **Detection & Parsing**: Logstash with custom Grok rules.
- **SIEM Dashboard**: Kibana for attack visualization.

---

## ✨ Capabilities

- 🔐 Simulate real-world threat behaviors using scripted tools  
- 📦 Aggregate 10K+ log events/hour using Filebeat  
- 🎯 Detect brute-force, misuse, and suspicious processes via Logstash  
- 📊 Visualize activity in interactive Kibana dashboards  
- 🛠 Tune detection thresholds and minimize false positives  

---

## 🧰 Tools & Stack

| Layer            | Tooling/Tech                                     |
|------------------|--------------------------------------------------|
| Attack Simulation| Python, Paramiko, Shodan API                     |
| Logging Agents   | Filebeat, Sysmon, Suricata                       |
| Ingestion Engine | Logstash with Grok filters                       |
| Storage          | Elasticsearch                                    |
| Visualization    | Kibana                                           |
| OS Platforms     | Ubuntu, Kali, Windows 10                         |

---

## 📁 Repo Structure

Threat_Simulation_SIEM_Pipeline/
├── src/ssh_bruteforce_tool/ # Python tool for SSH attacks
├── config/logstash/ # Logstash pipeline configs
├── data/sample_logs/ # Simulated log files
├── dashboards/kibana_exports/ # Kibana .ndjson exports
├── docs/ # Architecture diagrams, SOPs
└── README.md


---

## 🚀 Usage Scenarios

- ✅ SIEM Lab Projects  
- ✅ Threat Simulation & Detection Testing  
- ✅ SOC Analyst Skill Building  
- ✅ Red vs Blue Team Training  
- ✅ Resume/Portfolio Enhancement  

---

## 🖥️ System Requirements

- Python 3.8+  
- Filebeat, Sysmon, Suricata installed on test machines  
- ELK Stack (7.x or higher) running locally or on VM  
- Shodan API key for host discovery  

---

## ⚠️ Disclaimer

This project is for **educational and research purposes only**. Do not deploy or run any part of this simulation on unauthorized or production environments.

---

## 📌 Author

**Rudraksh Gupta**  
[LinkedIn](https://www.linkedin.com/in/rudrakshguptaa) | [Portfolio](https://mohakrudrakshh.github.io/portfolio/)
