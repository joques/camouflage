## Browser Fingerprinting

When it comes to methodologies for capturing and analysing web-based fraud, particularly through browser fingerprinting and phishing detection, several projects and techniques stand out:- 

**1. Web-based Fingerprinting Techniques**
   - The study by Bernardo and Domingos explores various web-based fingerprinting techniques, categorising them into browser and cross-browser fingerprinting. These techniques allow websites to differentiate devices based on browser features or system settings, even across different browsers. The taxonomy provided in this study helps identify security and privacy threats associated with each technique[1].

**2. SEON's Browser Fingerprinting**
   - SEON's platform employs browser fingerprinting as a fraud prevention technique. It uses HTML5 canvas fingerprinting and WebGL fingerprinting to create unique user IDs, which can help detect fraudulent activities like identity theft and card-not-present (CNP) fraud. SEON combines these techniques with other fraud detection features, such as social media lookups and IP analysis, to enhance security[6].

**3. FingerprintJS**
   - FingerprintJS is an open-source library that provides browser fingerprinting capabilities. It identifies website visitors by analysing their browser and device configurations, offering a high level of accuracy in detecting fraud. The library is easy to integrate and can be enhanced with the Pro version for server-side processing and additional features[8].

## Phishing Detection

**1. PhishNet**
   - PhishNet is a web application that uses machine learning, specifically XGBoost, to detect phishing websites. It processes datasets of URLs to extract features like URL length and domain age and training models to identify phishing sites with high accuracy. The application provides real-time predictions and is scalable, utilising platforms like Google Colab and AWS EC2[2].

**2. Fresh-Phish Framework**
   - The Fresh-Phish framework is an open-source system designed to build machine-learning models for phishing website detection. It focuses on feature extraction from URLs and employs various machine-learning algorithms to predict phishing sites. This framework addresses the challenge of detecting zero-day phishing attempts by automating feature engineering and model training[3].

**3. GitHub Phishing Detection Projects**
   - Several GitHub projects focus on phishing detection by extracting features from URLs and training machine learning models. For instance, the project by gangeshbaskerr uses features like domain age and URL length to train models such as Decision Trees and Random Forests, aiming to reduce phishing attacks significantly[4].

## Reference list
* [1] https://www.scitepress.org/Papers/2016/59656/59656.pdf
* [2] https://arxiv.org/abs/2407.04732
* [3] https://sist.sathyabama.ac.in/sist_naac/documents/1.3.4/1822-b.e-cse-batchno-287.pdf
* [4] https://github.com/gangeshbaskerr/Phishing-Website-Detection
* [5] https://github.com/Song-Li/cross_browser
* [6] https://seon.io/resources/browser-fingerprinting/
* [7] https://blog.castle.io/9-device-fingerprinting-solutions-for-developers/
* [8] https://fingerprint.com/blog/best-npm-packages-browser-fingerprinting/
