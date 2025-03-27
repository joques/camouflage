

# Mobile Anti-Phishing: Approaches and Challenges  

- **Authors:** Hossain Shahriar, Chi Zhang, Stephen Dunn, Robert Bronte, Atef Sahlan, and Khaled Tarmissi  
- **Digital Object Identifier:** [10.1080/19393555.2019.1691293](https://doi.org/10.1080/19393555.2019.1691293)  
- **Year:** 2019

## Abstract  
As technology is constantly evolving, modern conveniences such as mobile devices have changed the way that society performs its daily routines and functions as a whole. Because the evolution of technology has made it almost a requirement for citizens to possess mobile devices, this increase in ownership has also brought security issues such as phishing.  A phisher intends to obtain information that will aid the hacker by appearing to the unsuspecting owner as a trustworthy entity. The goal of phishing is to fool mobile device owners into giving the attacker sensitive information, such as usernames, passwords, as well as credit and debit card information. In this paper, we provide a taxonomy of mobile anti-phishing techniques and mitigation strategies available for mobile devices. Our goal is to provide an informative model to identify current solutions in reducing phishing attacks on mobile devices and outline limitations and future challenges.

## Context & Problem Statement  

- The widespread adoption of mobile devices has increased the risk of phishing attacks, as mobile users frequently engage in online banking, e-commerce, and social media.  
- Phishing is a method where attackers trick users into revealing sensitive information by impersonating legitimate websites or applications.  

### Common Forms of Mobile Phishing:  
- **Smishing (SMS phishing):** Malicious links sent via text messages.  
- **Malicious apps:** Fake applications designed to steal user credentials.  
- **Browser-based phishing:** Fake login pages that mimic real websites.  

### Why Mobile Phishing is Harder to Detect:  
- Small screen sizes make it difficult to verify URLs.  
- Users are less aware of phishing risks compared to desktop users.  
- More than 40% of mobile applications require users to enter credentials, creating phishing opportunities.  

### Goal of the Paper:  
- Provide a taxonomy of mobile anti-phishing techniques.  
- Identify existing solutions and their limitations.  
- Outline future research challenges.  

## Literature Review
- Mobile Phishing Context: The rise in mobile device usage has coincided with an increase in phishing attacks. Android, the most widely used mobile OS, is particularly vulnerable due to malicious apps in the Google Play Store (e.g., a 338% increase in malicious apps reported by Robinson, 2014).

- Existing studies have explored various methods for phishing detection, including behavior analysis, feature selection, and machine learning models.

- A large-scale study on 19,066 phishing attacks from PhishTank found that 90% were duplicates or slight modifications of previously recorded phishing attempts.

- Zero-day phishing attacks remain a major challenge, requiring more advanced detection techniques.


## Mobile Phishing Mitigation Techniques  
The paper categorizes mobile phishing detection and mitigation techniques into 10 approaches, each with unique strengths and weaknesses.

### 1 IP Packet Analysis
- MP-Shield (Android-based detection framework) 
  - Uses network traffic analysis to detect phishing attacks.  
  - Relies on blacklists, watchdog monitoring, and HTML analysis.  
  - **Weakness:** Limited to IP-based filtering, does not handle content-based phishing.  
  - **Effectiveness:** 71.99% detection accuracy using J48 decision tree classifier.  