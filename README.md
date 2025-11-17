# 🛡️ Damn Vulnerable Flutter App (DVFA) 📱

### "How *not* to build a Flutter app."

**Welcome to the most insecure Flutter app you'll (hopefully) ever run!**

> \[!NOTE\]
> **🚀 Project Status: Under Active Development!**
>
> This project is a work-in-progress. We are busy planting vulnerabilities (and their corresponding fixes!) right now.
> Feel free to star ⭐️ or watch 👀 the repo to follow our progress. Contributions are highly welcome!

## 🧐 What is DVFA?

Damn Vulnerable Flutter App (DVFA) is an open-source, interactive learning tool designed to teach and demonstrate mobile application security vulnerabilities.

It's built with Flutter and is **intentionally packed with common security flaws** based on the **OWASP Mobile Application Security Verification Standard (MASVS)**.

## 🤔 Why Does This Exist?

We all love Flutter for its speed, beauty, and cross-platform magic. But in the rush to build, security can sometimes become an afterthought. DVFA was created to bridge the gap between Flutter development and mobile security, providing a "playground" where developers, pentesters, and students can:

* 👀 **See** common vulnerabilities in a real Dart codebase.
* 💥 **Exploit** these flaws in a safe, legal environment.
* 🔒 **Learn** the best practices to fix and prevent them.

## 🚀 The Core Concept: A Tale of Two Branches

This repo is split into two parallel universes, represented by two key branches:

### Branch: `develop` 👹
* **STATUS:** 🚨 **COMPLETELY VULNERABLE** 🚨
* This branch is a security nightmare (by design!). It contains all the vulnerabilities, waiting to be exploited.
* **Use this branch** to practice your pentesting skills, analyze the flaws, and see what *not* to do.

### Branch: `main` 😇
* **STATUS:** ✨ **PATCHED & SECURE** ✨
* This is our "happily ever after" branch. For every flaw in `develop`, the correct security fix is implemented here.
* **Use this branch** to compare the code (`git diff develop main`), learn remediation techniques, and see best practices in action.

---

## 🕹️ What You'll Get to Break (The Vulnerabilities)

We are building this app to cover all major OWASP MASVS categories. Here's a preview of the "features" you'll find in the `develop` branch:

* **MASVS-STORAGE:**
    * Insecure data storage (using `shared_preferences` for user tokens).
    * Unencrypted database files.
* **MASVS-NETWORK:**
    * Lack of SSL Pinning (ready for your Man-in-the-Middle proxy!).
    * Sending sensitive data over HTTP.
* **MASVS-CODE:**
    * Hardcoded API keys and other secrets (go find 'em!).
    * Sensitive data leakage in logs (`print()` statements galore).
* **MASVS-PLATFORM:**
    * Insecure WebView implementation (XSS, anyone?).
    * Exported components opening the door to attackers.
* **MASVS-RESILIENCE:**
    * No root/jailbreak detection.
    * No code obfuscation (making reverse-engineering a breeze).

...and many more as the project grows!

## 🎯 Who is this for?

* **Flutter Developers** who want to write more secure code.
* **Security Professionals/Pentesters** who want to test their mobile-hacking skills.
* **Students** and anyone curious about mobile application security.

## 🏁 How to Get Started

1.  Clone the repository:
    ```bash
    git clone [https://github.com/your-username/damn-vulnerable-flutter-app.git](https://github.com/your-username/damn-vulnerable-flutter-app.git)
    ```
2.  Check out the "vulnerable" branch:
    ```bash
    git checkout develop
    ```
3.  Install dependencies:
    ```bash
    flutter pub get
    ```
4.  Run the app on an emulator/device:
    ```bash
    flutter run
    ```
5.  **Start hacking!** 🕵️
6.  When you're stuck (or just curious), peek at the solution on the `main` branch:
    ```bash
    git checkout main
    ```

---

## ⚠️ IMPORTANT DISCLAIMER ⚠️

This application is intentionally insecure and designed for **educational purposes ONLY**.

* **DO NOT** deploy this in a production environment.
* **DO NOT** use any of the code patterns from the `develop` branch in your real applications.
* We are not responsible for any "I accidentally shipped the vulnerable code" confessions to your boss. You have been warned.

## 🤝 Contributing

Got an idea for a new vulnerability? Found a bug in our... well, *features*? We'd love your help! Please feel free to open an issue or pull request.

**Happy (and safe) hacking!**
