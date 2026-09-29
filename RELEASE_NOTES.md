# iOS SDK 0.1.0

Standalone Swift Package for iOS 15.1+ and Mac Catalyst 15.1+, with no React Native dependency.

- Nine raw-observation collectors: application, locale, runtime timing, numeric consistency,
  telephony, network, audio latency, device identity and optional GPU benchmarking.
- Swift-importable Objective-C API, shared statistics helpers and native tests.
- No automatic collection, network transport, permission prompts, persistent IDs or risk scoring.
- Independent versioning and a reproducible, allowlisted export from the monorepo.

Pre-stable, partial API: remaining React Native probes are not included. Physical-device QA
is still required; Simulator cannot validate real carrier data or GPU performance.
See README for privacy and thread requirements, installation and usage.

Source: https://github.com/AfanasievN/react-native-device-risk-signals/tree/81db99a9cb1f82b257ca2328f91b6eea8d0a4c10
