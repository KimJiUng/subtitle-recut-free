# GitHub Free Edition v1.1.1

Fixes a review-interface bug where switching a retained segment after typing could restore an older caption draft. The latest text now survives segment changes, including a blank draft. Explicit confirmation is still required for the newly selected segment. Timing rules, checkpoint format, free one-track capacity and license permissions are unchanged.

Existing v1.1 checkpoints remain supported. Regression, browser and final public delivery evidence are recorded separately; this patch is not evidence of customer demand or revenue.

## Historical v1.1 notes

# GitHub Free Edition v1.1

Prepared 2026-09-30 for the existing free distribution. This version adds explicit local review-checkpoint save/resume to the one-real-track application. Partial drafts and confirmed decisions can be saved with original subtitles and cuts, then resumed after fresh original-timeline acknowledgement. A failed import preserves the previous workspace; new edits/imports override older reads.

Checkpoint validation rejects unsupported schemas/versions, duplicate/unknown fields, malformed source metadata, stale source/fragment references and edition/byte/cue/cut-limit violations. Analysis and outputs are recomputed. Checkpoint JSON is limited to 32 MiB, with the normal 2 MiB/5,000-cue source and 100-cut limits. The built-in synthetic demo cannot be checkpointed; the original example SRTs can be imported normally for the new pause/resume exercise. Checkpoints contain subtitle content and unfinished edits and are not authenticated documents.

The source product's 48 automated tests passed, including partial/full uninterrupted-output equivalence, exact original cue-number/text preservation, import atomicity and stale-reader tests. An independent source review and separate adversarial probes found no consequential defect. Finished v1.1 HTML was checked in desktop Chrome served from localhost: the Free edition rejected a two-track checkpoint, saved and resumed one imported track, and required fresh acknowledgement. Full-edition checks separately preserved partial Unicode drafts and confirmed choices, retained the workspace after malformed JSON, and produced SRT downloads byte-identical to independently computed expected output. These checks do not establish direct file opening, all-browser compatibility, customer demand or measured time savings. Prior v1.0 browser observations remain historical below.

The GitHub package uses the dedicated free-edition license, not the marketplace package license. Only the license's package/application filenames were updated to v1.1; its grants and restrictions are unchanged. Its Trial HTML must match the v1.1 product build; the paid Full HTML must remain absent. Final public package/hash checks are separate distribution evidence.

The v1.1 Trial HTML SHA-256 is `49848d9b7c1a41b2e5ca71a9a03d611e5013610cd4893620c17680d0616be529`.

## Historical GitHub Free Edition v1.0

Prepared 2026-09-29. This distribution repackages the existing Subtitle Recut Desk v1.0 free application. Its HTML is byte-identical to the previously released Trial HTML; no application behavior, capacity or arithmetic was changed. The new README and free-edition license permit the bounded redistribution and GitHub use described in `LICENSE.txt`. The six synthetic example files are unchanged. The original marketplace Trial ZIP is not included because it carries a different distribution license.

The free application accepts one real SRT, with 5,000 cues, 2 MiB and 100 entered cuts. Both editions include the same two-track synthetic tutorial. The paid Full edition is absent from this repository and this ZIP.

## Historical v1.0 product verification

The existing product release was checked with 38 automated tests, an independent 46,656-case interval calculation, and 160 assertions on the finished-browser output ZIP. Those are prior product-release checks, not new tests performed by this repackaging.

Finished HTML was exercised in desktop Chrome served from localhost: synthetic review/export, real SRT and plan import, explicit retained text edits, malformed timestamp and UTF-8 rejection, 5,000/5,001-cue boundary, stale-result clearing and an explicitly zero-byte SRT result. Free edition accepted one real file and rejected two. The supplied example's exact authored decisions produce 5 EN and 6 KO output cues.

Direct `file://` opening, mobile layout, all-browser compatibility, customer data and customer-production correctness remain unverified. Core capacity checks do not establish full-capacity browser performance or measured user speed. No payment, sales, customer uptake or time-saving result is claimed here.

## Historical v1.0 distribution verification

Before publication, the staging verifier compares the exact public allowlist, the repackaged ZIP's entries/CRCs, and the HTML/example bytes against the existing source release. Its report stays outside the public package. The public HTML's SHA-256 is `b56c00c04ca31eda1dc44b4dd90661cf275d61fd2e2480f25a8f9b2e2d68a9b9`.

AI-assisted code, interface and documentation. Review captions against the original footage: recorded decisions do not prove that retained words match it.
