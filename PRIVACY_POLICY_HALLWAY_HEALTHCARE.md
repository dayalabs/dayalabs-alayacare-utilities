# Privacy Policy for Hallway Healthcare - Daya utilities for AlayaCare

**Last Updated:** July 3, 2026

## Overview

Hallway Healthcare - Daya utilities for AlayaCare ("the Extension") is built by Daya Labs exclusively for Hallway Healthcare's AlayaCare environment. This privacy policy explains how we handle information when you use the Extension.

## Information Collection and Use

### What Information We Collect

The Extension **does not collect, store, or transmit any personal information**. Specifically:

- **No Personal Data:** We do not collect names, email addresses, or any personally identifiable information
- **No Health Information:** We do not collect, store, or transmit any patient or health data
- **No Browsing History:** We do not track or record your browsing history
- **No Usage Analytics:** We do not collect analytics or usage statistics
- **No Cookies:** We do not use cookies or similar tracking technologies
- **No Third-Party Sharing:** We do not share any data with third parties because we don't collect any data

### What the Extension Does

The Extension operates entirely within your authenticated AlayaCare session:

1. **Adds a QA button** to eligible client-form pages on Hallway Healthcare's AlayaCare domains
2. **Creates AlayaCare tasks:** QA notes entered by the user are sent directly to AlayaCare's own APIs, on the same AlayaCare site the user is logged into, using the user's existing session — and are stored only in the customer's own AlayaCare system
3. **Updates the form's status** through AlayaCare's own APIs, within the same session

All network requests go to the AlayaCare domain the user is logged into. The Extension makes no external network calls and uses no external servers.

### Permissions Explained

The Extension requests **no browser permissions**. Its content scripts run only on Hallway Healthcare's AlayaCare tenant domains (plus Daya Labs' internal test tenant). The Extension is completely inactive on all other websites.

## Data Storage

The only browser storage used is an optional local diagnostic flag. No user data, notes, or page content are stored by the Extension: QA notes live solely in the customer's AlayaCare system as tasks.

## Third-Party Services

The Extension does not integrate with any third-party services, analytics platforms, or advertising networks.

## Changes to This Privacy Policy

We may update this privacy policy from time to time. We will notify you of any changes by updating the "Last Updated" date at the top of this policy.

## Contact Information

If you have any questions or concerns about this privacy policy, please contact:

**Email:** marc-andre.choquette@dayalabs.com

## Summary

**What We Collect:** Nothing
**What We Share:** Nothing
**What We Store:** An optional local diagnostic flag only
**What We Track:** Nothing

---

## For Chrome Web Store Reviewers

This Extension:

- ✓ Does not collect user data
- ✓ Does not use remote code
- ✓ Does not make external network requests (only same-origin requests to AlayaCare's own APIs, within the user's existing session)
- ✓ Requests no browser permissions
- ✓ Runs content scripts only on Hallway Healthcare's AlayaCare tenant domains and Daya Labs' internal test tenant
- ✓ Has no analytics or tracking
- ✓ Complies with Chrome Web Store policies

**Permissions Justification:**

- `host_permissions` / content-script matches: limited to Hallway Healthcare's AlayaCare tenant domains (hallwayhealthcare.alayacare.com, hallwayhealthcare.staging.alayacare.com, hallwayhealthcare.uat.alayacare.com) and Daya Labs' internal test tenant (dayalabs.uat.alayacare.ca), required to add the QA button to form pages and call AlayaCare's same-origin APIs
