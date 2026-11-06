# Zorofin LG 1.2.0

Your Jellyfin library, on your LG TV. Browse movies and shows, continue watching, switch accounts and use supported Live TV.

- Saved sign-in defaults on when protected storage is available.
- Optional compatible-server Home rows with ordinary Jellyfin fallback.
- Next-episode autoplay and watched-completion retry/recovery.
- Episode selector opens at the current/next episode.
- Device-dependent playback with Jellyfin conversion for unsupported formats.

This is the exact production `org.zorofin.tv` 1.2.0 IPK submitted to LG. It was not rebuilt for Homebrew. Full source revision: `d81819a087f144cba00344501b6fa6d9111a865a`; clean build. SHA256: `9c44b6a9c62e6ef47c7ac058dcf1b391123b02ff17ebb13ffa76d595efbbf3ee`; 1,987,646 bytes.

Validation includes 127 LG DOM tests, 201 shared Dart tests and packaged bridge checks. Recorded LG B5/webOS 25 diagnostics include completion/watched state, autoplay, encrypted sign-in restore, episode navigation, codec/HLS and short 4K SDR playback. The owner reports physical TV testing and human review of the generated LG source. These do not establish older-device, Homebrew/rooted, cross-store upgrade, HDR or high-bitrate endurance acceptance. Native Flutter webOS is deferred; this is the fast HTML/CSS/JS Web client with a shared Dart bridge.

Zorofin requires no media subscription or root. You provide your own server and lawful media. Optional plugin/Companion availability and setup are separate. Library 4K/HDR labels are not blanket playback guarantees. Screenshot films are not included; see CREDITS.md and SCREENSHOT_PROVENANCE.json. Third-party software licenses are in notices/ in the sideload ZIP.

AI tools assisted development, testing and release preparation. The Homebrew declaration records the owner's confirmation of human source review and TV testing. Community listing/approval and LG Store QA are independent of this binary download.
