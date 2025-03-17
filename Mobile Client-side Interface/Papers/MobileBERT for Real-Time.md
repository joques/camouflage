- **Title:** PhishLang: A Lightweight, Client-Side Phishing Detection Framework using MobileBERT for Real-Time, Explainable Threat Mitigation 
- **Authors:** Sayak Saha Roy and Shirin Nilizadeh 
- **Digital Object Identifier:** https://doi.org/10.48550/arXiv.2408.05667
- **Year:** 2024

## Abstract

In this paper, we introduce PhishLang, an open-source, lightweight language model specifically designed for phishing website detection through contextual analysis of the website. Unlike traditional heuristic or machine learning models that rely on static features and struggle to adapt to new threats, and deep learning models that are computationally intensive, our model leverages MobileBERT, a fast and memory-efficient variant of the BERT architecture, to learn granular features characteristic of phishing attacks. PhishLang operates with minimal data preprocessing and offers performance comparable to leading deep learning anti-phishing tools, while being significantly faster and less resource-intensive. Over a 3.5-month testing period, PhishLang successfully identified 25,796 phishing URLs, many of which were undetected by popular antiphishing blocklists, thus demonstrating its potential to enhance current detection measures. Capitalizing on PhishLang's resource efficiency, we release the first open-source fully client-side Chromium browser extension that provides inference locally without requiring to consult an online blocklist and can be run on low-end systems with no impact on inference times. Our implementation not only outperforms prevalent (server-side) phishing tools, but is significantly more effective than the limited commercial client-side measures available. Furthermore, we study how PhishLang can be integrated with GPT-3.5 Turbo to create explainable blocklisting -- which, upon detection of a website, provides users with detailed contextual information about the features that led to a website being marked as phishing.


## **1. Problem & Objective**
Phishing remains a major cybersecurity threat, with attackers constantly evolving their methods. 
**PhishLang** is designed to tackle phishing detection challenges by:
- Replacing static heuristic-based detection with contextual language analysis of phishing websites.
- Overcoming deep learning model limitations (high computational costs and reliance on centralized servers).
- Enhancing real-time phishing detection on client devices with MobileBERT, a lightweight model optimized for speed and memory efficiency
- Deploying a privacy-friendly, fully client-side browser extension that runs without needing external databases or blocklists.



## **2. Methodology**
The authors introduce PhishLang, which detects phishing attacks using:
1. **MobileBERT for Language Analysis**  
   - Extracts key linguistic and structural patterns in website source code to detect phishing.  
   - Requires minimal preprocessing and uses significantly less memory than traditional deep learning models.  

2. **HTML Source Code Parsing**  
   - Extracts only actionable HTML tags relevant to phishing, such as:
     - `<form>`, `<input>`, `<button>` (used for credential theft)
     - `<meta>`, `<iframe>`, `<script>` (used for malicious redirects and hidden elements)
     - `<a>`, `<title>`, `<footer>` (used for misleading content)
   - This reduces input size, improving training and inference speed.

3. **Dataset**  
   - Uses PhishPedia dataset (30K phishing, 30K benign websites).  
   - Evasion-aware: Categorized into behavioral JS evasions, clickjacking, DOM manipulations, and text encoding attacks.
   - Augmented with adversarial phishing techniques to enhance robustness.

4. **Model Selection**  
   - Benchmarked MobileBERT against various language models:
     - MobileBERT (best performance, F1-score: 0.96, Memory usage: 74MB, Inference time: 0.39s)
     - LLaMA-2 (better accuracy but 4,873MB memory and 33.71s inference time, impractical for real-time detection)
     - GPT-2, T5, and FastText (lower accuracy)
   - MobileBERT chosen for best balance of speed, accuracy, and resource efficiency.

5. **Real-Time Detection Framework**  
   - Monitors live SSL certificate streams (Certstream)for new phishing threats.  
   - Scanned 42.7M domains (flagged 25,796 phishing websites over 3.5 months).  
   - Outperformed existing blocklists, catching threats that Google Safe Browsing and Microsoft SmartScreen missed.



## **3. Key Findings**
1. **Superior Detection Performance**  
   - F1-score: 0.96, better than DistilBERT (0.94), TinyBERT (0.85), and traditional ML models.
   - Outperformed commercial anti-phishing solutions like Google Safe Browsing.

2. **Adversarial Robustness**  
   - Tested against 16 realistic adversarial phishing attacks, such as:
     - JavaScript obfuscation (hiding malicious code)
     - Clickjacking (invisible login elements)
     - DOM manipulations (dynamically generated phishing content)
   

3. Explainability with GPT-3.5 Turbo  
   - Instead of just blocking sites, PhishLang explains why they are suspicious.
   - Uses LIME-based feature attribution to extract the top 3 phishing indicators.
   - Generates human-readable warnings (e.g., "Fake login form," "Misleading security indicators," "Suspicious JavaScript execution").

4. **Client-Side Efficiency & Privacy**  
   - Implemented as a lightweight Chromium browser extension.
   - Fully client-side, no external API calls or blocklists.
   - Runs on low-end devices without performance impact.

