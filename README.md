# ios-device-risk-signals

Standalone iOS device and runtime observations for Swift and Objective-C apps.
Product: **IOSDeviceRiskSignals**. Requires **iOS 15.1+** or **Mac Catalyst 15.1+**; not macOS.

## Install

In Xcode, choose File → Add Package Dependencies and enter:

`https://github.com/AfanasievN/ios-device-risk-signals.git`

Select version **0.1.0** and the **IOSDeviceRiskSignals** product.

```swift
.package(url: "https://github.com/AfanasievN/ios-device-risk-signals.git", exact: "0.1.0")
// In your target dependencies:
.product(name: "IOSDeviceRiskSignals", package: "ios-device-risk-signals")
```

## Use

```swift
import IOSDeviceRiskSignals

let locale = LocaleInfoProvider().localeSignals()
let application = ApplicationInfoProvider().applicationSignals()
```

Nine collectors cover application metadata, locale, runtime timing, numeric consistency,
telephony, network, audio latency, device identity and an optional GPU benchmark.
This is a **partial, pre-stable SDK**, not full React Native probe parity.
No collector runs automatically. GPU collection must run off the main thread; it skips on Simulator.
Never block the main thread waiting for a worker collecting device identity, which may hop to main.
Telephony fields are commonly absent on modern iOS. Missing data is not evidence of fraud.

## Privacy and limitations

Raw observations only: no score, trusted/untrusted verdict, blocking, network upload,
permission prompt, or persistent device identifier. The host owns consent, minimization,
retention, transport and decision-making. Local IP addresses, proxy details, locale and
hardware/runtime characteristics can be sensitive or high-entropy: collect only what you need.
Do not use these values to create a prohibited device fingerprint. Simulator checks do not
replace physical-device calibration; GPU, carrier and network behavior require device QA.

[API, privacy and threading details](https://github.com/AfanasievN/react-native-device-risk-signals/tree/81db99a9cb1f82b257ca2328f91b6eea8d0a4c10/sdks/ios/README.md) ·
[Native example](https://github.com/AfanasievN/react-native-device-risk-signals/tree/81db99a9cb1f82b257ca2328f91b6eea8d0a4c10/sdks/ios/example) ·
[Documentation](https://afanasievn.github.io/react-native-device-risk-signals/signals/)

## Development and releases

This repository is a generated distribution mirror. Submit changes and issues to the
[monorepo](https://github.com/AfanasievN/react-native-device-risk-signals).
SOURCE.json records the source commit and SHA-256 checksums. No independent implementation lives here.

Run tests on an available iOS Simulator with
`xcodebuild test -scheme ios-device-risk-signals -destination 'platform=iOS Simulator,name=iPhone 17 Pro'`.
`swift test` targets macOS and is not supported.

MIT licensed. See LICENSE.
