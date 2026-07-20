# Security Policy

Thanks for helping keep ShabuBox and its users safe.

## Reporting a vulnerability

Email **security@shabubox.com** with the details. Please include:

- what the issue is and where (a URL, a file, a build version),
- steps to reproduce, or a proof of concept,
- what an attacker could do with it.

We aim to acknowledge within **3 business days** and to keep you posted as we
work on a fix. Please give us a reasonable window to remediate before any public
disclosure, and don't run tests that could harm other users or their data.

You can report anonymously; if you'd like credit for a valid report, tell us how
you'd like to be named.

## Scope

In scope:

- **ShabuBox for macOS** — the notarized app distributed from shabubox.com and
  updated via Sparkle, including its license verification and the bundled
  scanner libraries.
- **shabubox.com** and its APIs — the marketing site, the licensing webhook, the
  license-recovery endpoint, and the revocation list.

Out of scope: reports that require a jailbroken/compromised machine or physical
access; social-engineering of the developer or Paddle; volumetric DoS; and issues
in third-party services we rely on (Cloudflare, Paddle, Apple) — please report
those to the respective vendor.

## What ShabuBox is (and isn't)

ShabuBox runs entirely on your Mac. There is **no account, no server-side copy of
your documents, and no telemetry** — your files never leave the machine. Payments
are handled by **Paddle** as merchant of record; ShabuBox never sees or stores
card details. The only network calls the app makes are: optional model downloads
you approve, optional iCloud Drive sync using your own Apple account, checking for
its own updates, and a weekly fetch of the public license-revocation list.

## Signing & notarization

Every release is **Developer ID signed and notarized by Apple**, and every update
is **EdDSA-signed** and verified by Sparkle before it installs. If macOS or Sparkle
reports a signature or notarization problem with a build that claims to be from us,
treat it as suspect and email us.
