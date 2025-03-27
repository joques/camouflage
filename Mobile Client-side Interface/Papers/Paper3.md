# Next Generation of Phishing Attacks Using AI-Powered Browsers

**Author**: Akshaya Arun  
**Affiliation**: Northumbria University, UK  
**Digital Object Identifier**: [https://doi.org/10.48550/arXiv.2406.12547](https://doi.org/10.48550/arXiv.2406.12547)  



## Abstract
The increase in the number of phishing demands innovative solutions to safeguard users from phishing attacks. This study explores the development and utilization of a real-time browser extension integrated with a machine learning model to improve the detection of phishing websites. The results showed that the model had an accuracy of 98.32%, precision of 98.62%, recall of 97.86%, and an F1-score of 98.24%. When compared to other algorithms like Support Vector Machine, Naïve Bayes, Decision Tree, XGBoost, and K Nearest Neighbor, the Random Forest algorithm stood out for its effectiveness in detecting phishing attacks. The zero-day phishing attack detection testing over a 15-day period revealed the model's capability to identify previously unseen threats and thus achieving an overall accuracy rate of 99.11%. Furthermore, the model showed better performance when compared to conventional security measures like Google Safe Browsing. The model had successfully detected phishing URLs that evaded detection by Google Safe Browsing. This research shows how using machine learning in real-time browser extensions can defend against phishing attacks. It gives useful information about cybersecurity and helps make the internet safer for everyone.


## Context & Problem
- Phishing attacks remain a major cybersecurity concern, leading to financial losses, malware infections, and unauthorized access to sensitive data.
- Attackers constantly evolve their techniques, leveraging new technologies to evade detection.
- Traditional blacklist-based detection methods are ineffective because new phishing domains can be registered quickly.
- The study proposes a real-time browser extension integrated with a machine learning model to detect phishing websites.
- The primary goal is to develop a real-time, AI-powered phishing detection system that improves upon conventional security measures like Google Safe Browsing.

## Research Contributions
1. The paper proposes a real-time browser extension integrated with a machine learning-based phishing detection model to detect and block phishing websites.
2. The model leverages Random Forest (RF) as the primary classification algorithm, outperforming other ML models such as SVM, Naïve Bayes, XGBoost, and KNN.
3. **Key contributions**:
   - High-accuracy phishing detection (98.32% accuracy).
   - Zero-day phishing attack detection with 99.11% accuracy over a 15-day period.
   - Comparison with Google Safe Browsing, proving superior performance in identifying new phishing URLs.
   - Integration of a reporting feature, allowing users to flag suspicious websites, contributing to an adaptive threat detection system.


## Literature Review
The paper reviews various phishing detection approaches, identifying their strengths and weaknesses:

### Traditional Approaches
1. **Blacklist-Based Detection**:
   - Maintains a list of known phishing URLs.
   - Limitation: Cannot detect newly launched (zero-day) phishing sites.
2. **Heuristic-Based Detection**:
   - Uses predefined rules to analyze website content, URLs, and metadata.
   - Limitation: Attackers can modify website features to bypass detection.

### Machine Learning-Based Approaches
- **Feature Selection-Based ML Models**:
   - Prior research used wrapper feature selection combined with classifiers like Random Forest and SVM, achieving 97.3% accuracy.
   - Weakness: High computational cost and inability to detect zero-day phishing attacks.
- **CSS-Based Phishing Detection**:
   - Analyzes webpage styling to detect fake sites mimicking legitimate ones.
   - Weakness: Consumes high memory and fails when dealing with complex CSS rules.
- **URL-Based Detection**:
   - Uses lexical analysis and feature selection to classify phishing sites.
   - Weakness: Does not account for content-based phishing techniques.

### Gaps in Existing Research
1. Lack of real-time zero-day phishing detection.
2. Dependency on third-party services (DNS, WHOIS, search engines), which introduce latency.
3. Offline operation of most ML-based systems, reducing their effectiveness in real-time detection.

## Research Methodology

### Data Collection & Processing
- The dataset consists of 380,009 URLs, split into:
  - 196,757 legitimate URLs
  - 183,252 phishing URLs
- Data was sourced from PhishTank and Kaggle, ensuring a mix of real-world and synthetic phishing URLs.
- 42 key features were extracted, including URL structure, domain age, HTTPS presence, and page content analysis.

###  Machine Learning Model
- Random Forest was chosen due to its superior performance in phishing detection.
- The dataset was split 70-30 for training and testing.
- The trained model was saved using joblib for integration into the browser extension.

### Browser Extension Development
- Developed using JavaScript, HTML, and CSS.
- The extension sends a real-time HTTP request to the ML model API (Flask-based) for URL classification.
- If a URL is identified as phishing, the extension blocks access and alerts the user.
- A reporting system was integrated, allowing users to flag phishing websites for dataset updates.


## Results

### Zero-Day Phishing Detection
- The model was tested against new phishing URLs reported daily on PhishTank over 15 days.
- Out of 225 phishing URLs, the model correctly classified 223, achieving 99.11% accuracy.
- Google Safe Browsing failed to detect several phishing URLs, while the proposed model successfully identified them.

### Comparison with Other ML Models
| Algorithm                   | Accuracy (%) |
|-----------------------------|--------------|
| Random Forest               | 98.32        |
| Support Vector Machine (SVM) | 95.76        |
| Naïve Bayes                 | 93.12        |
| Decision Tree               | 96.48        |
| XGBoost                     | 97.89        |
| K-Nearest Neighbor (KNN)    | 94.63        |

### Key Findings
- Random Forest achieved the best performance compared to other models.
- The browser extension effectively blocks phishing URLs in real-time.
- Zero-day phishing attack detection is highly effective, surpassing conventional methods.

## Limitations
- The model does not analyze website behavior after initial classification.
- Dynamic phishing attacks (using JavaScript obfuscation) could bypass detection.
- The browser extension currently works only in Google Chrome.
