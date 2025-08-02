# VAPT
Perform a Vulneribility Assessment and Penetration Testing on "icampus erp"

# 🔐 Vulnerability Assessment of iCampus ERP Portal

This project demonstrates a **Vulnerability Assessment and Penetration Testing (VAPT)** conducted on the student login portal of **iCampus ERP** using the **OWASP ZAP** tool. The analysis highlights key security flaws, evaluates their impact, and proposes mitigation strategies to improve web application security for educational platforms.

---

## 🧰 Tools and Environment

- **OWASP ZAP v2.16.1**  
- **Firefox Browser**  
- **Kali Linux OS**

---

## 📋 Methodology

1. **Reconnaissance** – Initial exploration of the target web portal.  
2. **Spidering & Crawling** – Discovery of links and input vectors using ZAP’s spider tool.  
3. **Active Scanning** – Automated scripts to detect vulnerabilities.  
4. **Manual Testing** – Validation of cookies, headers, and site behavior.

---

## 🚨 Key Findings

| Vulnerability                                | Risk Level   | Description                                               |
|---------------------------------------------|--------------|-----------------------------------------------------------|
| CSP Header Not Set                          | Medium       | Increases susceptibility to XSS attacks                   |
| Timestamp Disclosure                         | Low          | Reveals internal system timings                           |
| Cookie Without Secure Flag                   | Low          | May allow interception over non-HTTPS                     |
| X-AspNet-Version Disclosure                  | Low          | Exposes backend tech stack details                        |
| Use of Vulnerable JS Libraries               | Medium       | Can be exploited via known vulnerabilities                |
| Unsafe Inline & Eval Scripts                 | Medium       | Opens door to script injection attacks                    |

---

## 📈 Graphical Insights

- **Alert Breakdown:** Medium, Low, Informational alerts categorized by type and confidence.
- **Response Charts:** Visual representation of system behavior during scans.
- **Site Summary:** Focused on `https://student.icampuserp.in` among other associated domains.

---

## 🛡️ Recommendations

- Enforce **Content Security Policy (CSP)** headers.  
- Use **Secure** and **HttpOnly** attributes for all cookies.  
- Suppress or sanitize **HTTP response headers** that leak server details.  
- Regularly **audit and update third-party JS libraries**.  
- Integrate **CAPTCHA security practices** through secure APIs.

---

## 🏁 Conclusion

The project successfully identified several medium and low-risk vulnerabilities in iCampus ERP’s login module. Proactive VAPT assessments, especially for systems handling sensitive student data, are crucial for maintaining robust digital defenses.

---

## 🔗 References

- [OWASP Top 10](https://owasp.org/www-project-top-ten/)  
- [ZAP Documentation](https://www.zaproxy.org/docs/)  
- [CWE Vulnerability Database](https://cwe.mitre.org)  

