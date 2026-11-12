# LG 1.4.0 validation — November 12, 2026

Clean source `0cbf921bf81e0df45cf6f6c4e91155c30b1244ef`, based on the installed
1.4 baseline `a3820e72cf3da90c781a240ac1426209f8bf3733`. The owner confirmed
baseline TV testing/human review and explicitly requested the Catch Up focus
correction before publication. The correction binds the existing ZoroUI focus
helper. Two asynchronous/capability-call test expectations were corrected;
all 134 original LG DOM cases then passed with the normal test command.
The earlier baseline run had 130 passes and 4 failures; those are not presented
as a successful baseline suite.

The unmodified final IPK is 2,000,618 bytes, SHA-256
`a1c78155e6bbfdf0991d2eb3bf470961ae49c0155a1ce86845aa4eeedd504133`.
Its embedded `org.zorofin.tv` / `1.4.0` identity, packaged focus binding, preserved
icon/notices and absence of private origins, keys, workstation paths and source
maps were verified. Build receipt reports clean source. No public 1.2.0 bytes
were replaced or relabeled.

The official webosbrew-ipk-verify 0.10.0-1 static compatibility checker exited 0
for the declared `>=10.2.0` range using retained 10.2.0/11.2.0 firmware data.
This static check does not establish physical compatibility across those models.
The owner-tested baseline ran on LG B5/webOS 25; this task did not install or
perform a new physical-TV pass on the corrected final IPK. Homebrew/rooted,
cross-store, other-model, HDR and endurance acceptance remain separate.

Existing artwork and SCREENSHOT_PROVENANCE.json describe historical 1.2.0
sample-library captures. They have not been relabeled as new 1.4 captures.
Public URL and catalog checks are recorded separately after publication.

## Published URL and catalog checks

All 16 versioned release assets were anonymously fetched using normal HTTPS;
`public-url-verification.json` records the exact bytes and SHA-256 values.
The Latest manifest was separately verified as version 1.4.0 with the final
IPK hash/size above after promotion from prerelease.

The current upstream validators at apps-repo
`72513e1beee74070119cb21b8f5f3b24184f79b9` exited 0 for catalog lint,
public IPK identity/hash and declared compatibility. Their reports and exit
records are retained here. Homebrew PR #333's package-lint and final PR checks
also passed on head `b4f279ffa911c83c675d31c27f9889e05ff07ec3`. It remains
open and awaiting maintainer review as of November 12, 2026; passing checks
are not catalog acceptance.
