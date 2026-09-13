# Mobile Application Dynamic Analysis & Runtime Instrumentation

## Introduction
Static analysis reveals the blueprint of an application, but dynamic analysis exposes its true behavior. In mobile security, the most critical vulnerabilities often only surface when the app is running, hidden behind obfuscation, encrypted traffic, and anti-tampering mechanisms. This project shifts focus from reading code to manipulating runtime environments. You will master the art of instrumentation using industry-standard tools like Frida and Objection, learning to hook functions, bypass root detection, and break SSL pinning in real-time. By forcing the application to execute on your terms, you will uncover sensitive data flows and logic flaws that static analysis alone can never reveal.

## Context
You have been provided with a target Android APK designed with security controls intended to prevent inspection. Standard static analysis has proven insufficient due to code obfuscation and complex logic. Your mission is to deploy the application within a secure emulator or device and conduct a comprehensive dynamic assessment. You will intercept network communications, bypass client-side restrictions, and inject scripts to manipulate the application's runtime state. The objective is to demonstrate how an attacker can circumvent security measures to access protected functionality and exfiltrate sensitive data, documenting every step from initial setup to final exploitation.

## Resources
**Read or watch:**
* [CodeShare](https://codeshare.frida.re/)
* [JNI Overview](https://developer.android.com/training/articles/perf-jni)
* [Android Developer Guide](https://developer.android.com/guide)
* [Android NDK Documentation](https://developer.android.com/ndk/guides)
* [Android Reverse Engineering (ARE)](https://github.com/ashishb/android-security-awesome)
* [Android Security Documentation](https://source.android.com/docs/security)
* [Reverse Engineering Guides](https://binarly.io/posts)
* [Frida Documentation](https://frida.re/docs/home/)
* [OWASP Mobile Application Security Testing Guide (MASTG)](https://mas.owasp.org/)

## Tools

### Dynamic Analysis Tools
* [Objection](https://github.com/sensepost/objection)
* [Frida Official Site](https://frida.re/)
* [ADB Documentation](https://developer.android.com/tools/adb)
* GDB
* Ghidra
* IDA Pro
* [Android Studio](https://developer.android.com/studio)

### Network Interception Tools
* Burp Suite
* mitmproxy
* Wireshark

### APK Analysis Tools
* APKTool
* jadx

### Programming and Scripting
* Python

## Learning Objectives
At the end of this project, you are expected to be able to explain to anyone, without the help of Google:
* What is dynamic analysis, and how does it differ from static analysis in mobile security?
* How can dynamic analysis be effectively applied to mobile applications to monitor real-time behavior?
* How can Frida be used to inject scripts, hook functions, and interact with applications at runtime?
* In what ways does Objection simplify Frida’s capabilities, and how can it assist in tasks like bypassing security features and extracting data?
* What techniques allow us to observe hidden functions and sensitive data handling in real-time?
* How can mobile applications’ interactions with system resources and their internal data flows be analyzed dynamically?
* How can we intercept and analyze an app’s network traffic to identify vulnerabilities in data transmission?
* What are effective methods for bypassing SSL pinning to gain deeper insight into network communications?
* What are common anti-debugging and anti-tampering techniques used in mobile apps?
* How can we bypass protections like root detection, code obfuscation, and method protection to facilitate a smoother dynamic analysis?
* What are best practices for documenting the dynamic analysis process, tool usage, and observed behaviors?
* How can identified vulnerabilities and sensitive findings be reported in a way that highlights risks and suggests improvements?

## Requirements

### General
* **Allowed Tools:** Frida, Objection, GDB, APKTool, JADX, Wireshark, mitmproxy, Android Debug Bridge (ADB), Burp Suite.
* **Environment:** All analyses should be conducted on an Android emulator or a physical device within a secure, controlled environment.
* **Backup:** Regularly back up APK files, scripts, and key data before and during the analysis process.
* **Execution Compatibility:** Ensure all scripts and tools can be executed and run on Kali Linux or a compatible analysis environment.
* **Path Management:** Use relative paths for all file references to avoid dependency on hardcoded paths.
* **Integrity Checks:** Validate APK and binary integrity before analysis to prevent issues due to corrupted or tampered files.
* **Tool Configuration:** Configure all monitoring and network tools correctly, including proxy and certificate settings, before beginning the analysis.
* **Documentation:** Maintain organized, clear, and detailed documentation for each step of the analysis, including findings and tool usage.
* **Focus:** Concentrate your analysis on the designated APK provided for the project.
* **Local Execution:** All work must be completed within the secure environment on the local machine or emulator; use of online tools or cloud services is not permitted for this project.
