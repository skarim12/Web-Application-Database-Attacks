# Performing Web Application and Database Attacks

## Overview

This lab demonstrates common web application vulnerabilities and how they can be exploited in a controlled environment. Using Damn Vulnerable Web Application (DVWA) and OWASP Juice Shop, I performed security testing against Cross-Site Scripting (XSS), SQL Injection, Command Injection, and authentication vulnerabilities to understand how insecure input handling can expose sensitive systems and data.

Completed as part of the Cybersecurity Systems curriculum at St. John's University.

---

## Lab Environment

| Target | Purpose |
|---------|---------|
| DVWA (Damn Vulnerable Web Application) | XSS, SQL Injection, Command Injection |
| OWASP Juice Shop | Stored XSS, SQL Injection, Authentication Testing |
| Firefox Developer Tools | Web application analysis |
| cURL | HTTP request manipulation |
| SQL Database | Backend database testing |

---

## Objectives

- Perform web application reconnaissance
- Identify input validation weaknesses
- Demonstrate reflected and stored XSS attacks
- Exploit SQL Injection vulnerabilities
- Test command injection vulnerabilities
- Analyze authentication weaknesses
- Understand secure web development practices

---

## Tools Used

- **DVWA** — Vulnerable web application
- **OWASP Juice Shop** — Modern vulnerable web application
- **Firefox Developer Tools** — HTML and request inspection
- **cURL** — HTTP request manipulation
- **SQL** — Database query testing

---

# Lab Walkthrough

## 1. Cross-Site Scripting (XSS)

Reflected and stored XSS attacks were performed against DVWA to demonstrate how malicious JavaScript can execute when user input is not properly sanitized. The stored XSS attack showed how malicious code continues executing whenever another user visits the affected page.

---

## 2. SQL Injection

SQL Injection testing was performed to understand how unsanitized input can manipulate database queries. By testing different SQL statements, database structure information was identified before retrieving user information from vulnerable database tables.

---

## 3. Command Injection

The command execution feature in DVWA was tested to demonstrate how applications that pass user input directly to the operating system can allow arbitrary command execution.

---

## 4. Stored XSS on OWASP Juice Shop

Customer feedback functionality was tested for input validation weaknesses. Multiple payloads were evaluated until a stored XSS payload successfully executed each time the affected page was loaded.

---

## 5. SQL Injection on OWASP Juice Shop

The product search API was analyzed using SQL Injection techniques to determine the database structure. After identifying the correct number of query columns, user account information including email addresses and password hashes was retrieved from the Users table.

---

## 6. Authentication Testing

Authentication was evaluated by testing SQL Injection against the login form. The exercise demonstrated how insecure authentication logic can allow unauthorized access when applications fail to properly validate user input.

---

# Key Findings

- Reflected and stored XSS vulnerabilities allow attackers to execute malicious JavaScript within a user's browser.
- SQL Injection can expose sensitive database information when applications fail to validate input.
- Command Injection allows operating system commands to be executed through vulnerable web applications.
- Poor authentication logic can result in unauthorized account access.
- Proper input validation and parameterized queries significantly reduce web application risk.

---

# Defensive Takeaways

This lab reinforced the importance of implementing:

- Input validation and sanitization
- Output encoding
- Parameterized SQL queries
- Secure authentication mechanisms
- Proper error handling
- Principle of least privilege
- Regular web application security testing

Understanding these vulnerabilities helps security professionals identify insecure application behavior and improve detection and mitigation strategies.

---

## Skills Demonstrated

- Web Application Security
- Cross-Site Scripting (XSS)
- SQL Injection
- Command Injection
- Authentication Testing
- HTTP Request Analysis
- Vulnerability Assessment
- Secure Coding Awareness

---

## Disclaimer

This lab was conducted in an isolated educational environment using intentionally vulnerable applications as part of the Cybersecurity Systems curriculum at St. John's University. All testing was performed for defensive learning purposes only.
