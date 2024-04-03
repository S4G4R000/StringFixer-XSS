# StringFixer-XSS
Here, I've uploaded a report showing how I discovered a reflected XSS vulnerability in a website.

## Conclusion

In this report, I conducted a thorough examination of the target website, [stringfixer.com](https://stringfixer.com/), focusing on the footprinting phase of the penetration testing process. Footprinting involves gathering information about the target host to understand its architecture, technologies used, and potential vulnerabilities.

### Technology Used

I identified the following technologies utilized by the website, emphasizing the importance of keeping them updated to prevent potential security risks. The investigation revealed the presence of vulnerabilities that could be exploited by attackers:

- **Gobuster**: A fast brute-force tool used for discovering hidden URLs, files, and directories within websites. It proved instrumental in uncovering hidden paths within the website's directory structure.

- **Dirsearch**: A command-line tool utilized for web application directory enumeration and discovery. Through dirsearch, I discovered hidden URLs such as `/apps`, `/js`, `/js.php`, `/backup`, among others.

### Fuzzing

During the fuzzing phase, I identified missing parameters in specific URLs, such as `/js.php` and `/report.php`, which could potentially lead to security vulnerabilities. Further investigation revealed a reflected cross-site scripting (XSS) vulnerability in the `/report.php` endpoint, demonstrating the website's susceptibility to malicious attacks.

### Vulnerability Exploitation

I successfully exploited the XSS vulnerability by injecting malicious JavaScript code into the `id` parameter of the `/report.php` URL. This vulnerability could enable attackers to steal session cookies, redirect users to malicious websites, or deface the website.

---

This report highlights the critical importance of conducting thorough security assessments and implementing robust measures to safeguard against potential vulnerabilities. By proactively identifying and addressing security weaknesses, organizations can mitigate the risk of exploitation and protect their assets from malicious actors.

---

