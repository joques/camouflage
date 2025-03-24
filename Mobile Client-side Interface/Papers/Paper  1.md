# A Machine Learning-Based Approach for Phishing Detection Using Hyperlinks Information

**Authors:** Ankit Kumar Jain, B. B. Gupta  
**Digital Object Identifier:** [https://doi.org/10.1007/s12652-018-0798-z](https://doi.org/10.1007/s12652-018-0798-z)  
**Published in:** Journal of Ambient Intelligence and Humanized Computing (2019)


## Abstract
This paper presents a novel approach that can detect phishing attacks by analyzing the hyperlinks found in the HTML source code of a website. The proposed approach incorporates various new outstanding hyperlink-specific features to detect phishing attacks. The approach divides hyperlink-specific features into 12 different categories and uses these features to train machine learning algorithms. Performance evaluation was conducted on various classification algorithms using phishing and non-phishing website datasets. The proposed approach is entirely client-side and does not require third-party services. Additionally, it is language-independent and can detect websites written in any textual language. The proposed approach achieved more than 98.4% accuracy on the logistic regression classifier.


## Context & Problem Statement 
- Phishing is a major cybersecurity threat affecting e-commerce, online banking, and social networks. Attackers create fake websites resembling legitimate ones to steal user credentials.
- 90% of cyberattacks start with phishing emails, and phishing accounts for over half of all internet fraud.
- Phishing websites have a short lifespan (few hours to days), making blacklist-based detection ineffective.
- There is a need for real-time, intelligent phishing detection without relying on third-party services.

### Limitations of Traditional Approaches
- Dependence on third-party services (WHOIS, search engines, DNS records) slows detection and makes it unreliable.
- Ineffective against zero-hour phishing attacks (new attacks not yet blacklisted).
- Many existing models are language-dependent, reducing their applicability to multilingual websites.

### Proposed Solution
- A client-side phishing detection system analyzing hyperlinks in a webpage’s HTML source code.
- **Key Features:**
  - Uses hyperlink-specific attributes for classification.
  - Categorizes hyperlinks into 12 types.
  - Does not require third-party services, ensuring fast and privacy-preserving detection.
  - Language-independent and capable of detecting phishing in any textual language.
  - Effective against zero-hour phishing attacks.
  
  
  
  