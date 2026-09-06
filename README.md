# Mobile Security Specialization

## Background Context
Mobile applications are among the most widely used software in the world — and among the most targeted. Every APK contains layers of compiled bytecode, native libraries, resource files, and configuration data that together define how an application behaves. Understanding these layers is a fundamental skill for any mobile security professional.

Static analysis lets you examine an application's structure, permissions, and logic without ever running it. Combined with dynamic analysis — monitoring function calls, memory operations, and runtime behavior — you gain a complete picture of what an application is truly doing, beyond what its interface suggests.

In this module, you will work directly with real APK files. You will decompile bytecode, analyze native libraries, inspect manifest files, and reverse engineer obfuscated code using industry-standard tools. You will learn how attackers find hidden methods, extract secrets, and identify vulnerabilities, as well as how defenders use the same techniques to harden applications before they ship. 

> *"You cannot secure what you do not understand."*

---

## Learning Objectives
By the end of this module, you should be able to explain the following concepts without external assistance:

* How to use reverse engineering tools to analyze native libraries (`.so`) and APK bytecode (`.dex`).
* Techniques for extracting and understanding obfuscated or optimized code.
* Methods for decompiling and analyzing an APK file to uncover vulnerabilities or hidden methods.
* The role of resources (`res/`) and the manifest file (`AndroidManifest.xml`) in understanding an app’s structure and attack surface.
* How dynamic analysis tools monitor function calls, IPC, and memory operations at runtime.
* How to use profiling tools to detect performance issues or security vulnerabilities.
* Debugging and profiling native code to detect memory leaks, buffer overflows, or pointer errors.
* How to combine debugging tools across native (C/C++) and Java/Kotlin layers to uncover security flaws.
* How static code analysis helps identify OWASP Mobile Top 10 risks.
* Overcoming anti-analysis, anti-debugging, and obfuscation challenges in APK reverse engineering.
* Maintaining integrity, safety, and operational security during the analysis process.

---

## Requirements & Environment Guidelines
* **Environment:** All analyses must be conducted inside an Android Emulator or a dedicated physical device within an isolated testing environment.
* **OS Compatibility:** All scripts and tools must be executable on Kali Linux or compatible Debian-based analysis distributions.
* **Allowed Tools:** 
  * *Static Analysis & Reverse Engineering:* JADX, APKTool, Ghidra, IDA Pro, Dex2jar, JD-GUI.
  * *Dynamic Analysis & Instrumentation:* Frida, GDB, Valgrind, Android Studio Profiler.
  * *Automation & Scripting:* Python 3, NumPy, JMH.
* **Path Management:** All scripts must strictly use relative paths to avoid hardcoded dependency failures during automated grading/evaluation.
* **Integrity & Security:** 
  * Validate file hashes (MD5/SHA256) before analysis.
  * Work locally — usage of online decompilers or cloud-based analysis services is strictly prohibited.
* **Backup:** Maintain regular backups of original APKs, scripts, and logs.

---

## Repository Structure

```text
.
├── static_analysis_in_mobile_security/   # Static Analysis & APK Reverse Engineering Lab
└── README.md                             # Global Mobile Security Module README
