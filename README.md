#CS 305 Portfolio Artifact

For this course portfolio artifact, I selected my **Artemis Financial Practices for Secure Software Report**. This project focused on identifying security weaknesses in a web application and then refactoring the code to improve secure communication and integrity verification.

Artemis Financial was the client. The company provides individualized financial planning services and wanted stronger software security to help protect client and financial data. One of the main issues they wanted addressed was secure communication in the web application, along with a way to verify that transferred data had not been changed. To address that, I added HTTPS support, generated and configured a self-signed certificate, and implemented a SHA-256 checksum route for data verification.

One thing I did well in this project was finding the main security gaps in the starter application and focusing on practical fixes instead of adding unnecessary complexity. I identified that the original code was missing a checksum route and secure HTTPS configuration, and I was able to refactor the application so those features worked correctly. Coding securely is important because it helps protect confidentiality, integrity, and trust. For a company like Artemis Financial, that adds real value because clients need to know their data is being handled safely.

The most helpful part of the vulnerability assessment was seeing how security is not only about code syntax, but also about configuration, certificates, dependency management, and testing after changes are made. One challenging part was separating the vulnerabilities that already existed in the older dependency stack from the changes I personally introduced. That made me pay more attention to the difference between inherited risk and new risk caused by refactoring.

I increased layers of security by adding HTTPS, using a certificate-based SSL setup, implementing SHA-256 for checksum verification, and then running dependency-check after the refactoring. In the future, I would continue using static analysis tools, dependency scanners, manual review, and functional testing together. That gives a better picture than relying on only one method.

To make certain the application was functional and secure, I tested the code after each major change. I checked that the server ran correctly over HTTPS, confirmed that the `/hash` route returned the expected checksum output, and ran dependency-check to review whether the refactoring introduced any new issues. I also reviewed the code manually to make sure the logic and configuration changes were correct.

Some of the most useful tools and practices from this project were Java Keytool, Spring Boot configuration, OWASP Dependency Check, secure hashing with SHA-256, and the habit of testing after every refactor. Those are all things I can use again in future assignments and real development work.
