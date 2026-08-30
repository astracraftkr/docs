# docs

ScoreCue(밴드 연주자용 악보 뷰어, Android + iOS)의 **외부 공개용 사용자 가이드·문서 저장소**입니다.
GitHub Pages(Jekyll)로 서비스하며, 7개 언어의 사용자 가이드와 앱 스토어·RevenueCat 페이월이 참조하는 약관·정책을 제공합니다.

앱 코드 저장소: [astracraftkr/ScoreCue](https://github.com/astracraftkr/ScoreCue) (Android/iOS 서브모듈)

## 구성

```
index.md              다국어 사용자 가이드·정책 허브
_layouts/guide.html   7개 언어 공통 사용자 가이드 레이아웃
_data/guides.yml      사용자 가이드 번역 원문
{locale}/guide/       ko/en/ja/es/de/fr/pt-br 가이드 URL
assets/screenshots/android/{locale}/  Android 실기기 스크린샷
assets/screenshots/ios/{locale}/      iPadOS 스크린샷(플랫폼별 분리)
ko/{terms,privacy,refund,eula,licenses}.md   한국어 (정본)  → /ko/…/
en/{terms,privacy,refund,eula,licenses}.md   English 번역   → /en/…/
_layouts/default.html 공통 레이아웃 (page.lang으로 헤더·푸터 언어 전환)
assets/style.css      스타일 (라이트/다크 대응)
_config.yml           Jekyll 설정 (url: https://doc.astracraft.kr, baseurl: 빈 값)
```

각 페이지는 front matter의 `permalink`로 URL을 고정한다. **스토어·RevenueCat에 등록한 뒤에는 permalink를
바꾸지 말 것** — 링크가 깨진다. 파일 이름을 바꿔도 permalink가 그대로면 URL은 유지된다.

front matter 필드: `lang`(가이드 7개 언어, 정책 ko/en — 레이아웃의 언어 전환 기준), `alt`(반대 언어 페이지 경로 — 헤더의 언어
전환 링크와 `hreflang`에 쓰인다), `effective`(시행일), `updated`(최종 수정일, 선택).

**한국어판이 정본이다.** 영문판 각 문서 상단에 그 사실과 "불일치 시 한국어판 우선"을 명시해 두었다.
내용을 고칠 때는 반드시 양쪽을 함께 고칠 것 — 한쪽만 고치면 정본과 번역이 어긋난다.

## 공개 URL

GitHub Pages 설정: Settings → Pages → Source = `main` 브랜치 / 루트.

기준 URL: `https://doc.astracraft.kr/`

| 문서 | 한국어 | English |
|---|---|---|
| 허브 | `/` | `/` |
| 이용약관 | `/ko/terms/` | `/en/terms/` |
| 개인정보처리방침 | `/ko/privacy/` | `/en/privacy/` |
| 결제·환불 | `/ko/refund/` | `/en/refund/` |
| EULA | `/ko/eula/` | `/en/eula/` |
| 오픈소스 고지 | `/ko/licenses/` | `/en/licenses/` |
| 사업자 정보 | `/ko/business/` | `/en/business/` |

이 URL을 넣어야 하는 곳:

- **RevenueCat 페이월** — 약관·개인정보처리방침 링크 (페이월 편집기의 footer 링크 필드)
- **App Store Connect** — 앱 정보의 개인정보처리방침 URL, 라이선스 계약(사용자 지정 EULA 사용 시)
- **Google Play Console** — 스토어 등록정보의 개인정보처리방침 URL
- **앱 설정 화면** — 약관·개인정보처리방침 링크 (아직 미배선)

## 확인이 필요한 사항 (초안 상태)

문서 내용은 2026-07-30 시점의 실제 앱 동작(Android `main`)과 [ScoreCue/doc/pricing.md](https://github.com/astracraftkr/ScoreCue/blob/main/doc/pricing.md)의
확정 정책을 근거로 작성했다. 다음은 **법률 검토나 사업자 정보 확정이 필요**한 부분이다.

- 약관·EULA·환불 정책은 법률 전문가의 검토를 받지 않은 초안이다. 유료 판매 개시 전에 검토를 권한다.
- **사업자 정보는 기재 완료**다(2026-08-14). 계약 당사자는 **Astra Craft**이며, 표기는 세 곳에 있다 —
  `ko/business.md`·`en/business.md`(전용 페이지), 약관 제1조, 전 페이지 푸터. **한 곳만 고치면 어긋난다.**
- **전화번호는 아직 비워 두었다**(2026-08-15). 「전자상거래법」 표시 항목이자 **Play Console 한국 필수
  정보의 입력 칸**이므로 출시 전에 채워야 한다. 넣을 때 고칠 곳: 위 세 곳 + Play Console.
- **스토어 퍼블리셔명을 `Astra Craft`로 맞출 것.** 문서상 계약 당사자와 스토어 표기가 다르면 심사·분쟁에서
  문제가 된다. D-U-N-S·사업자등록증의 상호와도 글자 단위로 같아야 한다.

> 이 저장소는 **GitHub Pages로 공개 서비스**된다. 내부 판단·미결 사항은 여기 적지 말고
> `ScoreCue/doc/TODO.md`에 둘 것 — `_config.yml`의 `exclude`가 README를 사이트 빌드에서 빼 주지만,
> 저장소가 공개면 github.com에서는 그대로 보인다.
- **만 14세 미만 계정 금지**로 작성했다(개인정보보호법상 법정대리인 동의 절차를 두지 않는 선택).
  아동 대상 정책을 바꾸려면 약관 제4조·방침 7항을 함께 고쳐야 한다.
- 개인정보처리방침의 보관 기간 중 Analytics 14개월·Crashlytics 90일은 각 서비스의 기본 설정값이다.
  Firebase 콘솔에서 값을 바꿨다면 문서도 함께 수정할 것.
- iOS 미출시 상태에서도 문서는 양 플랫폼을 함께 다룬다. 출시 계획이 달라지면 문구를 조정할 것.

## 로컬 미리보기

```bash
bundle exec jekyll serve
```

Ruby/Jekyll이 없으면 GitHub Pages에 push해서 확인해도 된다(빌드 1~2분).

## 문서 갱신 규칙

- 앱의 데이터 수집·요금·권한 정책이 바뀌면 **같은 커밋 흐름에서 이 저장소도 갱신**한다.
  특히 [pricing.md](https://github.com/astracraftkr/ScoreCue/blob/main/doc/pricing.md) 변경은
  `ko/terms.md`·`ko/refund.md`에 직접 영향을 준다.
- 이용자에게 불리한 변경은 시행일 전 고지 기간을 둔다(약관 제3조: 7일, 중대한 변경 30일 / 방침: 30일).
- 각 문서 front matter의 `effective`(시행일)와 `updated`(최종 수정일)를 갱신한다.
