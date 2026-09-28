# Linux Forensic Triage & Secure SSH Lab

A hands-on incident response and systems administration lab focused on investigating compromised Linux environments, analyzing malicious footholds, and implementing security remediation.

## 📁 Skills Demonstrated
* **Incident Response & Triage:** Identified active persistence mechanisms (cron backdoors, shell loops) and tracked attacker footprints via system logs (`auth.log`).
* **Linux Systems Administration:** Managed file systems, navigation shortcuts, configuration states, and user permissions via command-line interface (CLI).
* **Identity & Access Management (IAM):** Implemented SSH public/private key-pair authentication to mitigate password brute-force vulnerabilities.

## 🕵️‍♂️ Investigation Breakdown & Findings

### Phase 1: The Webadmin Server Breach
* **The Footprint:** Discovered a password brute-force entry in `auth.log` leading to an unauthorized public key insertion from IP `185.220.101.47`.
* **The Malware:** Located a malicious cron tab (`update-check.cron`) beaconing out to download an external shell script every 5 minutes.
* **Remediation:** Isolated evidence into incident logs, wiped the cron job, structured file directories cleanly, and enforced secure permissions.

### Phase 2: The Deploy Server Challenge (Unguided)
* **The Backdoor:** Discovered an active persistent shell loop in `update-agent.sh` targeting domain `cdn-analytics.top`.
* **Remediation:** Validated threat via automation tools, documented indicators of compromise (IoCs) in `findings.txt`, and purged malicious infrastructure.

## 🛠️ Tools Used
* Docker, Linux Shell (WSL2/Ubuntu), SSH, Grep, Find, Sudo, Tar/Gzip.

* <img width="816" height="712" alt="tree2" src="https://github.com/user-attachments/assets/f882af5f-1833-4c1b-8b1f-ae8b47b1edc0" />

