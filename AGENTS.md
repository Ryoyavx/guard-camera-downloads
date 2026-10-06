# Guard Camera Downloads

- This public repository contains Guard Camera release binaries and installation notes only.
- The application source is maintained in the private Ryoyavx/guard-camera repository.
- Current preview release: v0.2.0-preview, with a signed Android APK and a self-contained Windows x64 ZIP.
- Before updating a release, build from the canonical source workspace, verify Android package ID/version/signature and both file SHA-256 hashes, then update README links and hashes.
- Keep signing keys, credentials, user data, debug logs, and private source out of this repository.
- Public Android package io.github.ryoyavx.guardcamera is separate from the development package com.example.guardcamera; do not claim automatic data migration.
- LAN or Tailscale access only; never recommend router port forwarding or direct internet exposure.
