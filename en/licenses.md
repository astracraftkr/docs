---
title: ScoreCue Open Source Notices
permalink: /en/licenses/
effective: 2026-08-25
updated: 2026-08-25
description: Third-party open source components included in ScoreCue and their licenses
lang: en
alt: /ko/licenses/
---

ScoreCue uses the open source and third-party components listed below. Copyright in each component belongs
to its respective holder, and use is governed by the applicable license. Full license texts are available
in each project's repository.

- **Apache License 2.0**: [apache.org/licenses/LICENSE-2.0](https://www.apache.org/licenses/LICENSE-2.0)
- **MIT License**: [opensource.org/license/mit](https://opensource.org/license/mit)
- **BSD 3-Clause License**: [opensource.org/license/bsd-3-clause](https://opensource.org/license/bsd-3-clause)

## Shared (Android · iOS)

<div class="table-wrap" markdown="1">

| Component | Used for | License |
|---|---|---|
| [Firebase SDK](https://github.com/firebase/firebase-android-sdk) (Android / [iOS](https://github.com/firebase/firebase-ios-sdk)) | Sign-in, data storage, usage statistics, crash reporting | Apache-2.0 |
| [RevenueCat Purchases](https://github.com/RevenueCat/purchases-android) (Android / [iOS](https://github.com/RevenueCat/purchases-ios)) | Purchase/subscription handling and paywalls | MIT |
| Google Analytics for Firebase (GoogleAppMeasurement) | Usage statistics | Google proprietary license |

</div>

## Android

<div class="table-wrap" markdown="1">

| Component | Used for | License |
|---|---|---|
| [Kotlin](https://github.com/JetBrains/kotlin) · [kotlinx.coroutines](https://github.com/Kotlin/kotlinx.coroutines) · [kotlinx.serialization](https://github.com/Kotlin/kotlinx.serialization) | Language and standard libraries | Apache-2.0 |
| [AndroidX](https://github.com/androidx/androidx) (Core, AppCompat, Lifecycle, Activity, Navigation, DataStore, Credentials) | App foundation components | Apache-2.0 |
| [Jetpack Compose](https://github.com/androidx/androidx) · Material 3 | User interface | Apache-2.0 |
| [Room](https://github.com/androidx/androidx) | Local database | Apache-2.0 |
| [Media3 / ExoPlayer](https://github.com/androidx/media) | Audio playback and sync | Apache-2.0 |
| [Dagger · Hilt](https://github.com/google/dagger) | Dependency injection | Apache-2.0 |
| [Coil](https://github.com/coil-kt/coil) | Image loading | Apache-2.0 |
| [android-youtube-player](https://github.com/PierfrancescoSoffritti/android-youtube-player) | YouTube playback | MIT |
| [AndroidPdfViewer](https://github.com/mhiew/AndroidPdfViewer) | Score PDF display | Apache-2.0 |
| [PdfiumAndroid](https://github.com/oothp/PdfiumAndroid) (based on [PDFium](https://pdfium.googlesource.com/pdfium/)) | PDF rendering engine | Apache-2.0 (PDFium: BSD-3-Clause) |
| [PdfBox-Android](https://github.com/TomRoush/PdfBox-Android) | Annotated PDF export | Apache-2.0 |
| [ML Kit Text Recognition](https://developers.google.com/ml-kit) | Score analysis (on-device text recognition) | [Google APIs Terms of Service](https://developers.google.com/ml-kit/terms) |
| [Google Identity Services (googleid)](https://developers.google.com/identity) | Google sign-in | Apache-2.0 |

</div>

## iOS · iPadOS

<div class="table-wrap" markdown="1">

| Component | Used for | License |
|---|---|---|
| [YouTubePlayerKit](https://github.com/SvenTiigi/YouTubePlayerKit) | YouTube playback | MIT |
| [abseil-cpp](https://github.com/abseil/abseil-cpp) | Firebase internal dependency | Apache-2.0 |
| [gRPC](https://github.com/grpc/grpc) | Firebase internal transport | Apache-2.0 |
| [SwiftProtobuf](https://github.com/apple/swift-protobuf) | Data serialization | Apache-2.0 |
| [Google Promises](https://github.com/google/promises) | Asynchronous handling | Apache-2.0 |
| [GoogleUtilities](https://github.com/google/GoogleUtilities) · [GoogleDataTransport](https://github.com/google/GoogleDataTransport) · [GTMSessionFetcher](https://github.com/google/gtm-session-fetcher) · [interop-ios-for-google-sdks](https://github.com/google/interop-ios-for-google-sdks) · [App Check](https://github.com/google/app-check) | Firebase internal dependencies | Apache-2.0 |
| [LevelDB](https://github.com/google/leveldb) | Firestore local storage | BSD-3-Clause |
| [nanopb](https://github.com/nanopb/nanopb) | Firebase internal dependency | zlib |

</div>

## Contact

If you find an error or omission in this list, please let us know:
<a href="mailto:support@astracraft.kr">support@astracraft.kr</a>
