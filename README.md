# Atomic SecOps Mapping

[![Website](https://img.shields.io/badge/Website-atomicsecops.com-blue)](https://atomicsecops.com)
![GitHub License](https://img.shields.io/github/license/yourusername/atomic-secops-mapping?style=flat)
![GitHub Actions Workflow Status](https://img.shields.io/github/actions/workflow/status/yourusername/atomic-secops-mapping/deploy.yml?style=flat)
![Website](https://img.shields.io/website?url=https%3A%2F%2Fatomicsecops.com&style=flat)

<img src="logo.png" alt="Atomic SecOps Mapping, detection rules, Unified Data Model" width="250">

This repository provides a mapping of detection rules—originally in formats like Sigma—into a unified format (YARAL) tailored for integration with Google SecOps and the Unified Data Model (UDM). It serves as a bridge between simulated adversary techniques and operational security detection strategies.

### [Go to Atomic SecOps Mapping](https://atomicsecops.com)

## 🎯 Project Purpose

The purpose of Atomic SecOps Mapping is to streamline the integration of detection rules into modern security operations. By converting and mapping rules (such as Sigma rules) into YARAL, this project enables security teams to rapidly deploy and validate detections within the Google SecOps framework. This helps ensure that adversary simulations and threat detection capabilities are in sync.

## 🛠️ Project Origin

This project was born out of the need to enhance detection capabilities in a personal lab environment. Through the execution of simulated attacks and rigorous testing, detection rules were collected, converted, and mapped to the UDM used in Google SecOps. The conversion process combines both automated scripts and manual fine-tuning to achieve optimal compatibility and performance.

### Environment Setup

- **Operating System:** Primarily Windows (with plans to extend to other platforms)
- **Testing Tools:** Various threat simulation tools (e.g., Atomic Red Team)
- **Rule Conversion:** Custom Python scripts for converting Sigma rules to YARAL format, with adjustments for RE2 syntax and UDM field requirements
- **Integration:** Designed for use with the Google SecOps detection engine and UDM

The current focus is on Windows-based detections, though future updates will expand support for additional platforms.

## 🔄 Rule Conversion Process

Detection rules from formats such as Sigma are converted into YARAL using a multi-step process:
- **Parsing & Sanitization:** Load the Sigma rule YAML and clean up whitespace and problematic comments.
- **Regex & Field Adjustments:** Modify regular expressions to be RE2-compatible and insert the necessary `$event.` prefixes for UDM fields.
- **Targeted Fixes:** Apply custom fix-ups (e.g., escaping characters, collapsing duplicate modifiers) to ensure that the rules meet YARAL language constraints.
- **Metadata Formatting:** Use backticks for metadata values (description, references, etc.) and replace any internal backticks with single quotes.

This automated process significantly reduces manual effort when integrating new detection rules into the SecOps environment.

## 🤝 Contribution

Contributions are welcome! Here are a few ways you can help improve Atomic SecOps Mapping:

- **Rule Testing & Validation:** Help test the converted rules across different environments and provide feedback on their performance.
- **Conversion Enhancements:** Propose or implement improvements to the rule conversion scripts to handle new edge cases.
- **Documentation:** Improve this README and other documentation to better explain the mapping process and integration details.
- **General Feedback:** Open issues with suggestions, bug reports, or feature requests.

Feel free to submit a pull request or open an issue if you have ideas or improvements.

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 📞 Contact

For any questions or further discussion, please open an issue or contact the maintainer at [email@example.com](mailto:email@example.com).

---

Happy Detecting! 🔒
