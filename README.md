# CloudGarrison Multi-Cloud Posture Workbench

CloudGarrison is an **offline-capable operator console** designed for local evidence analysis, multi-cloud posture planning, and isolated simulations across AWS, Azure/Entra ID, GCP, Kubernetes, identity graphs, and detection engineering platforms. 

This local build runs inside the browser environment using Pyodide/WASM, acting as a secure sandbox that **does not perform live cloud checks or execute remote credentials**.

## 🚀 Key Features

- **Multi-Cloud Attack Surface Enumeration:** Simulated evaluation of AWS IAM/permission graphs, Azure subscription/resource topologies, and GCP service account privilege escalation pathways.
- **Local Infrastructure as Code (IaC) Audits:** Run embedded Checkov/TFLint compatible rules and Open Policy Agent (OPA) Rego simulations strictly in memory.
- **SaaS & CI/CD Trust Boundaries:** Audit trust connections for GitHub Actions and GitLab CI/CD workflows.
- **Graph & Timeline Analysis:** Map BloodHound, Cartography, or Stormspotter directory dumps, and analyze local AWS CloudTrail streams without sending data over a network.
- **Detection Draft Helper:** Author and validate multi-platform detection queries (Sigma, Sentinel KQL, Splunk SPL, Elastic EQL, Google SecOps YARA-L).

## 🔒 Security Architecture & Local-Input Policy

This repository provides the single-file offline local analysis layout (`offline-local-simulations`). 
- **Zero Provider Access:** Browser-to-cloud API endpoints are strictly disabled.
- **No Persistence:** Automatic workbench persistence is deactivated; tracking history remains inside temporary tab memory.
- **Sanitized Inputs:** Accepts only local files, redacted configuration snippets, or structural artifacts. 

## 🛠️ Requirements & Getting Started

1. Clone this repository.
2. Open the foundational `.html` workbench file in any modern web browser that supports WebAssembly.
3. Ensure Pyodide/Wasm completes its runtime compilation bootstrap loop directly in your browser.
