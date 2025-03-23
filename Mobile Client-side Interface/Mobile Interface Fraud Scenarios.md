# Client-side Detection of  Banking Information Theft Detection

## Overview

Scammers exploit mobile users' limited screen visibility and trust in familiar interfaces to launch phishing attacks. A client-side extension can mitigate these threats by analyzing URLs, website content, and behavior, leveraging machine learning for real-time fraud detection. The extension will feature content scripts for data extraction, a background script for ML processing, and an intuitive user interface for alerts. Testing on mobile devices ensures compatibility. 



## Scenario 1:Phishing via Fake Banking/Ecommerce Websites

Phishing through fake banking or e-commerce websites involves attackers creating deceptive sites that closely resemble legitimate platforms. These fraudulent sites often use slightly altered URLs, such as typosquatting (e.g., "chasse.com" instead of "chase.com"), to trick users into entering login credentials, banking details, or payment information. The limited screen space on mobile devices makes it harder for users to detect subtle URL differences, increasing the risk of falling victim to these attacks.


## Scenario 2:Fake Account Opening Sites

Attackers create fake websites that closely resemble legitimate banking or e-commerce platforms, tricking users into providing personal and financial information under the pretense of opening a new account. These fraudulent sites often appear in search results through SEO manipulation or are promoted via social media ads, making them seem credible to unsuspecting users.


## Attack Vector

1. **Typosquatting & Homograph Attacks**  
   - Attackers register domain names that are subtly misspelled or visually similar to legitimate websites (e.g., chasse.com instead of chase.com).  
   - They may also use non-Latin characters that appear identical to Latin letters.

2. **User Receives a Phishing Link**  
   - The user gets an email, SMS, or push notification containing a fraudulent link that appears genuine.  
   - Example: "Your Bank A account is locked—verify at BankA.com" (with a slight variation in the URL).  

3. **User is Directed to the Fake Site**  
   - The user clicks a misleading link from a search engine result, social media ad, or sponsored post.  
   - Example: An ad stating, "Open a Shop A account today and get 50% off on your first purchase " or a search query like “Open Bank A account” leading to a fake site through SEO manipulation.  

4. **User Visits the Phishing Site:**  
   - The fake website mimics the legitimate platform’s design, logos, and interface to create a false sense of trust.  
   - The site prompts users to enter login credentials, payment details, or other sensitive information.  

5. **Phishing Attack Execution:**  
   - Once the user submits their data, the fraudulent site captures it in real time.  
   - Attackers use the stolen information for unauthorized transactions, identity theft, or further social engineering scams.

## How the Extension Will Detect Fraudulent Websites 

### URL and Domain Analysis 
- The mobile extension examines URLs when a user visits a banking or e-commerce website.  
- It extracts domain-level features, including:  
  - **Domain age** – Checks how recently the domain was registered (newly registered domains are often suspicious).  
  - **Character patterns** – Detects unusual symbols, misspellings, or deceptive subdomains.  
  - **HTTPS verification** – Identifies if the site lacks SSL/TLS encryption, a common red flag for phishing sites.  
- The extracted features are compiled into a feature vector for real-time analysis.  
- The system calculates domain similarity to known legitimate websites (e.g., detecting that chasse.com closely resembles chase.com).  
- If the domain is flagged as suspicious, the extension triggers an immediate user alert.  

###  Website Content Analysis
- The extension scans and extracts key elements from the webpage to detect fraudulent behavior:  
  - **HTML structure & form elements** – Identifies suspicious login forms or hidden input fields designed to capture sensitive data.  
  - **JavaScript behavior** – Monitors scripts that record keystrokes or manipulated form inputs.  
  - **Mobile-specific elements** – Flags unusual mobile behaviors, such as forced APK downloads or deceptive pop-ups.  
- These extracted elements are processed into a feature vector for real-time machine learning analysis, helping classify the site as safe, suspicious, or malicious.


## Machine Learning Model 
- The feature vector is processed through a pre-trained machine learning model, which analyzes the extracted data in real-time.  
- The model simultaneously evaluates multiple indicators, such as domain anomalies, content structure, and suspicious JavaScript behavior, to identify patterns consistent with phishing attempts.  
- Based on these patterns, the model classifies the threat into one of three categories:  
  - **Safe**  
  - **Suspicious**  
  - **Dangerous**  

## User Alert Generation
- **High-Confidence Threats:** For severe threats, the interface displays a prominent red warning sign.
- **Medium-Confidence Threats:** A warning banner appears, providing an explanation of the potential risk.  
- **Alert Details:** Alerts include specific reasons for the warning, such as:  
  - "This site closely resembles {site names identified} but uses a different domain."  
- **User Options:** The user is given clear choices:  
  - Proceed with caution 
  - Report the site for further analysis