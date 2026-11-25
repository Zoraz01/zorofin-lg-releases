# Zorofin LG 1.5.0

Your Jellyfin library, on your LG TV.

- Blu-ray (PGS) subtitles are drawn on the TV, so the server no longer
  re-encodes the video to burn them in. Styled (ASS/SSA) subtitles keep their
  colours, positions and italics. Playback info says where subtitles are drawn.
- HDR titles open the HDR stream instead of falling back to SDR.
- "Who's watching?" gives everyone their own profile, progress and rows.
- Trailer previews play when you rest on a poster in a row.
- Continue Watching keeps unfinished titles and the next episode together.
- Player: Skip intro, subtitle timing, and chapters (off by default; turn them
  on in Settings).

Production identity: `org.zorofin.tv`, version `1.5.0`. Clean source:
`09abca3429bf77ffb72a88bc173b768c395c3da5`. IPK: `2,090,712` bytes. SHA-256: `4a2ee3c43e0179f878df4d25f3ecd7c33255ba7c91e3391fb34264e1658e6b77`.

Tested in the 1.5 QA pass on an LG B5, including this exact package. Other
models, Homebrew/rooted installation and switching between store and sideloaded
copies are separate acceptance cases.

Works with ordinary Jellyfin servers. Optional features (Home rows, Pick
Together, Catch Up, Calendar, Requests, Live TV scores) appear when the server
has the free Zorofin plugin and Companion. No server, account, media, channels
or subscription is included. No root is required. Install with Developer Mode
and DevMode Manager using INSTALL.md. Install over the existing app to update;
uninstalling may remove saved accounts. LG 1.4.0 stays available for rollback.

Screenshots are the historical 1.2.0 sample-library captures (see
SCREENSHOT_PROVENANCE.json), not new 1.5 captures.

Third-party code: libpgs 0.9.0 (MIT) and webOSTV.js 1.2.13 (Apache-2.0); licences
are in `notices/`. AI tools assisted development, testing and release
preparation. LG Store approval and webOSbrew catalog acceptance are independent
of this direct download.
