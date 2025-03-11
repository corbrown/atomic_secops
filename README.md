# Atomic SecOps

[![Website](https://img.shields.io/badge/Website-atomicsecops.com-blue)](https://atomicsecops.com)
![Website](https://img.shields.io/website?url=https%3A%2F%2Fatomicsecops.com&style=flat)

<img src="secops-atomic-logo.png" alt="Atomic SecOps Mapping, detection rules, Unified Data Model" width="250">

## 🎯 Project Purpose

Atomic SecOps is designed to unify detection rules for security operations by mapping **Sigma rules** to **Google SecOps YARAL rules** and correlating them with **Atomic Red Team** adversary emulation tests. This provides **SOC teams and threat hunters** with a structured and actionable detection library.

### [Explore the Atomic SecOps Mapping](https://atomicsecops.com)

## 🔍 How It Works

1. **Data Sources**
   - **Atomic Red Team**: Provides adversary simulation test cases mapped to MITRE ATT&CK techniques.
   - **Sigma Rules**: Open-source detection rules mapped to relevant threats.
   - **Google SecOps YARAL**: Converted Sigma rules tailored for Google’s Unified Data Model (UDM).

2. **Automated Mapping**
   - Each **Sigma rule filename** is matched against **corresponding YARAL rules**.
   - Techniques from **Atomic Red Team** are linked with their **Sigma and SecOps detections**.
   - A **unified web interface** dynamically presents these mappings for easy reference.

3. **Live Threat Intelligence & Testing**
   - Security teams can **search, filter, and validate** detections based on MITRE ATT&CK techniques.
   - Analysts can execute **Atomic Red Team tests** and quickly access relevant detection logic.
   
## 🛠️ Project Origin

This project emerged from the need to bridge **threat simulation** with **real-world detection**. By leveraging Atomic Red Team for execution and Google SecOps for detection, **SOC analysts and blue teams** can improve their detection engineering workflows.

Disclaimer: This project is in its early stages. The effectiveness of detection logic heavily relies on the specific log sources ingested and how those logs are parsed. While the rules provided may validate successfully, modifications to UDM field names and logic may still be necessary to align with your specific environment. Additionally, these rules should be treated as baseline detections intended for testing pipelines and workflows, and should not be considered comprehensive or sufficient for full enterprise coverage.

## Credit

This project was heavily inspired by [AttackRuleMap](https://github.com/krdmnbr/AttackRuleMap).  

Conversions were assisted by a heavily doctored version of [pySigma Google SecOps (AttackIQ)](https://github.com/attackIQ/pySigma-Google-SecOps).

Adversary emulation scenarios are credited to the excellent team at Red Canary [Atomic Red Team](https://github.com/redcanaryco/atomic-red-team).  

Framework mappings and ATT&CK matrix concepts are credited to [The MITRE Corporation](https://github.com/mitre-attack).  

Finally, special appreciation and respect to Florian Roth at [SigmaHQ](https://github.com/SigmaHQ/sigma), whose pioneering contributions continue to inspire detection engineers around the globe.

## 🚀 Features

✅ **End-to-End Mapping** – MITRE ATT&CK Techniques → Atomic Tests → Sigma → SecOps YARAL  
✅ **Automatic Rule Matching** – Matches Sigma rules directly to YARAL equivalents  
✅ **Full Web UI** – Browse, filter, and search mapped rules dynamically  
✅ **Live Threat Validation** – Execute Atomic Red Team tests and validate detections  
✅ **Custom Rule Expansion** – Extend the mapping with additional detection engines  

## 🤝 Contribution

Want to improve Atomic SecOps Mapping? Here’s how you can help:

- **Validate Rules** – Test detections in different environments and submit feedback.
- **Enhance Automation** – Improve the mapping scripts to better handle edge cases.
- **Expand Data** – Add more Sigma rules, SecOps mappings, or atomic tests.
- **Documentation** – Refine explanations, usage guides, and technical details.

Feel free to **submit a pull request** or **open an issue** with suggestions.

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 📞 Contact

For inquiries, open an issue or contact the maintainer at [mail@threatlabs.tech](mailto:mail@threatlabs.tech).

---
