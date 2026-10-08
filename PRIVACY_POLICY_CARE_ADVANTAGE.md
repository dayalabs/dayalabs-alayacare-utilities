# Privacy Policy for Care Advantage - Daya utilities for AlayaCare

**Last Updated:** October 8, 2026

## Overview

Care Advantage - Daya utilities for AlayaCare ("the Extension") is built by Daya Labs exclusively for Care Advantage's AlayaCare environment. This privacy policy explains how we handle information when you use the Extension.

## Information Collection and Use

### What Information We Collect

The Extension **does not collect any personal information, and sends nothing to Daya Labs or any other party**. Everything it reads or sends stays between your browser and Care Advantage's own AlayaCare site. Specifically:

- **No Personal Data sent to us:** The Extension never sends names, email addresses, or any other personally identifiable information to Daya Labs or any third party. The employee's name and status, read from AlayaCare (below), are used only inside the form
- **No Health Information:** The Extension does not read patient or health data, and sends none to Daya Labs or any third party
- **No Browsing History:** We do not track or record your browsing history
- **No Usage Analytics:** We do not collect analytics or usage statistics
- **No Cookies:** The Extension sets no cookies and uses no tracking technologies; its requests carry the AlayaCare session the browser already holds
- **No Third-Party Sharing:** We do not share any data with third parties because we don't collect any data

### What the Extension Does

The Extension operates entirely within your authenticated AlayaCare session:

1. **Replaces the Terminate action on employee profiles** (the ⋯ menu's Terminate item, and choosing Terminated in the Employee Info status field) with a Daya Labs termination form, on Care Advantage's AlayaCare domains
2. **Reads the employee's record** from AlayaCare's own Employee API, using only the name and current status, to show who is being terminated and to check whether they are already terminated
3. **Terminates the employee:** when the user submits the form, the termination reason, the reason's HR code, whether the employee is eligible for rehire, the termination date, the last day worked and any notes entered by the user are sent directly to AlayaCare's own Employee API, on the same AlayaCare site the user is logged into, using the user's existing session. The Extension writes them only to the customer's own AlayaCare system, as the employee's termination note. Care Advantage's HR integration, a separate service operated by Daya Labs for Care Advantage and not part of the Extension, reads them from there

All network requests go to the AlayaCare domain the user is logged into. The Extension makes no external network calls and uses no external servers.

### Permissions Explained

The Extension requests **no browser permissions**. Its content scripts run only on Care Advantage's AlayaCare tenant domains (plus Daya Labs' internal test tenant). The Extension is completely inactive on all other websites.

## Data Storage

The Extension writes nothing to browser storage; it only reads an optional diagnostic flag. No user data, termination details, or page content are stored by the Extension: termination details are written only to the customer's AlayaCare system, as the employee's termination note. With the diagnostic flag on, the Extension also writes the details it sends to the browser's developer console; they stay on the device.

## Third-Party Services

The Extension does not integrate with any third-party services, analytics platforms, or advertising networks.

## Changes to This Privacy Policy

We may update this privacy policy from time to time. We will notify you of any changes by updating the "Last Updated" date at the top of this policy.

## Contact Information

If you have any questions or concerns about this privacy policy, please contact:

**Email:** engineering@dayalabs.com

## Summary

**What We Collect:** Nothing
**What We Share:** Nothing
**What We Store:** Nothing (the Extension only reads an optional diagnostic flag)
**What We Track:** Nothing

---

## For Chrome Web Store Reviewers

This Extension:

- ✓ Does not collect user data
- ✓ Does not use remote code
- ✓ Does not make external network requests (only same-origin requests to AlayaCare's own APIs, within the user's existing session)
- ✓ Requests no browser permissions
- ✓ Runs content scripts only on Care Advantage's AlayaCare tenant domains and Daya Labs' internal test tenant
- ✓ Has no analytics or tracking
- ✓ Complies with Chrome Web Store policies

**Permissions Justification:**

- Content-script matches (no `host_permissions` declared): limited to Care Advantage's AlayaCare tenant domains (careadvantage.alayacare.com, careadvantage.staging.alayacare.com, careadvantage.uat.alayacare.com) and Daya Labs' internal test tenant (dayalabs.uat.alayacare.ca), required to replace the Terminate action on employee profiles with the Daya Labs termination form and call AlayaCare's same-origin Employee API
