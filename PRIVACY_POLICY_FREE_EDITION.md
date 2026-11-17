# Privacy Policy for Free Edition - Daya utilities for AlayaCare

**Last Updated:** November 17, 2026

## Overview

Free Edition - Daya utilities for AlayaCare ("the Extension") is a free Chrome extension
built by Daya Labs for home care agencies that use AlayaCare. It adds a few features to
AlayaCare pages. This privacy policy explains what information the Extension handles, what
leaves your browser, and where it goes.

## Information Collection and Use

### What Information We Collect

The Extension sends Daya Labs **daily usage statistics**. It collects nothing else.

Once a day, for each AlayaCare site you use it on, the Extension sends Daya Labs:

- a random identifier, created by the Extension for this browser and that AlayaCare site.
  It is not linked to you, your AlayaCare account, or your identifier on any other
  AlayaCare site.
- the Extension's version
- the AlayaCare site's address (for example `youragency.alayacare.com`), with no page path
- the date the statistics cover, and the browser's offset from UTC on that date
- how many times each feature was used that day, and how many AlayaCare requests failed
  (a server error, or no connection)

The statistics never contain names, client or visit details, claim or visit numbers,
search terms, page content, or anything about your AlayaCare account. As with any request
on the internet, our servers see your IP address when the statistics arrive. It is used
only to protect the service from abuse (rate limiting) and is not stored with the
statistics.

Daya Labs uses the statistics to understand which features are used, on which AlayaCare
sites, and to notice when a feature starts failing. They are seen only by Daya Labs staff.

The statistics are always on. Uninstalling the Extension stops them.

- **No Browsing History:** We do not track or record your browsing history. The only site
  address sent is the AlayaCare site's, as described above.
- **No Third-Party Sharing:** We do not sell or share any data with third parties.

### What the Extension Does

The Extension runs only on AlayaCare sites, inside your existing AlayaCare session:

1. **Claim versions:** on a Medicaid claim page, a **Versions (N)** button lists every
   version of the claim.
2. **Claim search:** a **Find visit or claim** box in AlayaCare's top bar searches claims
   by id or number, and looks up a visit by its exact id.
3. **Visit search:** on a client's Scheduling calendar, a **Find Visit by ID** button
   finds and highlights a visit shown on the calendar.
4. **Bookmarks:** a bookmark button in AlayaCare's top bar saves AlayaCare pages to come
   back to, grouped by category.
5. **Export descriptions:** in the **Add Accounting Export** popup, a box says what the
   chosen export type produces.
6. **Request more features:** a button in AlayaCare's top bar, and in the Extension's own
   popup, opens the Daya Labs contact page (https://dayalabs.com/en/contact/) in a new tab
   when you click it. The link sends nothing, and it does not tell dayalabs.com which
   AlayaCare page you came from.

The AlayaCare features read and add elements to AlayaCare pages. Claim versions and claim
search call AlayaCare's own APIs on the AlayaCare site you are logged into, using your
existing session. They can do nothing a logged-in user's browser cannot already do, and
their results are shown to you and not sent anywhere else.

The Extension makes network requests to two places only:

- the AlayaCare site you are using, for the features above
- `internal.dayalabs.com`, Daya Labs' own server, for the daily usage statistics

### Permissions Explained

The Extension requests one permission:

- **`storage`:** used to save your bookmarks, and to keep the usage statistics until they
  are sent.

It requests no `host_permissions`. Its content scripts run only on AlayaCare sites:
`*.alayacare.com` and `*.alayacare.ca`, including their `staging` and `uat` sites. The
Extension does nothing on any other website.

## Data Storage

The Extension stores the following in your browser:

- **Bookmarks**, in Chrome's synced extension storage (`chrome.storage.sync`). Each one
  holds the title you give it (filled in from the page's title, which you can change), the
  AlayaCare page's path (for example `/#/clients/4821`), its category, and when you saved
  it. Chrome keeps them with your Chrome profile, so if you sign in to Chrome with sync on,
  they follow you to your other computers. Bookmarks are never sent to Daya Labs or to
  AlayaCare.
- **Usage statistics waiting to be sent**, in Chrome's local extension storage
  (`chrome.storage.local`). For each AlayaCare site, this holds the random identifier, the
  dates it was last used and last sent, and the daily counts not yet sent. A day's counts
  are deleted once they are sent, or after 30 days if they never could be. An AlayaCare site
  not used for 90 days is removed, identifier included.
- **A visit lookup handoff**, in the AlayaCare site's `localStorage`. When a visit found
  with claim search opens in a new tab, its visit id and date are passed to that tab this
  way. The entry is cleared once used, and ignored after a minute.
- **Optional diagnostic flags**, in the AlayaCare site's `localStorage`, only if you turn
  them on yourself.

## Third-Party Services

The Extension does not integrate with any third-party services, analytics platforms, or
advertising networks. The usage statistics go only to Daya Labs' own server.

## Changes to This Privacy Policy

We may update this privacy policy from time to time. We will notify you of any changes by
updating the "Last Updated" date at the top of this policy.

## Contact Information

If you have any questions or concerns about this privacy policy, please contact:

**Email:** engineering@dayalabs.com

## Summary

**What We Collect:** Daily usage statistics: a random identifier, the Extension's version,
the AlayaCare site's address, the date, and how many times each feature was used or an
AlayaCare request failed.
**What We Share:** Nothing with any third party.
**What We Store:** In your browser: your bookmarks, usage statistics not yet sent, and a
short-lived visit lookup handoff. On Daya Labs' server: the daily usage statistics.
**What We Track:** Daily counts of feature use per AlayaCare site. Nothing from the pages
themselves.

---

## For Chrome Web Store Reviewers

This Extension:

- ✓ Does not use remote code
- ✓ Does not track browsing history
- ✓ Sends daily usage statistics (feature counts, the extension version, the AlayaCare
  site's hostname, and a random per-site identifier) to `internal.dayalabs.com`, Daya
  Labs' own server
- ✓ Otherwise makes only same-origin requests to AlayaCare's own APIs, within the user's
  existing session
- ✓ Requests only the `storage` permission, and no `host_permissions`
- ✓ Runs content scripts only on `*.alayacare.com` and `*.alayacare.ca`, including their
  `staging` and `uat` sites
- ✓ Complies with Chrome Web Store policies

**Permissions Justification:**

- Content-script matches: limited to AlayaCare's own domains, `*.alayacare.com` and
  `*.alayacare.ca`, where the features add their buttons and call AlayaCare's same-origin
  APIs.
- `storage`: required to save the user's bookmarks (`chrome.storage.sync`) and to hold
  usage statistics until they are sent (`chrome.storage.local`).
