🛡️ ScamShield.ng

ScamShield.ng is an accessibility-focused scam detection prototype designed to help Nigerians identify suspicious SMS, WhatsApp, email, and social-media messages before they click links, send money, or share sensitive information.

Disclaimer: This is an educational cybersecurity prototype. Its results are risk assessments, not guarantees. Always verify unusual requests through an organisation's official website, mobile app, branch, or verified telephone number.

Features

Rule-based scam message analysis

Risk score from 0 to 100

Threat classification and explanation

Detection of OTP, PIN, CVV, password, BVN, and NIN requests

Fake bank-verification detection

Investment and Ponzi-scheme warnings

Fake grant, loan, giveaway, lottery, and advance-fee detection

Suspicious-link analysis

WhatsApp impersonation detection

Voice warnings

Large-text and high-contrast modes

Strong visual alerts

Optional family guardian alert through WhatsApp

Local scam reporting and threat statistics

Screenshot preview

Browser-based local storage

Technology

HTML5

CSS3

Vanilla JavaScript

Browser localStorage

Web Speech API

WhatsApp click-to-chat links

The current coded version is contained in one index.html file. No package installation or build process is required.

Run Locally

Clone the repository:

git clone https://github.com/izu500/scamshield-ng.git
cd scamshield-ng

Open index.html in a modern browser.

You can also run a local server:

python -m http.server 8000

Then visit:

http://localhost:8000

Test the Scam Detector

Bank phishing

Dear customer, your bank account has been suspended. Click
https://secure-bank-login.xyz immediately and provide your BVN and OTP
to restore access.

Expected result: High-Risk Scam

Investment scam

Invest ₦20,000 today and receive ₦200,000 guaranteed profit within
24 hours. Limited slots available. Send money now.

Expected result: High-Risk Scam

Fake grant

Congratulations! You have qualified for a CBN grant. Pay a ₦5,000
processing fee and click bit.ly/claim-grant to receive your money.

Expected result: High-Risk Scam

Low-risk comparison

Hello, our family meeting has been moved to Saturday at 10am.
Please call me when you arrive.

Expected result: Low Detected Risk

Use fictional details only. Do not test with real OTPs, passwords, account numbers, BVNs, NINs, card details, or active phishing links.

How Detection Works

ScamShield.ng uses regular expressions and weighted security rules. Each matched indicator adds points to the message's risk score.

Score

Result

0–19

Low Detected Risk

20–39

Caution Required

40–69

Suspicious Message

70–100

High-Risk Scam

Examples of indicators include:

OTP or verification-code requests

Password, PIN, or CVV requests

BVN or NIN requests

Account-blocking threats

Guaranteed returns

Processing-fee demands

Urgency and pressure language

Suspicious or shortened links

WhatsApp “new number” impersonation

The score is capped at 100, and the strongest matched category is shown as the likely threat type.

Privacy

The current version runs in the browser and does not require a backend.

The following may be stored locally on the user's device:

Analysis statistics

Scam reports

Guardian details

Accessibility preferences

Users can remove a saved guardian or select Reset Local Demo Data to clear stored prototype information.

Guardian Alert

When a high-risk message is detected, the user may choose to open a pre-filled WhatsApp alert for a saved trusted contact.

ScamShield.ng does not:

Send the message automatically

Access the user's WhatsApp account

Contact anyone without the user's action

Upload the analysed message to a server

Current Limitations

Detection is based on keywords and regular expressions.

False positives and false negatives are possible.

A low-risk result does not prove that a message is genuine.

Screenshot text is not extracted automatically.

Reports are stored locally and are not sent to authorities.

The prototype does not currently use machine learning or a shared threat database.

Local data may disappear when browser storage is cleared.

Future Improvements

OCR for screenshot text extraction

Machine-learning classification

Nigerian-language support

Secure cloud reporting

Shared threat intelligence

URL reputation checking

Browser extension

Mobile application

Automated test suite

Larger scam-message dataset

Verified reporting integrations

Suggested Repository Structure

scamshield-ng/
├── index.html
├── README.md
├── LICENSE
└── screenshots/
    ├── analyser.png
    ├── dashboard.png
    └── accessibility.png

Screenshots

Create a screenshots folder and add images of the application.

![ScamShield analyser](screenshots/analyser.png)
![Threat dashboard](screenshots/dashboard.png)
![Accessibility controls](screenshots/accessibility.png)

Contributing

Contributions are welcome.

Fork the repository.

Create a branch:

git checkout -b feature/your-improvement

Commit your changes:

git commit -m "Add your improvement"

Push the branch:

git push origin feature/your-improvement

Open a pull request.

Helpful contributions include new scam rules, accessibility improvements, mobile testing, automated tests, privacy reviews, and documentation improvements.

Never publish victims' private information or active malicious links in an issue or pull request.

Reporting Issues

When opening a GitHub issue, include:

Browser and device

Expected result

Actual result

A redacted fictional example

Steps to reproduce the problem

Licence

Choose a licence before publishing the repository publicly. The MIT Licence is commonly used for educational open-source projects.

After adding a LICENSE file, you may use:

This project is licensed under the MIT Licence. See the LICENSE file for details.

Author

Dong

Cybersecurity learner with the 3 Million Technical Talent (3MTT) programme.

Add your preferred portfolio, LinkedIn profile, or professional contact information here.

Mission

ScamShield.ng aims to support a safer digital Nigeria by helping people pause, inspect suspicious messages, protect vulnerable users, and make better security decisions before taking action.

Support the Project

Give the repository a star, test it using safe fictional examples, and share constructive feedback through GitHub Issues.
