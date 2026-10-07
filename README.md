# Subtitle Recut Desk — Free Edition

A self-contained desktop-browser tool for applying a **known original-time deletion plan** to an existing UTF-8 SRT file. Captions that cross a deletion require an explicit editorial choice before export: keep one surviving segment with reviewed text, or drop the caption.

The free edition completes the entire workflow for one real subtitle track. It does not cut video, listen to speech, infer alignment, or split sentences automatically.

## Download and start

[Try the free browser edition](https://pocketlogicprints.itch.io/subtitle-recut-desk): on itch.io, choose **Run tool**, then **Load synthetic example**. Both free versions accept one real SRT track; the supplied two-track tutorial is an exception.

For a local copy, [download the free one-track ZIP](https://github.com/KimJiUng/subtitle-recut-free/releases/download/v1.1.2-github-free/Subtitle-Recut-Desk-GitHub-Free-v1.1.2.zip), extract it, and open `Subtitle-Recut-Desk-Trial-v1.1.2.html` in a modern desktop browser. The HTML embeds its code and styles; it needs no installation or runtime network connection. The `Trial` filename is retained because its bytes are identical to the v1.1.2 free application.

Direct opening from an extracted folder has not been verified by the browser tooling used for this release. Finished-app checks were performed in desktop Chrome served from localhost. Test with copies of your files in your own browser before relying on the result; mobile and all-browser compatibility are unverified.

1. Import **one original UTF-8 SRT**, or choose **Load synthetic example** first.
2. Enter deletion ranges on the original video's timeline. Alternatively, use **Import cut plan** with `examples/example-plan.json` for the supplied synthetic files.
3. Confirm the original-timeline checkbox and select **Analyze cuts & review**.
4. For each crossing caption, select **Drop this whole caption**, or choose **Keep segment N**, review/edit the retained text, and select **Confirm retained text**. Use your normal video player/editor to decide what the surviving footage actually says.
5. Once every crossing caption is resolved, use **Download SRT**, **Download report**, or **Download all as ZIP**. Use **Save cut plan** to save only the original-time deletion ranges for another session.
6. To pause an imported-file review, use **Save review checkpoint**. Later choose **Resume checkpoint**, recheck the originals/cuts and tick the original-timeline acknowledgement again. Confirmed choices and unfinished drafts return without another Analyze. Final exports still require every boundary decision.

Keep the original SRT. Never apply an original-time plan again to an already retimed output.

## What happens at a cut

Consider one caption from `00:00:11,000` to `00:00:15,000` and a single deletion from `00:00:12,000` to `00:00:14,000`.

| Original caption piece | Retimed piece if retained |
| --- | --- |
| 11–12 seconds | 11–12 seconds |
| 14–15 seconds | 12–13 seconds |

The tool will not duplicate the whole sentence into both pieces. Choose **one** piece and confirm the text that belongs there, or drop the caption. This timing calculation does not prove which words match the footage. This standalone illustration contains only that one cut; the supplied tutorial also has an earlier cut and therefore has different final times.

A cue completely inside deleted time is removed. A cue wholly outside a cut is shifted by earlier deleted time. A cue ending exactly when a cut starts, or beginning exactly when it ends, does not cross that cut. Touching and overlapping deletion ranges merge.

## Capacity and formats

| Limit | Free edition |
| --- | --- |
| Real files per session | 1 SRT track |
| Cues per track | 5,000 |
| File size per track | 2 MiB: 2,097,152 bytes |
| Entered deletion ranges | 100 |
| Cut coordinates | Original-time, half-open `[start, end)` intervals |
| Exports | Revised SRT, complete JSON change report, result ZIP, cuts-only JSON plan, review checkpoint |
| Checkpoint JSON | 32 MiB; one real track with normal source limits |

SRT input must be UTF-8 with positive, unique cue numbers, nondecreasing start times, positive durations, nonempty text, and blank lines between cues. Timestamps use `HH:MM:SS,mmm --> HH:MM:SS,mmm`, hours 00–99 and minutes/seconds 00–59. Unsupported SRT dialects and ambiguous malformed blocks are rejected. Unicode, multiline text and literal markup are preserved. Existing overlaps are reported, not repaired.

Outputs are ordered by new start time and renumbered; report entries retain original cue references and order. A completely deleted track exports an explicitly empty SRT. No fabricated placeholder caption is added.

## Worked synthetic example

**Load synthetic example** loads two authored tracks even in this free edition. That is a tutorial exception, not permission to import two real files. Successfully importing a real file replaces the whole tutorial state. A rejected or unreadable import leaves the current tutorial or review intact.

The original tracks contain 17 cues. With the exact six review choices in [the worked example guide](examples/worked-example-guide.txt), four crossing captions are kept and two dropped, producing **5 EN cues + 6 KO cues**. The guide lists every retained segment and exact text. `expected-en.srt` and `expected-ko.srt` are reference outputs, not input files for another application of the plan.

The unchanged built-in tutorial also offers **Apply the worked example decisions**. This applies authored synthetic choices only; it does not make editorial decisions for real files. Changing the example invalidates its original expected totals. To test normal file import, process `synthetic-en.srt` and `synthetic-ko.srt` in separate sessions.

## Privacy and review boundaries

The application processes imported files in browser memory. It performs no runtime network requests, automatic uploads, analytics, account login, or persistent browser storage. Visiting GitHub or a download page is separate from running the downloaded application. Closing or reloading loses unsaved work; download a checkpoint or your finished outputs first.

Reports contain source filenames, caption text, cuts and review decisions. Saved cut plans contain only the product schema and original-time ranges: no filenames, caption text or decisions. Successful file/plan imports or cut edits clear old results and require fresh acknowledgement and review. Replacement SRT files are validated together before they replace the workspace. Invalid, mixed-validity, over-limit or unreadable selections preserve current source tracks, results, decisions and unfinished drafts. Newer actions invalidate an older pending import.

Review checkpoints contain complete original subtitles, source names, cuts, confirmed decisions and unfinished drafts. Validation reparses source metadata and recomputes analysis before restoring matching choices; failed imports preserve your current work. A changed input/cut invalidates review as before. Checkpoints are editable local files, not authenticated evidence. Source filenames may contain up to 4,096 UTF-8 bytes and saved reviewed/draft text up to 2 MiB per caption. Escape-heavy saved content can exceed the 32 MiB checkpoint limit even if ordinary input fits.

The built-in two-track synthetic demo cannot be checkpointed. Import one supplied original SRT as a normal file to try the pause/resume exercise. Importing a Full checkpoint never grants the Free edition multiple real tracks or demo privileges.

All input timings must refer to the same original video. The app cannot check that relationship or determine which words belong in retained footage. It has no video playback/cutting, translation, speech recognition, acoustic synchronization, automatic sentence splitting, inserted-scene support, speed changes, or frame-rate conversion. No measured time saving or customer-production validation is claimed.

## License and optional larger sessions

This repository and its **GitHub Free** ZIP use [the included free-edition license](LICENSE.txt). Personal, internal business and client-output use are allowed. Noncommercial, unmodified redistribution/hosting with the complete notices is allowed, as is ordinary GitHub viewing and forking. This is a custom license with restrictions, **not an OSI open-source license**. The original marketplace package and paid Full edition have separate licenses; the Full edition is not included here.

If you need a shared session for up to ten real tracks, the [Full edition has a USD 5 one-time base price](https://pocketlogicprints.itch.io/subtitle-recut-desk). The cue, file-size and cut limits are the same. The free edition already includes all review decisions, result/report exports, plan reuse and checkpoint save/resume. A larger session is useful only if this focused workflow fits your work.

AI-assisted code, interface and documentation. See [release notes](RELEASE-NOTES.md) for the scope of prior verification and this repackaging.
