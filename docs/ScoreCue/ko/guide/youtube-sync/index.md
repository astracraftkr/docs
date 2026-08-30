---
layout: manual
manual: true
lang: ko
section: 재생과 싱크
title: YouTube 싱크
description: YouTube 영상과 악보 진행의 시작점을 맞춰 원곡, 반주 영상과 함께 연습합니다.
when: YouTube의 원곡이나 반주를 재생하면서 악보가 같은 위치를 따라가게 만들고 싶을 때
permalink: /ScoreCue/ko/guide/youtube-sync/
prev_url: /ScoreCue/ko/guide/count-in/
prev_title: 카운트인 설정
next_url: /ScoreCue/ko/guide/local-audio/
next_title: 로컬 오디오 싱크
---

## YouTube 주소 연결

<ol class="task-list">
  <li>악보를 열고 빈 곳을 탭해 상단 퀵 메뉴를 표시합니다.</li>
  <li>조절 아이콘의 <strong>악보 속성</strong>을 엽니다.</li>
  <li><strong>YouTube 주소</strong>에 공유 링크 또는 영상 주소를 붙여 넣습니다.</li>
  <li>패널을 닫고 하단 추가 컨트롤에서 <strong>오디오 싱크 → YouTube</strong>를 선택합니다.</li>
</ol>

일반 `youtube.com/watch` 주소와 짧은 `youtu.be` 공유 주소를 사용할 수 있습니다. 주소가 올바르지 않으면 입력란에 오류 안내가 표시됩니다.

## 시작 위치 맞추기

영상은 시작하자마자 음악이 나오지 않는 경우가 많습니다. 설명, 무음, 카운트가 있다면 악보의 첫 박과 영상의 실제 음악 시작점을 맞춰야 합니다.

1. YouTube 플레이어에서 음악의 첫 박 직전으로 이동합니다.
2. 악보 재생을 시작해 첫 마디와 영상이 맞는지 듣습니다.
3. 영상이 늦으면 YouTube 시작 위치를 앞당기고, 빠르면 늦춥니다.
4. 처음 4~8마디를 반복해 오차가 가장 작은 값을 찾습니다.

<p class="tip">처음부터 완벽하게 맞추려 하지 말고 0.1~0.2초 단위로 조정하세요. Bluetooth 출력 지연이 있다면 영상 시작값과 별도로 전역 싱크 지연을 보정합니다.</p>

## 영상은 맞는데 뒤로 갈수록 어긋날 때

시작점 문제가 아니라 악보 진행의 BPM 또는 템포 변화가 영상과 다른 경우입니다.

- 전체가 일정한 비율로 벌어진다면 기본 연주 속도를 조절합니다.
- 특정 지점부터 어긋나면 진행 편집에서 템포 구간을 나눕니다.
- 원곡이 자유 템포라면 YouTube를 들으며 직접 탭 기록을 만드는 편이 정확합니다.

## 재생되지 않을 때

- 기기가 인터넷에 연결되어 있는지 확인합니다.
- 영상이 비공개, 삭제, 연령 제한 또는 지역 제한 상태인지 확인합니다.
- YouTube 광고나 버퍼링이 끝난 뒤 다시 시작합니다.
- 앱을 최신 버전으로 업데이트합니다.

<p class="warning">YouTube 광고와 네트워크 버퍼링은 ScoreCue가 제어할 수 없습니다. 공연에서는 네트워크 영상보다 기기에 저장한 로컬 오디오가 더 안정적입니다.</p>

