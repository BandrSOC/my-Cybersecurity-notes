# Phishing Analysis Fundamentals 🎣

## Concept

* Phishing is when attackers trick users into giving sensitive info through fake emails 🎣
* It’s a mix of technical tricks + human manipulation (social engineering)
* As an analyst, I don’t trust the email — I verify what’s behind it

## Key Points

* Email = username + domain → domain is what really matters 🧠
* SMTP sends, DNS finds, IMAP sync device, POP3 download on a single device 📩
* Headers reveal the real source (IP, servers, auth results)
* Links can lie → always check the actual URL 🔗
* Base64 = encoding (hiding), not encryption 🔐
* Red flags: urgency, threats, weird domains, fake branding 🚨

## Real SOC Use

* Compare the sender domain with what it claims to be
* Check headers → originating IP + SPF/DKIM results
* Hover over links → does the URL match?
* Look for pressure tactics like “act now” or “account suspended”
* Analyze attachments → especially encoded or unexpected files

## Tools

* CyberChef → decode Base64 / inspect hidden data

## Example

* Email says “PayPal Alert” but link goes to paypal-secure-login.xyz → obvious phishing

## What I Learned

* Never trust the display name — always check the domain
* Headers tell the truth, the email body can lie
* Phishing is more about psychology than hacking
* Thinking like a SOC analyst = question everything before trusting it
