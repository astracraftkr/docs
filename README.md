# Astra Craft Docs

여러 Astra Craft 제품의 **외부 공개용 사용자 가이드·정책 사이트 저장소**입니다.
GitHub Pages(Jekyll)는 저장소 전체가 아니라 `docs/`만 게시합니다. 현재 공개 제품은 ScoreCue이며,
7개 언어의 사용자 가이드와 앱 스토어·RevenueCat 페이월이 참조하는 약관·정책을 제공합니다.

앱 코드 저장소: [astracraftkr/ScoreCue](https://github.com/astracraftkr/ScoreCue) (Android/iOS 서브모듈)

## 구성

```
README.md                    저장소 운영 문서 (Pages 비공개)
Gemfile                      로컬 미리보기 의존성 (Pages 비공개)
notes/                       제작 메모 (Pages 비공개)
docs/                        GitHub Pages 게시 루트
  _config.yml                사이트 전체 Jekyll 설정
  CNAME                      doc.astracraft.kr
  .well-known/               Android App Links · iOS Universal Links 도메인 검증
  index.html                 제품 목록 허브
  ScoreCue/
    index.md                 ScoreCue 다국어 허브 → /ScoreCue/
    invite/index.html        공통 밴드 초대·설치 안내 페이지
    _layouts/                공통·가이드 레이아웃
    _data/guides.yml         사용자 가이드 번역 원문
    {locale}/guide/          ko/en/ja/es/de/fr/pt-br 가이드
    assets/screenshots/android/{locale}/  Android 실기기 스크린샷
    ko/{terms,privacy,refund,eula,licenses}.md  한국어 정본
    en/{terms,privacy,refund,eula,licenses}.md  English 번역
```

각 페이지는 front matter의 `permalink`로 URL을 고정한다. **스토어·RevenueCat에 등록한 뒤에는 permalink를
바꾸지 말 것** — 링크가 깨진다. 파일 이름을 바꿔도 permalink가 그대로면 URL은 유지된다.

front matter 필드: `lang`(가이드 7개 언어, 정책 ko/en — 레이아웃의 언어 전환 기준), `alt`(반대 언어 페이지 경로 — 헤더의 언어
전환 링크와 `hreflang`에 쓰인다), `effective`(시행일), `updated`(최종 수정일, 선택).

**한국어판이 정본이다.** 영문판 각 문서 상단에 그 사실과 "불일치 시 한국어판 우선"을 명시해 두었다.
내용을 고칠 때는 반드시 양쪽을 함께 고칠 것 — 한쪽만 고치면 정본과 번역이 어긋난다.

## 공개 URL

GitHub Pages 설정: Settings → Pages → Source = `main` 브랜치 / `docs` 폴더.

기준 URL: `https://doc.astracraft.kr/ScoreCue/`

| 문서 | 한국어 | English |
|---|---|---|
| 허브 | `/ScoreCue/` | `/ScoreCue/` |
| 이용약관 | `/ScoreCue/ko/terms/` | `/ScoreCue/en/terms/` |
| 개인정보처리방침 | `/ScoreCue/ko/privacy/` | `/ScoreCue/en/privacy/` |
| 결제·환불 | `/ScoreCue/ko/refund/` | `/ScoreCue/en/refund/` |
| EULA | `/ScoreCue/ko/eula/` | `/ScoreCue/en/eula/` |
| 오픈소스 고지 | `/ScoreCue/ko/licenses/` | `/ScoreCue/en/licenses/` |
| 사업자 정보 | `/ScoreCue/ko/business/` | `/ScoreCue/en/business/` |
| 밴드 초대 | `/ScoreCue/invite/#초대코드` | 양 플랫폼 공통 |

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

> `docs/` 아래의 파일은 **GitHub Pages로 공개 서비스**된다. 내부 판단·미결 사항은 게시 루트 밖의
> 이 README나 앱 저장소의 `doc/TODO.md`에 둔다. 단, 저장소 자체가 공개라면 GitHub에서는 여전히
> 읽을 수 있으므로 비밀키·개인정보는 저장소 어디에도 기록하지 않는다.
- **만 14세 미만 계정 금지**로 작성했다(개인정보보호법상 법정대리인 동의 절차를 두지 않는 선택).
  아동 대상 정책을 바꾸려면 약관 제4조·방침 7항을 함께 고쳐야 한다.
- 개인정보처리방침의 보관 기간 중 Analytics 14개월·Crashlytics 90일은 각 서비스의 기본 설정값이다.
  Firebase 콘솔에서 값을 바꿨다면 문서도 함께 수정할 것.
- 상세 사용자 가이드는 Android를 먼저 작성한다. iOS 문서는 앱 기능과 UI가 안정된 뒤 별도 제작한다.

## 로컬 미리보기

```bash
bundle exec jekyll serve --source docs
```

Ruby/Jekyll이 없으면 GitHub Pages에 push해서 확인해도 된다(빌드 1~2분).

## 문서 갱신 규칙

- 앱의 데이터 수집·요금·권한 정책이 바뀌면 **같은 커밋 흐름에서 이 저장소도 갱신**한다.
  특히 [pricing.md](https://github.com/astracraftkr/ScoreCue/blob/main/doc/pricing.md) 변경은
  `ko/terms.md`·`ko/refund.md`에 직접 영향을 준다.
- 이용자에게 불리한 변경은 시행일 전 고지 기간을 둔다(약관 제3조: 7일, 중대한 변경 30일 / 방침: 30일).
- 각 문서 front matter의 `effective`(시행일)와 `updated`(최종 수정일)를 갱신한다.
