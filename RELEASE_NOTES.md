# Zorofin LG 1.4.0

Your Jellyfin library, on your LG TV.

- Live TV opens Programs with Sports & live events and On now, alongside Guide.
- Catch Up has larger artwork, clearer actions, filters and Skip/Undo controls.
- Corrects Catch Up remote focus by binding the app's focus helper.
- Sign out appears last in the account menu.
- Compatible servers can expose optional looks, Calendar and Catch Up features.
  Ordinary Jellyfin browsing and playback still work without these extras.

Production identity: `org.zorofin.tv`, version `1.4.0`. Clean source:
`0cbf921bf81e0df45cf6f6c4e91155c30b1244ef`. IPK: 2,000,618 bytes. SHA-256:
`a1c78155e6bbfdf0991d2eb3bf470961ae49c0155a1ce86845aa4eeedd504133`. The package was built from source for this release;
it is not a relabeled 1.2.0 binary.

The owner confirmed TV testing and human code review of the installed 1.4
baseline on November 12, then explicitly requested the Catch Up focus correction
before publication. The corrected source passes all 134 LG DOM regressions.
The corrected IPK's identity, embedded focus binding, notices and privacy boundary
were checked. This publication task did not install or retest the corrected IPK
on a TV. Baseline device installation/readback was on LG B5/webOS 25. Other
models, Homebrew/rooted installation, cross-store updates, HDR and endurance
remain separate acceptance cases.

The optional features depend on services advertised by the user's own server.
No server, account, media library, channels or subscription is included. No root
is required. Install with Developer Mode and DevMode Manager using INSTALL.md.
Keep the previous release for rollback; uninstalling may remove saved accounts.

Existing screenshot images and SCREENSHOT_PROVENANCE.json remain historical
1.2.0 sample-library captures, not new 1.4 screenshots. Their film credits,
licenses and original attribution are preserved. AI tools assisted development,
testing and release preparation. LG Store approval and webOSbrew catalog
acceptance are independent of this direct download. This task does not establish
a new LG Store submission or approval.
