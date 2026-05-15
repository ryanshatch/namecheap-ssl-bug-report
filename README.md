# Namecheap SSL Certificate Quantity Validation Bug

## Summary

In July 2025, I discovered a logic flaw in Namecheap's GitHub Student promo workflow that allowed a user to request multiple PositiveSSL certificates by increasing the quantity field during checkout. Despite the promo being advertised as limited to one certificate per code, the system allowed quantities greater than one to be added and processed leaving the total sum all at \$0.00.

I manually reproduced the issue using Namecheap’s web UI, without automation or scripting. While I considered building a tool to automate the exploitation of this flaw, I chose to report it responsibly instead.

> *This is a high-level overview only. Full technical details will be shared post-remediation.*

## Impact

* Unlimited free PositiveSSL certificate generation
* Financial impact to Namecheap and Sectigo (the CA)
* Potential for abuse in phishing, fraud, or automation scenarios if weaponized

## Disclosure Timeline

* **2025-07-24** – Vulnerability discovered during routine testing
* **2025-07-26** – Reported to Namecheap via direct email to their security team (not through HackerOne)
* **As of 2025-07-27** – No confirmation of remediation, and the vulnerability still appears to be live

## Ethical Statement

* No third-party data was accessed
* No automation was used to exploit the bug
* All certificates were issued only for my own personal, test-use domains
* I disclosed this issue in good faith within 72 hours of discovery

## Technical Notes (Delayed Disclosure)

To avoid enabling active abuse of this vulnerability, I am intentionally omitting reproduction steps, screenshots, and any code or payload details until the issue is confirmed to be patched.

Once fixed, I will publish the original certificate ZIP metadata and redacted screenshots of the activation UI.

## Future Updates

This report will be updated to include:

* Confirmation of fix (if/when provided by Namecheap)
* Optional CVE ID or public vulnerability ID if accepted
* Proof-of-concept in a separate branch after safe disclosure window

## Attribution

Discovered and responsibly disclosed by **[Ryan Hatch](https://github.com/ryanshatch)**

---

## Repository Structure (Planned)

```ps
namecheap-ssl-quantity-validation-bug/
├── README.md                  ← Public summary and timeline
├── LICENSE                    ← Open source license
├── docs/
│   └── timeline.md            ← Detailed disclosure timeline
├── poc/                       ← Proof‑of‑concept code (private branch until it is patched)
│   └── [redacted for now]
```

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).
