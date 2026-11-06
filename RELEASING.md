# Releasing the LG binary

This repository contains public release records and catalog metadata. Application development/building happens separately. Import only an independently tested production package and its clean source receipt; never import private Git history or an entire development folder.

1. Prepare a new ignored `_release/assets/` directory containing the exact IPK, manifest, icon, marketing images, credits, notices, installation instructions, source receipt and checksum file. The 1.2.0 source/hash are in SOURCE.json. Preserve the stable app ID.
2. Render versioned GitHub Release URLs in the manifest and screenshots. Keep `catalog/org.zorofin.tv.yml` pointed at the latest release manifest. Do not change a published IPK while retaining its version/hash.
3. Verify SHA256/bytes, the package's embedded identity, every license/credit and all marketing provenance. Run the current upstream webOSbrew schema, network, IPK identity and compatibility checks locally. Separate automated evidence from physical-device acceptance.
4. Verify Actions remain disabled before pushing release documentation:

```sh
gh api repos/Zoraz01/zorofin-lg-releases/actions/permissions --jq .enabled
```

5. Commit only public documents, notices and catalog metadata. `_release/` and `_audit/` remain ignored. No workflow is needed. Create a release from the reviewed commit, uploading only the exact public asset allowlist. Use `--notes-file RELEASE_NOTES.md`. Tags here identify the release documentation; SOURCE.json identifies the application's original source.
6. Anonymously download every published asset and verify exact bytes/hash/content type. Run upstream webOSbrew checks against these real URLs. Do not call a draft release or successful upload a community listing.
7. Open/update the catalog PR in `webosbrew/apps-repo` with the single package file. Complete the template truthfully, including actual human source review, TV testing and AI use. Maintainers decide listing acceptance. Do not claim approval before their merge.

For updates use a scoped tool-neutral branch. Keep previous release artifacts available for rollback. Never uninstall account-bearing TV apps or root/change a TV as an incidental release step. LG Store QA, direct downloads and Homebrew catalog acceptance are separate.
