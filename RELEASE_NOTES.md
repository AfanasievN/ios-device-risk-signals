# iOS SDK 0.2.0-beta.1

**Experimental prerelease. Physical-iPhone QA has NOT been completed; use for evaluation only.**

Standalone Swift Package for iOS 15.1+ and Mac Catalyst 15.1+, with no React Native dependency.

- Sixteen collectors cover device identity, hardware, fonts, socket-free OS integrity, application, locale, network, telephony, cached geolocation, media/app observations, security posture, transaction snapshots, native timing, numeric consistency, audio latency and GPU benchmarking.
- Swift-importable Objective-C API, shared statistics helpers and native tests.
- No automatic collection, network transport, permission prompts, persistent IDs or risk scoring.
- Independent versioning and a reproducible, allowlisted export from the monorepo.

Pre-stable, partial API: remaining React Native probes are not included. Physical-device QA
is still required; Simulator cannot validate real carrier data or GPU performance.
See README for privacy and thread requirements, installation and usage.

Source: https://github.com/AfanasievN/react-native-device-risk-signals/tree/5be135fbf141773a82969386e6a1f9df7c748742
