# Jenkins Java Demo CI/CD Automation Pipeline ☕🚀

A clean, production-ready Java application designed for Jenkins Continuous Integration and Continuous Deployment (CI/CD) pipelines with automated build triggers and SCM polling.

## 👩‍💻 Author & Details
- **Student / Author**: Antara Parab
- **Institution**: VESIT (Vivekanand Education Society's Institute of Technology), Mumbai
- **Course Focus**: DevOps, Continuous Integration, Automated Build & SCM Polling

---

## 🛠️ Overview & Architecture
This project demonstrates automated Java application compilation and verification triggered by source control changes using Jenkins SCM polling (`Poll SCM`).

### Key Capabilities
- **Automated Verification**: Verifies Java build integrity upon every commit.
- **Poll SCM Automation**: Automatically triggers Jenkins build jobs upon scheduled polling intervals (`* * * * *` or webhook triggers).
- **Lightweight Footprint**: Pure Java with zero external runtime dependencies.

---

## 🚀 Running Locally

### Prerequisites
- **Java Development Kit (JDK)**: Version 17 or higher
- **Git**

### Compile & Execute
```bash
# 1. Compile the Java source file
javac HelloJenkins.java

# 2. Run the compiled bytecode
java HelloJenkins
```

### Expected Output
```text
Hello from Antara!
Java build was successful.
This line is used to check the functionality of Poll SCM.
```

---

## ⚙️ Jenkins CI/CD Setup Guide

1. **Create a Freestyle Project** in your Jenkins Dashboard:
   - Project Name: `JenkinsJavaDemo`
2. **Configure Source Code Management (SCM)**:
   - Select **Git**.
   - Repository URL: `https://github.com/Antara-Parab/JenkinsJavaDemo.git`
   - Branch Specifier: `*/main`
3. **Build Triggers**:
   - Enable **Poll SCM**.
   - Schedule: `H/5 * * * *` (polls GitHub every 5 minutes for new commits).
4. **Build Steps**:
   - Add build step: **Execute Windows batch command** (or Shell for Linux):
     ```bash
     javac HelloJenkins.java
     java HelloJenkins
     ```
5. Click **Save** and trigger a build!

---

## 📜 License
Distributed under the [MIT License](LICENSE). Copyright (c) 2026 Antara Parab.
