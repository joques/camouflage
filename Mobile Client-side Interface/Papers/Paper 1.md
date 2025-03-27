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
  
  
  
  

## Literature Review

### Traditional Approaches
1. **User Education:** Teaching users to recognize phishing signs.
   - **Limitation:** Attackers now use advanced techniques like homograph attacks and AI-generated scams, making manual detection difficult.
2. **Blacklist-based Detection:** Maintains a list of known phishing URLs.
   - **Limitation:** Fails to detect newly launched phishing websites.
3. **Visual Similarity-based Detection:** Compares website appearance with legitimate ones.
   - **Limitation:** Computationally expensive and ineffective against minor design changes.
4. **Search Engine-based Detection:** Uses domain popularity and rankings to verify legitimacy.
   - **Limitation:** Some phishing sites can still rank high in search results.

### Machine Learning-Based Approaches
- Machine learning (ML) methods extract features from URLs and website content.
- **Weaknesses Identified:**
  - Dependence on third-party lookups introduces delays.
  - Language-dependent models limit effectiveness against global phishing sites.
  - High false positive rates reduce usability.

## Used Approach
### Features Used in the Model
The authors define 12 hyperlink-specific features:
1. **Total hyperlinks (F1):** Total number of hyperlinks on a page.
2. **No hyperlink (F2):** Checks if the page has zero links (common in phishing sites).
3. **Internal hyperlinks (F3):** Counts links pointing within the same domain.
4. **External hyperlinks (F4):** Counts links pointing outside the domain.
5. **Null hyperlinks (F5):** Detects empty or fake links (e.g., `href="#"`).
6. **Internal/External CSS (F6):** Checks if external stylesheets are used.
7. **Internal Redirection (F7):** Counts internal links that redirect elsewhere.
8. **External Redirection (F8):** Counts links redirecting to different domains.
9. **Internal Error (F9):** Identifies broken links leading to internal 404 errors.
10. **External Error (F10):** Checks if external links return 404 errors.
11. **Login Form Link (F11):** Identifies suspicious login forms sending credentials to a different domain.
12. **Favicon Check (F12):** Determines if the favicon comes from the same domain.

### Feature Extraction Process
- Hyperlinks are extracted using a web crawler.
- Relative links are converted to absolute links.
- Feature vector construction:
  - Features are binary (0 or 1) based on phishing patterns.
  - Example: Many external redirects indicate a higher chance of phishing.

### Algorithms Used
- Logistic Regression (LR) classifier performed best.
- Training Dataset: 2,544 websites (1,428 phishing, 1,116 legitimate).
- **Other classifiers tested:**
  - Support Vector Machine (SVM)
  - Random Forest (RF)
  - Naïve Bayes (NB)
  - Neural Networks (NN)
  - Decision Tree (C4.5)
  - Adaboost

## Experimental Results
- **Dataset:** Phishing sites from Phishtank and legitimate sites from Alexa Top Sites.
- **Implementation:** Java (Jsoup for HTML parsing, WEKA for ML algorithms).
- **Evaluation:** 10-fold cross-validation.
- **Performance Comparison:**
  - **Logistic Regression:** 98.42% accuracy (best performer).
  - **Random Forest:** 97.37% accuracy.
  - **Neural Networks:** 97.25% accuracy.
  - **Decision Tree (C4.5):** 97.29% accuracy.
  - **Naïve Bayes:** 95.79% accuracy (lowest performer).

## Strengths
- **High Accuracy:** 98.42%, outperforming other ML-based phishing detection methods.
- **Zero-Hour Detection:** Works without blacklists, detecting phishing pages instantly.
- **Language-Independent:** Extracts structural features instead of text-based analysis.
- **Fast & Client-Side:** No need for third-party lookups (WHOIS, DNS), reducing latency.

## Limitations
- **Relies on HTML source code.** Attackers modifying hyperlink structures can reduce accuracy.
- **Cannot detect non-HTML phishing attacks** (e.g., image-based phishing).
- **Mobile phishing detection is not covered.**