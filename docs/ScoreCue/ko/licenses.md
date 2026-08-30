---
title: ScoreCue 오픈소스 라이선스 고지
permalink: /ScoreCue/ko/licenses/
redirect_from: /ko/licenses/
effective: 2026-08-25
updated: 2026-08-25
description: ScoreCue에 포함된 제3자 오픈소스 구성요소와 라이선스 목록
lang: ko
alt: /ScoreCue/en/licenses/
---

ScoreCue는 아래 오픈소스 및 제3자 구성요소를 사용합니다. 각 구성요소의 저작권은 해당 권리자에게 있으며,
사용 조건은 각 라이선스를 따릅니다. 라이선스 전문은 각 프로젝트 저장소에서 확인할 수 있습니다.

- **Apache License 2.0** 전문: [apache.org/licenses/LICENSE-2.0](https://www.apache.org/licenses/LICENSE-2.0)
- **MIT License** 전문: [opensource.org/license/mit](https://opensource.org/license/mit)
- **BSD 3-Clause License** 전문: [opensource.org/license/bsd-3-clause](https://opensource.org/license/bsd-3-clause)

## 공통 (Android · iOS)

<div class="table-wrap" markdown="1">

| 구성요소 | 용도 | 라이선스 |
|---|---|---|
| [Firebase SDK](https://github.com/firebase/firebase-android-sdk) (Android / [iOS](https://github.com/firebase/firebase-ios-sdk)) | 로그인, 데이터 저장, 사용 통계, 오류 보고 | Apache-2.0 |
| [RevenueCat Purchases](https://github.com/RevenueCat/purchases-android) (Android / [iOS](https://github.com/RevenueCat/purchases-ios)) | 구매·구독 처리 및 페이월 | MIT |
| Google Analytics for Firebase (GoogleAppMeasurement) | 사용 통계 | Google 독점 라이선스 |

</div>

## Android

<div class="table-wrap" markdown="1">

| 구성요소 | 용도 | 라이선스 |
|---|---|---|
| [Kotlin](https://github.com/JetBrains/kotlin) · [kotlinx.coroutines](https://github.com/Kotlin/kotlinx.coroutines) · [kotlinx.serialization](https://github.com/Kotlin/kotlinx.serialization) | 언어 및 표준 라이브러리 | Apache-2.0 |
| [AndroidX](https://github.com/androidx/androidx) (Core, AppCompat, Lifecycle, Activity, Navigation, DataStore, Credentials) | 앱 기반 구성요소 | Apache-2.0 |
| [Jetpack Compose](https://github.com/androidx/androidx) · Material 3 | 화면 구성 | Apache-2.0 |
| [Room](https://github.com/androidx/androidx) | 로컬 데이터베이스 | Apache-2.0 |
| [Media3 / ExoPlayer](https://github.com/androidx/media) | 오디오 재생 및 싱크 | Apache-2.0 |
| [Dagger · Hilt](https://github.com/google/dagger) | 의존성 주입 | Apache-2.0 |
| [Coil](https://github.com/coil-kt/coil) | 이미지 로딩 | Apache-2.0 |
| [android-youtube-player](https://github.com/PierfrancescoSoffritti/android-youtube-player) | YouTube 영상 재생 | MIT |
| [AndroidPdfViewer](https://github.com/mhiew/AndroidPdfViewer) | 악보 PDF 표시 | Apache-2.0 |
| [PdfiumAndroid](https://github.com/oothp/PdfiumAndroid) (기반: [PDFium](https://pdfium.googlesource.com/pdfium/)) | PDF 렌더링 엔진 | Apache-2.0 (PDFium: BSD-3-Clause) |
| [PdfBox-Android](https://github.com/TomRoush/PdfBox-Android) | 필기 PDF 내보내기 | Apache-2.0 |
| [ML Kit 텍스트 인식](https://developers.google.com/ml-kit) | 악보 분석(기기 내 문자 인식) | [Google API 서비스 약관](https://developers.google.com/ml-kit/terms) |
| [Google Identity Services (googleid)](https://developers.google.com/identity) | Google 로그인 | Apache-2.0 |

</div>

## iOS · iPadOS

<div class="table-wrap" markdown="1">

| 구성요소 | 용도 | 라이선스 |
|---|---|---|
| [YouTubePlayerKit](https://github.com/SvenTiigi/YouTubePlayerKit) | YouTube 영상 재생 | MIT |
| [abseil-cpp](https://github.com/abseil/abseil-cpp) | Firebase 내부 의존성 | Apache-2.0 |
| [gRPC](https://github.com/grpc/grpc) | Firebase 내부 통신 | Apache-2.0 |
| [SwiftProtobuf](https://github.com/apple/swift-protobuf) | 데이터 직렬화 | Apache-2.0 |
| [Google Promises](https://github.com/google/promises) | 비동기 처리 | Apache-2.0 |
| [GoogleUtilities](https://github.com/google/GoogleUtilities) · [GoogleDataTransport](https://github.com/google/GoogleDataTransport) · [GTMSessionFetcher](https://github.com/google/gtm-session-fetcher) · [interop-ios-for-google-sdks](https://github.com/google/interop-ios-for-google-sdks) · [App Check](https://github.com/google/app-check) | Firebase 내부 의존성 | Apache-2.0 |
| [LevelDB](https://github.com/google/leveldb) | Firestore 로컬 저장 | BSD-3-Clause |
| [nanopb](https://github.com/nanopb/nanopb) | Firebase 내부 의존성 | zlib |

</div>

## 문의

목록에 오류나 누락이 있으면 알려 주십시오:
<a href="mailto:support@astracraft.kr">support@astracraft.kr</a>
