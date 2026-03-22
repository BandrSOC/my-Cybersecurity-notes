# Phishing Analysis Fundamentals 🎣

## Concept

* Phishing is when attackers trick users into giving sensitive info through fake emails 🎣
* It combines social engineering (manipulating people) + technical tricks
* My job is to verify if the email is legit by checking both visible content and hidden data

## Key Points

* Email = username + @ seperate username from domain → domain is the real identity 🧠
* SMTP (Simple Mail Transfer Protocol) → sends emails
* DNS (Domain Name System) → finds the recipient’s mail server
* IMAP (Internet Message Access Protocol) → syncs emails across devices
* POP3 (Post Office Protocol v3) → downloads emails to one device
* Headers show real path (IP, servers, authentication results)
* SPF (Sender Policy Framework) → checks if sender IP is allowed for that domain
* DKIM (DomainKeys Identified Mail) → verifies email wasn’t modified in transit
* DMARC (Domain-based Message Authentication) → tells how to handle failed SPF/DKIM
* Base64 → encoding method used to hide content, not secure it 🔐

## Real SOC Use

* Check sender domain vs claimed company
* Analyze headers → originating IP + SPF/DKIM/DMARC results
* Hover over links → compare displayed vs actual URL 🔗
* Look for urgency or fear tactics (account locked, act now) 🚨
* Inspect attachments → especially encoded or unexpected files
* Check for domain tricks (typos, extra words, subdomains)

## Tools

* CyberChef → decode Base64 and inspect hidden data

## Example

* Email claims Microsoft but SPF fails and link goes to microsoft-login-secure.net → phishing

## What I Learned

* The domain and headers matter more than the email appearance
* SPF/DKIM help verify if the email is legit or spoofed
* Attackers rely on users not checking details
* Real SOC work = verify source, analyze behavior, don’t trust surface-level info

