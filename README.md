# Threat Simulation & SIEM Detection Pipeline (TS-SDP)

![image](https://github.com/user-attachments/assets/be38b777-e1b9-4619-af3e-16b2515c24c1)


Threat Simulation & SIEM Detection Pipeline (TS-SDP) is an end-to-end, modular security lab that simulates real-world attacks and detects them using a fully integrated ELK Stack. It enables hands-on experience with threat simulation, detection engineering, log analysis, and SOC workflows.

## Lab Diagram

![image](https://github.com/user-attachments/assets/66fc65e7-7fee-45aa-8cf5-e7a397e1c0e0)


## Lab Infrastructure Diagram

![image](https://github.com/user-attachments/assets/dfccc575-57fc-468d-ae2b-1bf03b89c367)


The diagram above outlines the architecture of TS-SDP, which includes the following key components:

- **Sources**: Sysmon, Suricata, Filebeat, and simulated attack logs from Linux/Windows endpoints.
- **Monitoring and Aggregation**: Filebeat ships logs to Logstash for parsing and forwarding to Elasticsearch.
- **Output Tools**: Kibana dashboards visualize brute-force attempts, process anomalies, and credential misuse.

### Key Elements:
1. **Sources**:
   - Sysmon
   - Suricata
   - Filebeat (Linux/Windows)
   - Simulated logs via Python script

2. **Monitoring & Data Ingestion**:
   - Logstash (Grok Filters)
   - Elasticsearch

3. **Output & Analysis**:
   - Kibana Dashboards
   - Alert rules and visual queries

Each layer of the pipeline is designed to teach you how real-world telemetry is generated, parsed, and acted upon in a SOC environment.

## Capabilities

- **Realistic Attack Simulation**: Includes SSH brute-force and credential misuse using a custom Python + Shodan tool.
- **Custom Log Ingestion**: Parses logs from simulated attacks using Grok in Logstash.
- **Interactive Dashboards**: Kibana visualizes live attack patterns and detection metrics.
- **Rule Tuning Practice**: Simulated alerts allow hands-on experience in minimizing false positives.
- **Modular & Scalable**: Easily extendable to other attacks or log sources.

## System Architecture

### Components
- **SSH Brute-force Tool**: Python script using Shodan API and Paramiko for parallelized scanning.
- **Linux/Windows Clients**: Hosts that generate logs using Filebeat, Sysmon, Suricata.
- **Log Aggregator**: Logstash configures parsing and routes to Elasticsearch.
- **SIEM Frontend**: Kibana for dashboards and alerting.

## Key Takeaways

- Building end-to-end threat detection workflows.
- Writing and tuning Grok patterns in Logstash.
- Understanding attack telemetry in real-time.
- Developing detection logic and visual queries.
- Practicing alert triage based on live data.
- Hands-on SIEM engineering and blue team skills.

## Tooling

- **Python**: For simulating brute-force attacks.
- **Shodan API**: Real-time host discovery for scanning.
- **Paramiko**: SSH brute-force logic.
- **Sysmon & Suricata**: Endpoint and network telemetry.
- **Filebeat**: Log shipper for Linux/Windows.
- **Logstash**: Parsing and forwarding pipeline.
- **Elasticsearch**: Storage and search engine.
- **Kibana**: Dashboard and query visualization.

## System Requirements

- **Python 3.8+** (for attack tools)
- **ELK Stack (7.x+)** running locally or on VM
- **Filebeat + Sysmon + Suricata** on monitored machines
- **Shodan API Key** (for scanning public targets)
- **Ubuntu/Windows VMs** for simulation

## Integrated Solutions

- **Kibana**: Visualize brute-force, credential misuse, and anomaly detection.
- **Logstash**: Parse logs with Grok, enrich and forward to Elasticsearch.
- **Filebeat**: Stream logs from endpoints to Logstash.
- **Custom Attack Tool**: Runs SSH brute-force + Shodan scanning.
- **Sysmon & Suricata**: Capture endpoint and network-level events.

## Configuration Options

TS-SDP is modular and adaptable for:
- **Local VM-based testing** (ELK stack running on same host)
- **Cloud-based log collection** (via Filebeat + public IPs)
- **Tool replacement or extension** (e.g., add Caldera, Atomic Red Team)
- **Custom rules** for detections based on simulated attacks

## Usage Scenarios

- **SOC Lab Simulation**: Emulate a real detection pipeline.
- **Threat Detection Testing**: Validate your SIEM and alerting setup.
- **Detection Engineering Practice**: Learn to write Grok filters and tune rules.
- **Cybersecurity Education**: Train students on real telemetry and alerts.
- **Portfolio Development**: Add a practical, hands-on project to your GitHub.

## Credits

This project was built independently by **[Rudraksh Gupta](https://www.linkedin.com/in/rudrakshguptaa)** to demonstrate hands-on threat simulation, detection, and response workflows. Inspired by community contributions and the goal of enabling better blue team readiness.
