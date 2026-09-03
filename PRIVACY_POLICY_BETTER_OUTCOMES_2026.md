# Privacy Policy for Better Outcomes 2026 - Daya utilities for AlayaCare

**Last Updated:** September 2, 2026

## Overview

Better Outcomes 2026 - Daya utilities for AlayaCare ("the Extension") is built by Daya Labs
for demonstration purposes at the Better Outcomes 2026 conference. It is not built for, or
scoped to, any specific customer's AlayaCare tenant. This privacy policy explains how we
handle information when you use the Extension.

## Information Collection and Use

### What Information We Collect

The Extension does not collect analytics, track browsing history, or share any data with
third parties. It does, however, transmit login credentials and identity information you
choose to enter, described precisely below — this Extension is not a "collects nothing"
extension, and this policy names exactly what leaves your browser and where it goes.

- **No Browsing History:** We do not track or record your browsing history.
- **No Usage Analytics:** We do not collect analytics or usage statistics.
- **No Third-Party Sharing:** We do not share any data with third parties. Data you submit
  through the Extension's DayaCloud login feature goes only to DayaCloud, Daya Labs' own
  internal system — never to any other party.

### What the Extension Does

The Extension operates within your authenticated AlayaCare session, plus one feature that
connects to a separate Daya Labs system:

1. **AlayaCare page features:** the Extension reads and adds elements to AlayaCare pages,
   using your existing AlayaCare session. It makes no AlayaCare API requests beyond what a
   logged-in user's browser already can.
2. **DayaCloud login demo:** a card on the AlayaCare home screen, and a button in the
   Extension's own menu, let you log in to DayaCloud (Daya Labs' internal webapp — not
   AlayaCare, and not the customer's own system) against a sandboxed demo tenant. If you
   use this feature:
   - The **email address and password** you enter are sent directly to DayaCloud's
     authentication service to sign you in, including a one-time verification code for
     multi-factor authentication.
   - On a successful login, DayaCloud returns **access, ID, and refresh tokens**, which the
     Extension stores in your browser's temporary session storage (cleared automatically
     when you close the browser — never written to disk, never sent anywhere else).
   - The Extension then makes one authenticated request to DayaCloud to confirm the login,
     which returns your **email address, DayaCloud role names, and permission names** —
     displayed back to you in the Extension, not stored beyond the same temporary session
     storage.
   - This feature is a demo connecting to a seeded sandbox tenant with no real client data.

All AlayaCare-related network requests go to the AlayaCare domain you are logged into. The
DayaCloud login feature's requests go to Daya Labs' own DayaCloud system — the only
external (non-AlayaCare) network destination this Extension ever contacts.

### Permissions Explained

The Extension requests:

- **`tabs`:** used only to read the URL of the currently active tab when the Extension's
  own menu is opened, so the DayaCloud login feature can determine which AlayaCare tenant
  you're using. The Extension does not read your browsing history or any other tab's
  content.
- **`storage`:** used to hold DayaCloud login tokens in temporary, session-only browser
  storage (cleared when the browser closes) after a successful DayaCloud login, and an
  optional local diagnostic flag. No data is written to persistent storage.
- **`host_permissions` for `demo.dayalabs.com`, `demo.staging.dayalabs.com`, and
  `demo.dev1.dayalabs.com`:** required so the DayaCloud login feature can make requests to
  DayaCloud's authentication and identity APIs.

Its content scripts run only on `dayalabs.alayacare.com`, `dayalabs.staging.alayacare.com`,
`dayalabs.uat.alayacare.com`, and `dayalabs.uat.alayacare.ca`. The Extension is completely
inactive on all other websites, other than the DayaCloud requests described above.

## Data Storage

DayaCloud login tokens are held only in `chrome.storage.session` — cleared automatically
when the browser closes, never written to disk, and never accessible outside your own
browser. No AlayaCare data, notes, or page content are stored by the Extension.

## Third-Party Services

The Extension does not integrate with any third-party services, analytics platforms, or
advertising networks. DayaCloud is Daya Labs' own internal system, not a third party.

## Changes to This Privacy Policy

We may update this privacy policy from time to time. We will notify you of any changes by
updating the "Last Updated" date at the top of this policy.

## Contact Information

If you have any questions or concerns about this privacy policy, please contact:

**Email:** marc-andre.choquette@dayalabs.com

## Summary

**What We Collect:** The email/password you enter to log in to DayaCloud (a Daya Labs
system), sent directly to DayaCloud to authenticate you.
**What We Share:** Nothing with any third party. DayaCloud login data goes only to
DayaCloud.
**What We Store:** DayaCloud login tokens, in temporary browser session storage only
(cleared on browser close); an optional local diagnostic flag.
**What We Track:** Nothing.

---

## For Chrome Web Store Reviewers

This Extension:

- ✓ Does not collect analytics or track browsing history
- ✓ Does not use remote code
- ✓ Makes external network requests to `demo.dayalabs.com`, `demo.staging.dayalabs.com`,
  and `demo.dev1.dayalabs.com` (Daya Labs' own DayaCloud system), in addition to
  same-origin requests to AlayaCare's own APIs within the user's existing session
- ✓ Requests `tabs` (read the active tab's URL only, when the Extension's own menu opens)
  and `storage` (session-only token storage)
- ✓ Runs content scripts only on `dayalabs.alayacare.com`, `dayalabs.staging.alayacare.com`,
  `dayalabs.uat.alayacare.com`, and `dayalabs.uat.alayacare.ca`
- ✓ Has no analytics or tracking
- ✓ Complies with Chrome Web Store policies

**Permissions Justification:**

- `host_permissions` / content-script matches: limited to `dayalabs.alayacare.com`,
  `dayalabs.staging.alayacare.com`, `dayalabs.uat.alayacare.com`, and
  `dayalabs.uat.alayacare.ca` for the AlayaCare-page features, plus the three DayaCloud
  demo hosts above for the DayaCloud login feature.
- `tabs`: required to read the active tab's URL so the DayaCloud login feature can
  determine which AlayaCare tenant environment the user is on.
- `storage`: required to hold DayaCloud login tokens in temporary session storage
  (`chrome.storage.session`), cleared automatically on browser close.
