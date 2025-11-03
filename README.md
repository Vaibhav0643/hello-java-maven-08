# 🧩 Jenkins – Java Maven Build Pipeline

## 🚀 Project Overview
This project demonstrates how to integrate a **Java Maven application** with **Jenkins** to automate the build process.  
The pipeline automatically fetches the source code from GitHub, compiles it using Maven, and produces a deployable `.jar` artifact.

---

## ⚙️ Tools & Technologies Used
- **Jenkins** – Continuous Integration server  
- **Maven** – Build automation and dependency management  
- **Java** – Application source language  
- **GitHub** – Source code repository  
- **Docker** *(optional)* – To containerize Jenkins setup  

---

## 🧱 Jenkins Job Configuration
1. **Create a new Freestyle project** in Jenkins.  
2. Under **Source Code Management**, choose **Git** and add your repo URL:  https://github.com/<your-username>/hello-java-maven-08.git
3. Under **Build Environment**, check:
- `Delete workspace before build starts` *(optional)*
4. Under **Build Steps**, choose:  **Invoke top-level Maven targets**
5. Save and build the project.

---

## 🧰 Prerequisites
Ensure the following are installed and configured in Jenkins:
- JDK (Java 11+)
- Apache Maven
- Git

If using Jenkins Global Tools:
1. Go to **Manage Jenkins → Tools**  
2. Add **Maven** installations
3. Check "Install automatically" → "Add Installer" → "Install from Apache"
4. Uncheck “Install automatically” if already installed on your system  

---

## 🧾 Build Verification
After running the build, verify:
- **Console Output** ends with: **BUILD SUCCESS**
- **Workspace → target/** contains: hello-java-maven-1.0.jar
```bash
ls -l /var/lib/jenkins/workspace/hello-java-maven/target/
```
- To run the application manually:
```bash
java -cp /var/lib/jenkins/workspace/hello-java-maven/target/classes/ HelloWorld
```


## 🖼️ Screenshots  
All screenshots related to this project are available in the [`./Screenshot`](./Screenshot) folder.  
They include:  
- Jenkins Dashboard  
- Job Configuration Page  
- Build Console Output  
- Workspace Target Folder  
- Running Application Output  
- Build History with Success Status  

---

## 📘 References  
- [Jenkins Official Documentation](https://www.jenkins.io/doc/)  
- [Apache Maven Documentation](https://maven.apache.org/guides/)  
- [GitHub – hello-java-maven-08 Repository](https://github.com/Vaibhav0643/hello-java-maven-08)  

---

## 🧠 Learnings  
By completing this task, you will:  
- Understand how Jenkins automates Java Maven builds  
- Learn to fetch and build code from a GitHub repository  
- Generate and verify build artifacts automatically  
- Gain practical CI/CD experience with real project setup  




