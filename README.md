#  PhishGuard

### Rule-Based Phishing Detection and Website Security System

PhishGuard is a web-based cybersecurity application designed to help users identify potentially malicious and phishing URLs. The system analyzes URL characteristics, applies predefined security rules, checks threat-intelligence information, and generates an explainable risk score.

The project focuses on rule-based detection, making the detection process transparent and easier to understand.

---

## Problem Statement

Phishing attacks use deceptive websites and URLs to trick users into revealing sensitive information such as passwords, banking details, and personal data.

Many users cannot easily determine whether a URL is legitimate or suspicious. PhishGuard aims to provide a simple system where users can submit a URL and receive a risk assessment along with the indicators that contributed to the result.

---

## Objectives

* Detect potentially phishing and suspicious URLs.
* Analyze different characteristics of submitted URLs.
* Apply a rule-based detection mechanism.
* Generate an understandable risk score.
* Explain the reasons behind a suspicious classification.
* Maintain scan history for registered users.
* Support blacklist and whitelist management.
* Provide an administrative dashboard.
* Integrate threat-intelligence sources where appropriate.
* Provide a foundation for a browser extension.

---

## Planned Features

### User Features

* User registration and login
* URL scanning
* Risk assessment
* Detection explanation
* Scan history
* Suspicious URL reporting

### Detection Features

* URL structure analysis
* HTTPS analysis
* IP-address detection
* Suspicious keyword detection
* Domain and subdomain analysis
* URL length and character analysis
* Blacklist checking
* Whitelist checking
* Rule-based risk scoring
* Threat-intelligence integration

### Admin Features

* Admin authentication
* User management
* Scan statistics
* Blacklist management
* Whitelist management
* Suspicious URL report management

### Future Features

* Browser extension
* Real-time website warnings
* Additional threat-intelligence integrations
* Email/link scanning

---

## System Architecture

                    User / Browser Extension
                              |
                              v
                       React Frontend
                              |
                              v
                       FastAPI Backend
                              |
                              v
                         URL Analyzer
                              |
                              v
                     Rule-Based Engine
                              |
                    +---------+---------+
                    |                   |
                    v                   v
            Threat Intelligence   Risk Assessment
                    |                   |
                    +---------+---------+
                              |
                              v
                         PostgreSQL
                              |
                              v
                            Result

## Detection Workflow

User submits URL
        |
        v
URL Validation
        |
        v
Feature Extraction
        |
        v
Rule-Based Analysis
        |
        v
Threat Intelligence Check
        |
        v
Risk Assessment
        |
        v
Risk Score + Explanation
        |
        v
Store Scan Result

## Detection Approach

PhishGuard uses a rule-based approach.

The system evaluates characteristics such as:

* HTTPS usage
* URL length
* IP address usage
* Number of subdomains
* Suspicious keywords
* Special characters
* URL encoding
* Domain characteristics
* Blacklist matches
* Whitelist matches
* Threat-intelligence results

Multiple indicators are combined to calculate a risk score.

> The rules and scoring thresholds will be evaluated and adjusted using testing data during development.

---

## Technology Stack

### Frontend

* React.js
* Tailwind CSS

### Backend

* Python
* FastAPI
* Uvicorn

### Database

* PostgreSQL
* SQLAlchemy

### Security

* JWT Authentication
* Password Hashing
* Input Validation

### Detection

* Python Rule-Based Engine
* URL Analysis
* Threat Intelligence

### Browser Extension

* JavaScript
* Manifest V3

### Development & Deployment

* Git
* GitHub
* Docker

---

## Project Structure

phishguard/
│
├── frontend/              # React frontend
│
├── backend/               # FastAPI backend
│
├── database/              # Database-related files and designs
│
├── extension/             # Browser extension
│
├── docs/                  # Project documentation
│   └── diagrams/          # UML and architecture diagrams
│
├── tests/                 # Testing files
│
├── .gitignore
├── README.md
└── LICENSE


## User Roles

### User

A registered user can:

* Scan URLs
* View risk assessments
* View scan history
* Report suspicious URLs

### Administrator

An administrator can:

* Manage users
* Manage blacklist and whitelist entries
* Review reported URLs
* View system statistics

---

## Testing

The system will be evaluated using legitimate and phishing/suspicious URL datasets.

Testing will consider:

* Detection accuracy
* Precision
* Recall
* F1-score
* False positives
* False negatives
* API functionality
* Security and input validation

Actual performance metrics will be added after testing is completed.

---

## Limitations

PhishGuard provides a risk assessment based on predefined rules and available threat-intelligence information. It cannot guarantee detection of every phishing website.

Legitimate websites may occasionally be classified as suspicious, and newly created malicious websites may not always be identified.

---

## Future Scope

Future development may include:

* Browser-based real-time warnings
* Browser extension integration
* Email phishing detection
* QR-code URL scanning
* Additional threat-intelligence sources
* More advanced URL and domain analysis
* Expanded security monitoring



## 👨‍💻 Team

Project: PhishGuard


**Team Members:**

1. Peehu
2. Nandani
3. Karman Vaid
4. Hardik

---

## Disclaimer

PhishGuard is developed as an academic cybersecurity project for educational and research purposes. Detection results should not be treated as a guarantee that a website is safe or malicious.
