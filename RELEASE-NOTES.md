# GitHub Free Edition v1.1.3

Prepared locally on 2026-10-11. Fixes data loss when a cut-plan import fails validation or cannot be read. The plan's schema, ranges and limits are validated before replacing current cuts or clearing review. Failed imports preserve source tracks, cuts, results, original-timeline acknowledgement, decisions and unfinished drafts. Review and exports pause during validation; newer actions supersede older pending reads.

A successful new plan still clears the old review and requires fresh acknowledgement and analysis. Earlier SRT-import and retained-text fixes remain included. Timing rules, checkpoint format, one-real-track Free capacity and license grants are unchanged. Existing v1.1 checkpoints and the same six synthetic examples remain supported.

## v1.1.3 verification scope

The product passed 76 automated tests. The selected cut-plan run reproduced partial/completed review loss before the fix and passed all 22 tests afterward, covering invalid input, limits, read failures, delayed import races, valid replacement, checkpoint/output equality and actual interface event handlers. Local packaging checks verify deterministic HTML and ZIP bytes. Full-edition tests concern the source product only; the Full application is absent from this GitHub Free distribution.

Finished v1.1.3 applications were checked in desktop Chrome served over localhost HTTP. Full imported the supplied EN 9-cue and KO 8-cue originals with tutorial cuts; five manual keeps and one KO drop produced EN 6 / KO 6 outputs. This is a deliberate review variant, not the guide's four-keep/two-drop 11-output result. A malformed plan preserved acknowledgement, the All captions view and zero unresolved decisions; actual report and checkpoint downloads were byte-identical before/after. Trial retained one confirmed Unicode caption and one unfinished draft, the selected segment, acknowledgement and one unresolved decision after an invalid-range plan, with byte-identical checkpoints. Confirming that draft exported the expected 1-2 second and 2-4 second captions with the custom text. Importing a valid 3-4 second plan cleared review and acknowledgement; re-analysis showed two unresolved captions with original text. Full checks concern the source product only; no paid application is included here.

These small synthetic Chrome HTTP checks do not establish direct file:// launch, mobile/all-browser behavior, full-capacity browser performance, Resolve integration, public or paid-download hashes, customer-production correctness or measured time savings. Public-delivery verification remains separate. Historical browser observations below apply to their stated versions.

The dedicated GitHub Free license changes only its two package/application filename references. Grants and restrictions remain unchanged; this is not an OSI open-source license.

## Historical v1.1.2 notes

# GitHub Free Edition v1.1.2

Fixes data loss after a rejected replacement SRT import. Files are read and validated together in a staging state; the current workspace is replaced only after the complete selection is accepted. Invalid or mixed-validity SRT selections, capacity-limit rejections and read failures now preserve existing source tracks, results, confirmed decisions and unfinished retained-text drafts. A generation guard prevents an older pending read from overwriting newer actions.

Successful replacement imports still invalidate the old review and require fresh original-timeline acknowledgement and boundary decisions. Timing rules, checkpoint format, one-real-track Free capacity and license permissions are unchanged. Existing v1.1 checkpoints remain supported. The six synthetic example files are unchanged.

## v1.1.2 verification scope

The product release passed 56 automated tests and an independent review of import races and release manifests. Finished applications were exercised in desktop Chrome served over localhost HTTP. The Trial accepted a real two-cue SRT, preserved a custom Unicode retained-text draft after a bad SRT import, and then confirmed and exported the retained caption. Separately, the Full synthetic tutorial kept two tracks, six completed decisions and zero unresolved crossings after a failed import; its before/after exported reports were byte-identical and the result contained 11 cues. These Full checks are product verification only: no Full application is included in this GitHub repository or ZIP.

Direct file:// launch was not verified because browser tooling policy disallowed it. Mobile, all-browser compatibility, customer-production results and measured time savings remain unverified. This release's package and public-delivery checks are separate distribution evidence, not customer demand or revenue.

Trial HTML SHA-256: `53c6a52896b552496a4eca39bb1a19a8cc1428d1617744087b4ff26e4a69135c`.

The dedicated GitHub Free license changes only its two package/application filename references. Grants and restrictions remain unchanged; this is not an OSI open-source license.

## Historical v1.1.1 notes

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
