# GitHub Free Edition v1.0

Prepared 2026-09-29. This distribution repackages the existing Subtitle Recut Desk v1.0 free application. Its HTML is byte-identical to the previously released Trial HTML; no application behavior, capacity or arithmetic was changed. The new README and free-edition license permit the bounded redistribution and GitHub use described in `LICENSE.txt`. The six synthetic example files are unchanged. The original marketplace Trial ZIP is not included because it carries a different distribution license.

The free application accepts one real SRT, with 5,000 cues, 2 MiB and 100 entered cuts. Both editions include the same two-track synthetic tutorial. The paid Full edition is absent from this repository and this ZIP.

## Existing v1.0 verification

The existing product release was checked with 38 automated tests, an independent 46,656-case interval calculation, and 160 assertions on the finished-browser output ZIP. Those are prior product-release checks, not new tests performed by this repackaging.

Finished HTML was exercised in desktop Chrome served from localhost: synthetic review/export, real SRT and plan import, explicit retained text edits, malformed timestamp and UTF-8 rejection, 5,000/5,001-cue boundary, stale-result clearing and an explicitly zero-byte SRT result. Free edition accepted one real file and rejected two. The supplied example's exact authored decisions produce 5 EN and 6 KO output cues.

Direct `file://` opening, mobile layout, all-browser compatibility, customer data and customer-production correctness remain unverified. Core capacity checks do not establish full-capacity browser performance or measured user speed. No payment, sales, customer uptake or time-saving result is claimed here.

## Distribution verification

Before publication, the staging verifier compares the exact public allowlist, the repackaged ZIP's entries/CRCs, and the HTML/example bytes against the existing source release. Its report stays outside the public package. The public HTML's SHA-256 is `b56c00c04ca31eda1dc44b4dd90661cf275d61fd2e2480f25a8f9b2e2d68a9b9`.

AI-assisted code, interface and documentation. Review captions against the original footage: recorded decisions do not prove that retained words match it.
