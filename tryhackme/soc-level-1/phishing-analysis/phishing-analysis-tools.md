# Phishing Emails in Action

## Concept

* This room is about analyzing real phishing emails and understanding how attackers trick users in practice
* Instead of just theory, I’m looking at real examples (links, attachments, fake brands)
* The goal is to identify what’s suspicious and how attackers try to get interaction

## Key Points

* Phishing emails usually create urgency (order problem, account locked, shipment issue)
* Links can look normal but redirect somewhere else
* Buttons in emails often hide the real URL behind HTML
* Tracking links are used to detect if the victim clicked
* Attachments (PDF, DOC, XLS) can contain malware or redirect to malicious pages
* Attackers impersonate trusted companies (Netflix, Apple, DHL)
* The display name is not important — the actual domain is what matters

## Detection

* Hover over links or buttons and check the real URL
* Look for redirects or unusual parameters in URLs
* Compare sender email domain with the company name
* Be careful with unexpected attachments
* Watch for urgency + action requests (click, download, login)
* Check file types and extensions carefully

## Tools

* URL Expander → reveal real destination of shortened links
  [https://checkshorturl.com/](https://checkshorturl.com/)

* CyberChef → decode or inspect hidden/encoded data
  [https://gchq.github.io/CyberChef/](https://gchq.github.io/CyberChef/)

## Example

* Email says “Track your DHL package” but the link goes through a tracking URL that redirects → attacker is monitoring clicks

## What I Learned

* Phishing emails can look very normal, not obvious
* Links and attachments are the main attack points
* I should always verify the real destination, not trust what I see
* Attackers depend more on user behavior than technical exploits
