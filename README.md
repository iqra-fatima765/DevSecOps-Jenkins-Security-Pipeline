# 🔐 DevSecOps Security Pipeline with Jenkins

A hands-on DevSecOps lab completed as part of the Secure Software Design and Development Lab (CY256L).

## 📌 Overview

This lab focuses on integrating security practices into a CI/CD pipeline using Jenkins. The pipeline demonstrates how different security testing and analysis techniques can be incorporated throughout the software development lifecycle.

## 🎯 Objectives

- Understand the fundamentals of DevSecOps and secure CI/CD.
- Configure Jenkins for automated pipeline execution.
- Integrate security testing into different pipeline stages.
- Identify vulnerabilities in source code and dependencies.
- Generate an SBOM for software component visibility.
- Detect exposed secrets and sensitive information.
- Perform container and runtime security testing.
- Analyze security reports and pipeline results.

# 🧩 Pipeline Stages

## 1. Checkout

The pipeline begins by retrieving the application source code required for the subsequent build and security testing stages.

### Activities

- Source-code retrieval
- Repository checkout
- Workspace preparation

---

## 2. Build

The build stage prepares the application for further analysis and security testing.

### Activities

- Application build
- Dependency preparation
- Build verification

---

## 3. Static Application Security Testing (SAST)

SAST analyzes application source code without executing the application.

In this lab, **SonarQube** was integrated into the Jenkins pipeline to perform static code analysis.

### Purpose

- Identify potential coding vulnerabilities
- Detect code-quality issues
- Identify security hotspots
- Analyze source-code weaknesses

### Tool

**SonarQube**

---

## 4. Dependency Check

The dependency-check stage analyzes third-party libraries and dependencies used by the application.

**OWASP Dependency-Check** was used to identify known vulnerabilities in project dependencies.

### Purpose

- Identify vulnerable dependencies
- Detect outdated components
- Analyze known Common Vulnerabilities and Exposures (CVEs)
- Improve dependency security

### Tool

**OWASP Dependency-Check**

---

## 5. Software Bill of Materials (SBOM)

An SBOM provides an inventory of software components and dependencies used within an application.

### Purpose

- Improve software component visibility
- Identify third-party dependencies
- Support vulnerability management
- Improve software supply-chain transparency

---

## 6. Secrets Detection

The secrets detection stage checks the source code for accidentally exposed sensitive information.

Examples include:

- Passwords
- API keys
- Access tokens
- Credentials
- Other sensitive configuration data

### Purpose

To reduce the risk of credentials or sensitive information being accidentally committed to source-code repositories.

---

## 7. Software Composition Analysis (SCA)

Software Composition Analysis focuses on identifying security risks within third-party and open-source components.

### Purpose

- Identify vulnerable open-source dependencies
- Analyze third-party libraries
- Improve software supply-chain security
- Support dependency risk management

---

## 8. Container Security

The container security stage evaluates application containers for potential security weaknesses.

### Purpose

- Identify vulnerable container components
- Improve container security
- Detect potential security risks
- Support secure container deployment

---

## 9. Dynamic Application Security Testing (DAST)

DAST analyzes an application while it is running.

Unlike SAST, which examines source code, DAST evaluates the application's runtime behavior from an external perspective.

### Purpose

- Identify runtime vulnerabilities
- Test application behavior
- Detect potential web security issues
- Evaluate the security posture of the running application

---

# 🛠️ Tools & Technologies

### CI/CD & Automation

- Jenkins
- CI/CD
- DevSecOps

### Application Security

- SonarQube
- SAST
- DAST
- SCA

### Dependency & Supply Chain Security

- OWASP Dependency-Check
- SBOM
- Secrets Detection

### Container Security

- Container Security
- Container Vulnerability Assessment

---

# ⚙️ Jenkins Pipeline

The Jenkins pipeline automates the execution of different security checks.

Each stage performs a specific security function and produces results that can be analyzed to identify potential vulnerabilities and weaknesses.

## 📊 Security Workflow

```text
Source Code
     ↓
  Checkout
     ↓
    Build
     ↓
    SAST
     ↓
Dependency Check
     ↓
    SBOM
     ↓
Secrets Detection
     ↓
     SCA
     ↓
Container Security
     ↓
    DAST
     ↓
Security Analysis & Reporting
