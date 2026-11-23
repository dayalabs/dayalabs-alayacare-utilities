# Privacy Policy for AccordCare - Daya utilities for AlayaCare

**Last Updated:** November 20, 2026

## Overview

AccordCare - Daya utilities for AlayaCare ("the Extension") is built by Daya Labs exclusively for AccordCare's AlayaCare environment. This privacy policy explains how we handle information when you use the Extension.

## Information Collection and Use

### What Information We Collect

The Extension **does not collect any personal information, and sends nothing to Daya Labs or any other party**. Everything it reads stays between your browser and AccordCare's own AlayaCare site. Specifically:

- **No Personal Data sent to us:** The Extension never sends names, email addresses, or any other personally identifiable information to Daya Labs or any third party
- **No Health Information sent to us:** The Extension reads claim and billing data from AlayaCare, including the client's name and the payer (below), to show it on the page and in exports you choose to make. It sends none of it to Daya Labs or any third party
- **No Browsing History:** We do not track or record your browsing history
- **No Usage Analytics:** We do not collect analytics or usage statistics
- **No Cookies:** The Extension sets no cookies and uses no tracking technologies; its requests carry the AlayaCare session the browser already holds
- **No Third-Party Sharing:** We do not share any data with third parties because we don't collect any data

### What the Extension Does

The Extension operates entirely within your authenticated AlayaCare session, and only reads from AlayaCare: it creates, changes or deletes nothing there.

1. **Journal entries panel:** on a Medicaid claim's page and on a service line's transactions page, the Extension reads the claim, its service lines and their accounting transactions from AlayaCare's own APIs, and shows the general-ledger entries those transactions made: by account, and as a journal (dates, transaction type, payment number, memo, the name of the AlayaCare user who recorded each transaction, GL accounts, debits and credits)
2. **Export:** from the Journal entries panel, you can choose to export what it shows:
   - **CSV:** a file downloaded to your computer, with the claim number and version, service lines and the journal's rows
   - **PDF:** a print view opened in the browser's print dialog, which you can save as a PDF on your computer. Its header shows the claim number, the **client's name** and the **payer**, the service lines covered and the export time

   The Extension builds both files inside your browser and sends them nowhere. Once saved, they are files on your computer like any other, under your organization's own data-handling rules
3. **Find claim:** a button in AlayaCare's top bar opens a search box. What you type is sent to AlayaCare's own Medicaid claim listing, which matches it against claim numbers and internal control numbers (ICN, the number the payer assigns); when it is all digits, it is also looked up as a claim id. Both lookups go to the same AlayaCare site you are logged into. The matching claims are listed with their number, version, ICN, client name, payer and status, and which of those the search matched. Each result links to the claim's page; a copy-link button copies that page's address to your clipboard

All network requests go to the AlayaCare domain the user is logged into. The Extension makes no external network calls and uses no external servers.

### Permissions Explained

The Extension requests **no browser permissions**. Its content scripts run only on AccordCare's AlayaCare tenant domains (plus Daya Labs' internal test tenant). The Extension is completely inactive on all other websites.

## Data Storage

The Extension stores no claim records (no client names, amounts or journal entries) and sends nothing anywhere. What it does keep on the device is limited to AlayaCare ids for the remembered view and, when something fails, error details in the browser's developer console:

- **The panel's selected view** ("By account" or "Journal"), in the browser tab's session storage (`sessionStorage`), with the AlayaCare ids of the page it was picked on (funder, claim and, on a service line's page, the service line). One entry, overwritten by the next choice, and cleared by the browser when the tab is closed
- **Optional diagnostic flags**, which the Extension only reads, never writes. With one on, the Extension also writes diagnostic details (such as a Find claim search's text and result count) to the browser's developer console
- **Error messages in the developer console:** whether or not a flag is on, when a Find claim search or a copy-link fails, the Extension writes the error to the browser's developer console. A failed search's error includes the search text and AlayaCare's error response. Like the diagnostic details, these stay on the device

Exported CSV and PDF files are saved on your computer by your own action, as described above.

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
**What We Store:** The panel's selected view, in the tab's session storage (the Extension only reads the optional diagnostic flags). Exports are files you save on your own computer
**What We Track:** Nothing

---

## For Chrome Web Store Reviewers

This Extension:

- ✓ Does not collect user data
- ✓ Does not use remote code
- ✓ Does not make external network requests (only same-origin, read-only requests to AlayaCare's own APIs, within the user's existing session)
- ✓ Requests no browser permissions
- ✓ Runs content scripts only on AccordCare's AlayaCare tenant domains and Daya Labs' internal test tenant
- ✓ Has no analytics or tracking
- ✓ Complies with Chrome Web Store policies

**Permissions Justification:**

- Content-script matches (no `host_permissions` declared): limited to AccordCare's AlayaCare tenant domains (accordcare.alayacare.com, accordcare.staging.alayacare.com, accordcare.uat.alayacare.com) and Daya Labs' internal test tenant (dayalabs.uat.alayacare.ca), required to add the Journal entries panel to Medicaid claim and service-line pages, add the Find claim button to the top bar, and call AlayaCare's same-origin APIs
- No `downloads` permission: the CSV export is a link to a file built in the page, which the browser downloads like any other; the PDF goes through the browser's own print dialog
