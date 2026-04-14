---
title: "HackThisSite Writeups"
layout: single
permalink: /labs/hackthissite/
author_profile: true
---

# 🔐 HackThisSite Writeups

This section documents my hands-on solutions and analysis of web security challenges from :contentReference[oaicite:0]{index=0}.

The goal of these exercises is to identify vulnerabilities, understand insecure implementations, and apply practical exploitation techniques in a controlled environment.

---

## 🧠 Skills Demonstrated

- Web Application Security Testing  
- Source Code Analysis  
- Authentication Bypass  
- Insecure File Handling  
- Command Injection  
- Basic Cryptography Analysis  

---

# 🚀 Challenge Writeups

---

## 🔹 Level 1  

**Vulnerability:** Client-Side Information Exposure  

**Approach:**  
- Inspected page source  
- Identified hidden password in HTML comments  

**Finding:**  
Sensitive data exposed in frontend code  

**Lesson:**  
Never store secrets in client-side code  
👉 [View Full Report](../assets/Hack_This_Site/level_1.pdf)

---

## 🔹 Level 2  

**Vulnerability:** Broken Authentication Logic  

**Approach:**  
- Observed password validation relied on a missing file  
- Exploited logic flaw due to absent backend resource  

**Finding:**  
Authentication failed due to missing dependency  

**Lesson:**  
Always validate backend dependencies and handle errors securely  
👉 [View Full Report](../assets/Hack_This_Site/level_2.pdf)
---

## 🔹 Level 3  

**Vulnerability:** Direct Access to Sensitive Files  

**Approach:**  
- Inspected source code  
- Found reference to a `.php` file  
- Accessed file directly via URL  

**Finding:**  
Sensitive file publicly accessible  

**Lesson:**  
Restrict access to backend files and sensitive resources
👉 [View Full Report](../assets/Hack_This_Site/level_3.pdf)

---

## 🔹 Level 4  

**Vulnerability:** Hardcoded Credentials  

**Approach:**  
- Reviewed client-side scripts  
- Extracted password from embedded code  

**Finding:**  
Password stored in plaintext within script  

**Lesson:**  
Never hardcode credentials in frontend code  
👉 [View Full Report](../assets/Hack_This_Site/level_4.pdf)
---

## 🔹 Level 5  

**Vulnerability:** Information Disclosure  

**Approach:**  
- Triggered password reminder functionality  
- Observed system exposing sensitive information  

**Finding:**  
Password leaked via insecure reminder mechanism  

**Lesson:**  
Use secure password reset flows instead of exposing credentials  
👉 [View Full Report](../assets/Hack_This_Site/level_5.pdf)
---

## 🔹 Level 6  

**Vulnerability:** Weak Encryption Mechanism  

**Approach:**  
- Analyzed encryption tool  
- Identified predictable position-based character shifting  
- Reversed transformation to recover plaintext  

**Finding:**  
Encryption was easily reversible  

**Lesson:**  
Avoid custom encryption; use established cryptographic standards  
👉 [View Full Report](../assets/Hack_This_Site/level_6.pdf)
---

## 🔹 Level 7  

**Vulnerability:** Command Injection  

**Approach:**  
- Identified input passed to UNIX `cal` command  
- Injected additional commands (e.g., `ls`)  
- Discovered hidden file in directory  
- Retrieved password from file  

**Finding:**  
Application allowed execution of arbitrary system commands  

**Lesson:**  
Always sanitize user input and avoid direct system command execution  
👉 [View Full Report](../assets/Hack_This_Site/level_7.pdf)
---

# 📌 Key Takeaways

- Small misconfigurations can lead to full system compromise  
- Input validation is critical in web applications  
- Sensitive data must never be exposed or improperly stored  
- Secure coding practices are essential to prevent exploitation  

---

# ⚠️ Disclaimer

All activities were performed in a legal, controlled environment for educational purposes only.
