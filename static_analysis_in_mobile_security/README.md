# Static Analysis in Mobile Security

## Project Description
This project covers the deep-dive static analysis phase of Android mobile application security. Every Android application (APK) consists of compiled DEX bytecode, manifest declarations, unpacked resources, native shared libraries (`.so`), and asset files. 

The primary objective of static analysis is to evaluate an application's attack surface, underlying logic, security posture, and hidden vulnerabilities without executing the code. By leveraging disassemblers, decompilers, and static extraction frameworks, security assessors can identify dangerous configurations, exposed sensitive data, weak cryptography, insecure IPC mechanisms, and obfuscated routines.

---

## Background Context
Static analysis forms the bedrock of mobile application security assessments. Unlike dynamic testing, which observes runtime behavior, static analysis exposes the architectural foundation and hardcoded secrets embedded inside the application package. 

Modern Android applications heavily rely on native libraries compiled from C/C++ to optimize performance or obscure critical business logic. Assessing these components alongside the Java/Kotlin layer requires a hybrid approach using both high-level Java decompilers and low-level native disassemblers. Mastering these static techniques enables defenders to audit code effectively, satisfy security standards (such as OWASP MASVS/MASTG), and harden applications against reverse engineering.

---

## Learning Objectives
By completing this static analysis module, you will be able to explain and demonstrate:

1. **Native Library & Bytecode Reverse Engineering:** How to decompile DEX bytecode and analyze native shared libraries (`.so`) using Ghidra, IDA Pro, and JADX.
2. **Obfuscation Analysis:** Techniques to identify, trace, and reverse-engineer obfuscated, optimized, or renamed code structures (e.g., ProGuard/R8).
3. **Decompilation & Vulnerability Identification:** Reconstructing APK source code to identify logic flaws, hardcoded credentials, and insecure API usage.
4. **Manifest & Resource Assessment:** Evaluating `AndroidManifest.xml` and resource files to understand exported components, permissions, and app capabilities.
5. **Static Risk Mitigation:** Identifying OWASP Mobile Top 10 vulnerabilities (such as insecure data storage and weak cryptography) through static code auditing.
6. **Integrity & Operational Security:** Conducting static investigations within a secure, isolated local environment while maintaining strict chain-of-custody and file integrity.

---

## Technical Requirements & Constraints
* **Environment:** Executed strictly within a local, controlled analysis environment (Kali Linux / Debian-based OS).
* **Relative Paths:** All scripts, tools, and output directives must use relative paths to ensure portability and automated execution compatibility.
* **Local Processing:** Cloud-based decompilers or online scanning utilities are prohibited; all processing is kept strictly local.
* **File Integrity:** Hash verification (MD5/SHA256) must be performed prior to unpacking or decompiling APK files.

---

## Tooling Framework

| Category | Tool | Purpose / Function |
| :--- | :--- | :--- |
| **APK Unpacking & Decoding** | **APKTool** | Decodes binary XML resources, assets, and extracts `smali` bytecode. |
| **Java/DEX Decompilation** | **JADX / JADX-GUI** | Decompiles `.dex` files into readable Java/Kotlin source code. |
| **DEX Conversion** | **Dex2jar / JD-GUI** | Converts Dalvik Executable formats to standard Java `.class` jars. |
| **Native Disassembly** | **Ghidra / IDA Pro** | Reverse engineers compiled native ELF/Shared Libraries (`.so` files). |
| **Scripting & Parsing** | **Python 3** | Automated pattern matching, regex scanning, and secret extraction. |

---

## Detailed Analysis Workflow

### 1. File Integrity & Package Unpacking
- Extract the raw APK package and verify file integrity using SHA256 checksums.
- Unpack binary assets, resources, and DEX files using APKTool:
  ```bash
  apktool d target_app.apk -o decompiled_apk/
