Compliance Automation
The Compliance Automation project is a Python-based tool designed to automate security and configuration checks against various industry compliance standards, including PCI-DSS, NIST SP 800 Series, and ISO 27001.

Its primary goal is to provide a fast, repeatable, and non-intrusive method for internal auditing and continuous monitoring of infrastructure and application configurations.

✨ Features
Modular Checks: Easily add new compliance checks as individual Python files.

Multi-Standard Support: Organized structure for checks against PCI-DSS, NIST, and ISO 27001 controls.

Configuration Driven: Use YAML files to define acceptable compliance thresholds (e.g., minimum password length, maximum log retention).

Reporting: Generates clear, actionable reports on compliance status (in a future iteration).

🚀 Installation
Prerequisites
You need Python 3.8+ installed on your system.

Steps
Clone the Repository:

git clone [https://github.com/your-username/compliance-automation.git](https://github.com/your-username/compliance-automation.git)
cd compliance-automation

Install Dependencies:
We use the PyYAML library to handle configuration settings.

pip install -r requirements.txt

⚙️ Configuration
All compliance parameters are managed in YAML files within the config/ directory.

The main configuration file is config/compliance_settings.yaml. You must adjust these values to reflect the specific requirements of your organization's compliance profile.

💻 Usage Example
The main.py script is the entry point for running the automated checks.

Run All Checks
To execute the entire suite of configured checks:

python main.py

Sample Check Output
The included sample, checks/password_policy.py, will run a check against the defined password requirements:

# Example command to run the specific module:
python main.py --check password_policy

Expected Output:

Compliance Check: Password Policy
-------------------------------------
[PASS] Minimum Length: Required 14, Found 14
[PASS] Complexity Requirement: Required upper/lower/number/symbol, Found satisfied
[FAIL] Password History: Required 24, Found 12. Policy not compliant.
-------------------------------------
RESULT: 1 FAILED check(s) found. NON-COMPLIANT.

🤝 Contributing
We welcome contributions! Please see the CONTRIBUTING.md (to be created) for details on how to submit pull requests and add new compliance modules.
