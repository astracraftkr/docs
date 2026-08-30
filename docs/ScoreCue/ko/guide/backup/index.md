---
layout: manual
manual: true
lang: ko
section: 계정과 데이터
title: 백업과 기기 변경
description: 설정과 악보 진행을 안전하게 보관하고 새 Android 기기에서 PDF 원본과 함께 다시 연결합니다.
when: 태블릿을 바꾸거나 앱을 다시 설치하기 전에 어떤 파일을 따로 보관해야 하는지 확인할 때
permalink: /ScoreCue/ko/guide/backup/
prev_url: /ScoreCue/ko/guide/account-subscription/
prev_title: 계정과 구독
next_url: /ScoreCue/ko/guide/troubleshooting/
next_title: 증상별 해결 방법
---

## 백업되는 것과 원본 파일의 차이

ScoreCue의 설정·데이터 백업과 PDF 원본 보관은 서로 다릅니다. <strong>백업 내보내기</strong>는 셋리스트·악보 진행·악보 정보를 JSON 파일로 저장하지만, PDF와 로컬 오디오 원본은 포함하지 않습니다.

| 항목 | 준비 방법 |
|---|---|
| PDF 악보 원본 | 파일 앱, PC, 개인 클라우드에 별도 복사 |
| 로컬 오디오 | 원본 폴더를 별도 복사 |
| 셋리스트·악보 진행·악보 정보 | ScoreCue의 백업 내보내기로 JSON 저장 |
| Pro 구매 | 같은 계정으로 로그인 후 구매 복원 |
| YouTube 주소 | 데이터 복원 뒤 각 악보 속성에서 확인 |

## 기존 기기에서 준비

<ol class="task-list">
  <li>설정의 <strong>데이터 · 계정 → 백업 / 복원 → 백업 내보내기</strong>를 실행합니다.</li>
  <li>ScoreCue에 등록한 PDF 폴더 전체를 PC나 개인 저장소로 복사합니다.</li>
  <li>로컬 오디오가 있다면 오디오 폴더도 복사합니다.</li>
  <li>중요한 공연 악보를 몇 개 열어 백업 직전 상태를 확인합니다.</li>
</ol>

## 새 기기에서 복원

1. ScoreCue를 설치하고 같은 Google 계정으로 로그인합니다.
2. 구매 복원을 실행해 Pro 상태를 확인합니다.
3. <strong>백업 가져오기</strong>에서 저장해 둔 JSON 파일을 선택합니다.
4. PDF와 오디오 원본을 새 기기의 전용 폴더에 복사합니다.
5. ScoreCue에서 해당 폴더를 등록하고 필요한 파일을 다시 연결합니다.

<p class="note">Android의 폴더 접근 권한은 기기마다 새로 허용해야 합니다. 데이터 복원이 성공해도 새 기기에서 폴더를 등록하기 전에는 PDF가 열리지 않을 수 있습니다.</p>

## 공연 직전 기기 변경

가능하면 기존 기기를 지우지 말고 새 기기에서 전체 셋리스트를 한 번 재생한 뒤 교체하세요. 자동 진행, 오디오 파일, YouTube 주소, 페달 키와 Bluetooth 지연값은 실제 공연 장비로 다시 확인해야 합니다.
