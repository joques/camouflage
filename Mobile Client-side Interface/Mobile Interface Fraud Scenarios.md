# Mobile Interface Fraud Scenarios for Banking Information Theft Detection

## Scenario 1:Phishing via Fake Banking/Ecommerce Websites

Attackers create fake banking/ecommerce websites that look identical to real ones but with slightly different URLs (e.g., chasse.com instead of chase.com). These sites are designed to trick users into entering login credentials and banking information when accessed through mobile browsers, taking advantage of the limited screen space that may hide the full URL from view.


## Scenario 2:Fake Account Opening Sites

Attackers create websites that mimic the account opening process of legitimate bank or ecommerce, tricking users into providing personal and banking information under the guise of opening a new account. Users may be directed to these sites through search engine optimization (SEO) techniques or social media ads.



## Attack Vector

### User Receives a Phishing Link
- Users receive a link via email or social media which looks legitimate.
- User Misspells URL: The user misspells the URL of their banking website and lands on a typosquatted domain.

### User Clicks the Link & Visits the Phishing Site
- Upon clicking, the user is directed to a site that closely resembles a legitimate bank's or ecommerce's account opening page, using similar logos, color schemes and language.
- The user sees a familiar login page and enters their banking information.

### Phishing Attack Happens
- The fake website captures the user's credentials in real time.

## How the Mobile Interface Detects It

### URL Analysis
- When a user navigates to a banking or e-commerce related website, the client-side interface intercepts the URL
- The system extracts domain name features (length, number of special characters, presence of suspicious terms)
- It calculates similarity metrics between the visited domain and known legitimate banking domains
- Suspicious domains trigger initial alert level based on these metrics

### Website Content Analysis
- The client-side script extracts key features from the loaded webpage:
  - HTML structure and form elements
  - JavaScript behavior (especially scripts that capture form inputs)
  - Mobile-specific elements like APK download links
- These features are compiled into a feature vector for real-time analysis

### Machine Learning Classification
- The feature vector is processed through a pre-trained machine learning model
- The model evaluates multiple indicators simultaneously, looking for patterns consistent with phishing attempts
- Classification results determine the threat level (safe, suspicious, or dangerous)

### User Alert Generation
- For high-confidence threats, the interface displays a prominent blocking screen
- For medium-confidence threats, it shows a warning banner with an explanation
- Alerts include specific reasons for the warning (e.g., "This site closely resembles {site names as identified} but has a different domain")
- The user is provided with options: proceed with caution, visit the legitimate site instead, or report the site