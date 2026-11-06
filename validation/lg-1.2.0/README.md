# LG 1.2.0 release validation — November 6, 2026

Application source d81819a087f144cba00344501b6fa6d9111a865a, dirty=false. Exact org.zorofin.tv 1.2.0 IPK: 1,987,646 bytes, SHA256 9c44b6a9c62e6ef47c7ac058dcf1b391123b02ff17ebb13ffa76d595efbbf3ee. No rebuild or binary modification for Homebrew.

## Public/local checks

- All 16 release assets downloaded anonymously with exact SHA256/byte matches.
- Five catalog icon/screenshot URLs return image/png and match the original PNG hashes. Images use commit-pinned raw GitHub URLs; binary downloads use GitHub Releases.
- Stable latest manifest resolves to the exact published manifest.
- Upstream catalog lint (new-package mode): exit 0.
- Upstream public IPK download/hash/embedded identity check: exit 0.
- Upstream declared compatibility check: exit 0 for webosRelease >=10.2.0. The checker examines webOS 10.2.0/11.2.0 firmware data and finds ES2020/runtime API compatibility. This is static compatibility, not physical acceptance on both releases.

Upstream snapshot: webosbrew/apps-repo f3c64646459e9526832fcfc6e61d5c8d009decb4. Official dev-toolbox-cli v20261017-2d5a7b6, package 0.10.0-1 arm64, release asset digests verified. Checks ran locally in an isolated Python 3.11 Linux container, not GitHub Actions. Container image digest a83ba18aef0f865b1a4a611c2cf460fe446f2795673bbb9fe43be570439e3b39. Python dependencies follow the upstream requirements; jsonschema 4.21.1. No TLS checks were disabled. Host curl used system TLS trust because the host Python CA store was unavailable.

To reproduce, check out the pinned upstream snapshot, install its documented dependencies and official toolbox, then run from that checkout:

```sh
python3 -m repogen.lintpkg -f /path/to/catalog/org.zorofin.tv.yml --new
python3 -m repogen.downloadipk -i /path/to/catalog/org.zorofin.tv.yml -o /path/to/download.ipk
python3 -m repogen.check_compat -i /path/to/catalog/org.zorofin.tv.yml -p /path/to/download.ipk
```

## Separate human/device evidence

The original candidate records 127 LG DOM and 201 shared Dart tests plus analyzer/VM/compiled-JS/package checks. Device diagnostics and owner-reported physical tests use LG B5/webOS 25, reported SDK 10.3.2 and firmware 33.31.75. The owner confirmed human review of the generated LG source beyond TV testing on November 6. The AI-use declaration relies on that confirmation; release automation does not substitute for human code review.

No new TV acceptance was performed in this publication run. A read-only attempt to obtain the current starfish-release identifier could not reach the paired TV; no app launch, install, root change or playback interruption occurred. The catalog minimum is a conservative distribution restriction checked against upstream firmware data, not a newly observed physical OS identifier. Homebrew/rooted installation, cross-store updates, other-model/older-device, HDR and endurance acceptance remain separate. Native Flutter webOS is deferred.

The download release, LG Store QA and webOSbrew catalog acceptance are independent. These passing checks do not establish either store/community approval.
