- **Title:** PhishCatcher: Client-Side Defense Against Web Spoofing Attacks Using Machine Learning
- **Authors:** Ahmedb Altamimi, Muzammil Ahmed, Wilayat Khan, Mohammad Alsaffar, Aakash Ahmad, Zawar Hussain Khan,Abdulrahman Alreshdi
- **Digital Object Identifier:** doi: 10.1109/ACCESS.2023.3287226.
- **Year:** 2023

## Abstract

Cyber security confronts a tremendous challenge of maintaining the confidentiality and integrity of user’s private information such as password and PIN code. Billions of users are exposed daily to fake login pages requesting secret information. There are many ways to trick a user to visit a web page such as, phishing mails, tempting advertisements, click-jacking, malware, SQL injection, session hijacking, man-in-the-middle, denial of service and cross-site scripting attacks. Web spoofing or phishing is an electronic trick in which the attacker constructs a malicious copy of a legitimate web page and request users’ private information such as password. To counter such exploits, researchers have proposed several security strategies but they face latency and accuracy issues. To overcome such issues, we propose and develop client-side defence mechanism based on machine learning techniques to detect spoofed web pages and protect users from phishing attacks. As a proof of concept, a Google Chrome extension dubbed as PhishCatcher, is developed that implements our machine learning algorithm that classifies a URL as suspicious or trustful. The algorithm takes four different types of web features as input and then random forest classifier decides whether a login web page is spoofed or not. To assess the accuracy and precision of the extension, multiple experiments were carried on real web applications. The experimental results show remarkable accuracy of 98.5% and precision as 98.5% from the trials performed on 400 classified phished and 400 legitimate URLs. Furthermore, to measure the latency of our tool, we performed experiments over forty phished URLs. The average recorded response time of PhishCatcher was just 62.5 milliseconds.



## **1. Problem & Objective**
The paper addresses the increasing threat of phishing attacks, where attackers create fake versions of legitimate web pages to steal sensitive user credentials such as passwords and PIN codes. The authors note that existing anti-phishing methods face issues related to latency and accuracy. To solve this, they propose a client-side defense mechanism that classifies URLs as either suspicious or trustful using machine learning algorithms.



## **2. Methodology**
- **Approach:** Development of a Google Chrome extension (PhishCatcher) that uses a Random Forest classifier to determine whether a login web page is legitimate or fake.
- **Input Features:** The algorithm takes into account four types of web features:
   - Visual Similarity (page layout and structure)
   - URL-based Features (length, HTTPS presence, subdomains, etc.)
   - Web Page Content (HTML elements, JavaScript behavior)
   - Blacklist Comparison (against known phishing sites)
- **Testing Approach:** The model was trained and tested using 400 phishing URLs and 400 legitimate URLs, and further experiments were conducted to assess latency.



## **3. Key Findings**
- The Random Forest classifier achieved 98.5% accuracy and 98.5% precision in identifying phishing websites.
- The average detection latency was only 62.5 milliseconds, making it highly efficient.
- The PhishCatcher Chrome extension successfully identified phishing pages in real-world tests, including a phishing attack targeting Inria (National Institute for Research in Digital Science and Technology, France).
- Compared to other anti-phishing tools, PhishCatcher performed significantly better in terms of detection accuracy and speed.



## **4. Conclusion **
- The client-side approach eliminates reliance on server-side solutions, enhancing privacy and independence from network latency.
- PhishCatcher provides real-time phishing detection, making it a useful tool for individual users and organizations.
- The study highlights the importance of machine learning in cybersecurity, especially for phishing attack detection.
- Future work could involve expanding the feature set, improving detection accuracy further and integrating with more browsers beyond Chrome.
