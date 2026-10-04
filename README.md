# Ruri credential helper releases

This repository hosts binary releases of the credential service and helpers used
by Ruri. The Ruri application and helper source code are maintained separately;
this repository currently contains release documentation only.

## Bundle contents

- `ruri-authfs-store`: macOS credential service.
- `ruri-authfs-ctl`: macOS control tool.
- `ruri-authfs-guest-aarch64`: Linux ARM64 container credential helper.
- `ruri-authfs-guest-x86_64`: Linux x86-64 container credential helper.
- `manifest.json` and `SHA256SUMS`: version metadata and integrity checks.

Bundles contain no user credentials, databases, or signing keys. Host architecture
and signing details are documented per release.

## Releases

Publish each validated bundle as a GitHub Release asset, using a versioned tag
such as `authfs-ca152b1f-p4` and an archive such as `ca152b1f-p4.tar.gz`.
Keep published versioned assets unchanged; publish a new version for new bytes.

Ruri source builds select a release through `src-tauri/authfs-bundle.lock.json`,
which records the release repository, tag, asset name, and checksums. Packaged
Ruri apps already include their helper bundle and require no access to this
repository at runtime.

No binary releases have been published from this placeholder yet.
