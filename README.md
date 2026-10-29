# 🛡️ Enterprise DevSecOps CI/CD Pipeline Security Framework

Production-grade Shift-Left DevSecOps automation framework designed to secure cloud infrastructure and deployment pipelines across **Azure DevOps** and **GitHub Actions**.

Developed by **[Ashish Pandey](https://github.com/Ashish09071991)** — Senior DevOps Engineer.

---

## 🌟 Security Architecture & Tool Matrix

| Layer | Tool | Purpose | Pipeline Gate |
|---|---|---|---|
| 🔑 **Secrets Detection** | **Gitleaks** & **TruffleHog** | Prevents committed API keys, tokens & credentials | Hard Fail on PR |
| 📦 **IaC Compliance** | **Checkov** & **TFSec** | Scans Terraform code for CIS benchmarks & Azure best practices | Blocking Gate |
| 🐳 **Vulnerabilities** | **Trivy** | Scans container images and filesystem dependencies (CVEs) | High/Critical Fail |
| 📊 **Code Quality** | **SonarQube** | Static Application Security Testing (SAST) & technical debt | Quality Gate |

---

## 📁 Repository Structure

\\\
├── .github/workflows/
│   └── devsecops-pipeline.yml   # Multi-stage GitHub Actions Security Workflow
├── azure-pipelines.yml          # Multi-stage Azure DevOps YAML pipeline definition
├── checkov-config.yml           # Customized Checkov security baseline rule overrides
└── README.md                    # Architecture and implementation guide
\\\

---

## 🚀 Key Benefits

* **Zero Hardcoded Secrets:** Automated pre-commit and pipeline-level secret detection.
* **Compliance by Code:** Prevents unencrypted storage, open NSG inbound rules, and missing tags before 	erraform apply.
* **Universal Pipeline Support:** Ready-to-use templates for both GitHub Actions and Azure DevOps YAML pipelines.
