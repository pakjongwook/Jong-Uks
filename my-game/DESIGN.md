---
name: 숲속 픽셀 RPG 마을 (index.html)
description: 만든 사람이 위에서 내려다본 도트 숲 RPG의 캐릭터로 자기소개하는 index.html의 시각 세계
colors:
  grass: "#5ea94c"
  grass-alt: "#58a247"
  grass-dark: "#4c9440"
  grass-light: "#74bd5c"
  path-edge: "#c49a5e"
  path: "#d9b37a"
  win: "#1c2a6b"
  win-deep: "#10183f"
  slot: "#2b3b85"
  ink: "#ffffff"
  ink-soft: "#c9d3ff"
  ink-selected-soft: "#3a4a8a"
  gold: "#ffe066"
  hp: "#7ee06a"
  red: "#ff7a5c"
typography:
  display:
    fontFamily: "Galmuri11, Malgun Gothic, sans-serif"
    fontSize: "33px"
    fontWeight: 700
    lineHeight: "40px"
    letterSpacing: "normal"
  headline:
    fontFamily: "Galmuri11, Malgun Gothic, sans-serif"
    fontSize: "22px"
    fontWeight: 700
    lineHeight: "32px"
    letterSpacing: "normal"
  title:
    fontFamily: "Galmuri14, Malgun Gothic, sans-serif"
    fontSize: "14px"
    fontWeight: 400
    lineHeight: "32px"
    letterSpacing: "normal"
  body:
    fontFamily: "Galmuri14, Malgun Gothic, sans-serif"
    fontSize: "14px"
    fontWeight: 400
    lineHeight: "24px"
    letterSpacing: "normal"
  body-dialog:
    fontFamily: "Galmuri14, Malgun Gothic, sans-serif"
    fontSize: "14px"
    fontWeight: 400
    lineHeight: "32px"
    letterSpacing: "normal"
  label:
    fontFamily: "Galmuri11, Malgun Gothic, sans-serif"
    fontSize: "11px"
    fontWeight: 700
    lineHeight: "16px"
    letterSpacing: "normal"
  label-chip:
    fontFamily: "Galmuri11, Malgun Gothic, sans-serif"
    fontSize: "11px"
    fontWeight: 700
    lineHeight: "24px"
    letterSpacing: "normal"
rounded:
  none: "0px"
spacing:
  px: "4px"
  t1: "8px"
  t2: "16px"
  t3: "24px"
  t4: "32px"
  t5: "40px"
components:
  window:
    backgroundColor: "{colors.win}"
    textColor: "{colors.ink}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: "16px"
  window-tab:
    backgroundColor: "{colors.win-deep}"
    textColor: "{colors.gold}"
    typography: "{typography.title}"
    rounded: "{rounded.none}"
    padding: "0 8px"
  menu-item:
    textColor: "{colors.ink}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: "8px"
  menu-item-selected:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.win-deep}"
    rounded: "{rounded.none}"
    padding: "8px"
  command:
    textColor: "{colors.ink}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: "8px"
    height: "48px"
  command-active:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.win-deep}"
    rounded: "{rounded.none}"
    padding: "8px"
    height: "48px"
  chip-level:
    backgroundColor: "{colors.gold}"
    textColor: "{colors.win-deep}"
    typography: "{typography.label-chip}"
    rounded: "{rounded.none}"
    padding: "0 8px"
  chip-play:
    backgroundColor: "{colors.hp}"
    textColor: "{colors.win-deep}"
    typography: "{typography.label-chip}"
    rounded: "{rounded.none}"
    padding: "0 8px"
  chip-soon:
    backgroundColor: "{colors.ink-soft}"
    textColor: "{colors.win-deep}"
    typography: "{typography.label-chip}"
    rounded: "{rounded.none}"
    padding: "0 8px"
  inventory-slot:
    backgroundColor: "{colors.slot}"
    rounded: "{rounded.none}"
    size: "56px"
  portrait:
    rounded: "{rounded.none}"
    size: "112px"
---

# Design System: 숲속 픽셀 RPG 마을 (index.html)

> **범위.** 이 문서는 `index.html` 한 페이지의 시각 세계, "숲속 픽셀 RPG 마을"만 기록한다. 이 프로젝트는 페이지마다 다른 스타일을 연습하는 곳이라 `mole.html`(밝은 잔디밭), `rps.html`(밝은 오락실 캐비닛), `bo.html`(밤의 숲), `arcade.html`(네온 아케이드)은 **의도적으로 각자 다른 세계**이며 이 시스템을 따르지 않는다. 게임들이 공통 스타일을 가질지는 아직 정하지 않았다. 앞으로 어떤 페이지가 이 세계를 쓰기로 고르면 그때 이 문서가 기준이 된다.

## Overview

**Creative North Star: "숲속 픽셀 RPG 마을"**

페이지 전체가 위에서 내려다본 도트 RPG 지도다. 두 가지 초록이 번갈아 깔린 잔디 타일 위로 모래색 흙길이 창과 창 사이를 좌우로 꺾이며 내려가고, 가장자리에는 도트 나무와 덤불, 꽃이 서 있고, 도트 낙엽이 끊어지는 프레임으로 떨어진다. 만든 사람은 이 지도 속 캐릭터로 등장한다. 표정을 바꿀 수 있는 16×16 도트 스프라이트, 이름, "Lv.1 게임 만드는 연습생"이라는 직업이 상태창에 뜨고, 대화창이 인사를 한 글자씩 친다.

모든 내용은 고전 JRPG 창 안에 산다. 남색 바탕, 흰 4px 테두리, 모서리가 한 칸씩 깎인 도트 프레임, 창 위에 얹힌 이름표. 노란색은 라벨과 ▶ 커서를 표시하는 색이다. 글꼴은 직접 올려 둔 갈무리 도트체 하나뿐이고, 둥근 모서리, 흐린 그림자, 부드러운 이징이 없다. 모든 움직임은 `steps()`로 끊어진다. 이모지는 문구 속에서 만든 사람의 말투로 남고, UI 아이콘은 전부 스크립트가 그리는 도트 SVG다.

밀도는 휴대폰 우선이다. 한 줄로 쌓인 창 사이를 흙길이 지나가고, 넓은 화면에서는 상태창과 대화창, 취미와 TMI가 나란히 선다.

**Key Characteristics:**
- 8px 타일 격자(`--t`)가 모든 간격을 정하고, 4px가 가장 작은 도트 단위다.
- 남색 JRPG 창 + 흰 도트 프레임 + 위에 얹힌 이름표.
- 갈무리 도트체를 글꼴 고유 크기(11·22·33px, 14px)로만 쓴다.
- 반경 0, 흐림 0. 깊이는 단색 테두리, 바깥 남색 링, 아래로 떨어지는 잔디 그림자로 만든다.
- 움직임은 전부 계단식(`steps()`), 낙엽·스프라이트·커서가 세계를 살아 있게 한다.
- 고른 줄은 색이 뒤집힌다(흰 바탕 + 남색 글자) 그리고 ▶ 커서가 깜박인다.

## Colors

잔디 초록과 흙길 모래색으로 된 지도 위에, 짙은 남색 창과 흰 글자, 노란 표시색이 얹히는 팔레트다.

### Primary
- **밤하늘 창 남색** (`win`): 모든 RPG 창의 바탕. 페이지에서 가장 넓게 쓰이는 "내용" 색이다.
- **창 그림자 남색** (`win-deep`): 도트 프레임의 바깥 윤곽, 이름표 바탕, 명령 창과 게이지 받침, 색이 뒤집힌 선택 줄의 글자색, 칩 글자색.

### Secondary
- **표시 노랑** (`gold`): 라벨(이름표 글자, 상태창 항목명, 취미 이름), ▶ 커서, ▼ 다음 표시, 레벨·날짜·카운트 칩 바탕, 포커스 링, 텍스트 선택색. 정보를 "가리키는" 일만 한다.
- **체력 초록** (`hp`): 채워진 경험치 칸과 퀘스트 게이지 칸, "플레이" 칩. 진행과 "갈 수 있음"을 뜻한다.

### Tertiary
- **경고 주황빨강** (`red`): 남은 시간 2초 이하의 깜박이는 타이머와 "Time Over!" 결과 창에만 쓴다.

### Neutral
- **흰 글자 / 흰 프레임** (`ink`): 본문 글자, 창 프레임의 흰 띠, 이름표·초상화·썸네일의 4px 테두리, 선택 줄과 눌린 명령의 반전 바탕, 말풍선.
- **흐린 하늘색 글자** (`ink-soft`): 보조 설명(게임 설명, 취미 설명, 대화창 힌트, 타이머 안내, "Made with"), "구경" 칩 바탕.
- **선택 줄 보조 글자** (`ink-selected-soft`): 흰 바탕으로 뒤집힌 메뉴 줄 안의 설명 글자.
- **빈 슬롯 남색** (`slot`): 비어 있는 경험치·게이지 칸, 인벤토리 슬롯 바탕.
- **잔디** (`grass`, `grass-alt`): 32px 칸이 번갈아 깔리는 잔디 타일의 두 초록. `grass`는 `theme-color`이기도 하다.
- **풀잎 그늘 / 풀잎 빛** (`grass-dark`, `grass-light`): 타일 위 풀잎 도트, 스크롤바 트랙, 초상화 발밑 잔디 띠.
- **흙길 / 흙길 가장자리** (`path`, `path-edge`): 창 사이를 꺾이며 내려가는 흙길의 안쪽 띠와 바깥 띠.

### Named Rules
**The Gold Points Rule.** 노랑은 무언가를 가리킬 때만 쓴다: 라벨, 커서, 포커스, 칩. 큰 면이나 장식 배경에 쓰지 않는다.

**The Inverted Selection Rule.** 고른 것은 흰 바탕(`ink`)에 남색 글자(`win-deep`)로 뒤집는다. 메뉴 줄과 명령 버튼이 같은 문법을 쓴다.

## Typography

**Display Font:** Galmuri11 Bold (대체: Malgun Gothic, sans-serif)
**Body Font:** Galmuri14 (대체: Malgun Gothic, sans-serif)

**Character:** 두 갈무리 도트체 모두 `fonts/`에 직접 올려 둔 woff2(OFL)다. 굵은 Galmuri11은 이름과 짧은 표시용, 가는 Galmuri14는 읽는 글용으로 나뉜다.

### Hierarchy
- **Display** (700, 33px, 40px): 지역 이름 배너 "어서오세요!"와 상태창의 이름. 400px 이하에서 배너는 22px/32px로 내려간다.
- **Headline** (700, 22px, 32px): 퀘스트 결과 창("Mission Complete!", "Time Over!").
- **Title** (400, 14px, 32px): 창 위 이름표. 노란 글자.
- **Body** (400, 14px, 24px): 모든 본문, 상태창 항목, 게임 이름, TMI, 명령 버튼.
- **Body-dialog** (400, 14px, 32px): 대화창 대사. 줄 간격을 한 타일 넓혀 타자 치는 대사가 숨 쉴 자리를 준다.
- **Label** (700, 11px, 16px): 게임·취미 설명, 대화창 힌트. 이름 바로 아래 4px 띄워 붙는다.
- **Label-chip** (700, 11px, 24px): 레벨 칩과 "플레이"/"구경" 칩.

### Named Rules
**The Native Size Rule.** 갈무리는 비트맵 격자에 맞는 크기로만 쓴다: Galmuri11은 11·22·33px, Galmuri14는 14px. 그 사이 크기는 도트가 뭉개진다.

**The Two-Step Pair Rule.** 목록 줄의 이름과 설명은 Body 14px와 Label 11px로 한 단계 차이를 두고, 설명은 `ink-soft`로 물린다.

## Layout

공간 모델은 지도 위에 세로로 쌓인 창들이다. 본문 폭은 최대 960px, 바깥 여백 24px(넓은 화면 위쪽 40px), 창 사이 간격 32px. 창 안 여백은 16px(400px 이하 8px). 모든 간격은 8px 타일(`--t`)의 배수이고, 테두리·게이지 틈·라벨 간격 같은 미세 단위만 4px를 쓴다.

배경 장면(잔디 타일, 흙길, 나무, 꽃)은 본문 폭을 넘어 화면 전체 폭에 깔린다. 흙길은 화면 가운데에서 출발해 창과 창 사이 틈마다 좌우로 꺾이고(가로·세로 직선만), 맨 아래 숲 끝 나무 줄의 가운데 틈으로 빠져나간다. 좁은 화면에서는 나무가 창 뒤로 살짝 보이고, 넓은 화면에서는 양쪽 잔디에 흙길을 비켜 서 있다.

반응형은 두 지점이다. 860px 이상: 상태창(1.15fr)과 대화창(1fr), 취미와 TMI(1:1)가 나란히 서고, 게임 메뉴는 2열, 명령은 4열. 400px 이하: 배너 글자가 22px로, 초상화가 104px로, 썸네일이 48px로 줄고 세이브 포인트가 가운데 정렬 1열이 된다.

### Named Rules
**The Tile Grid Rule.** 크기와 간격은 8px의 배수, 도트 단위는 4px. 그 밖의 값이 필요하면 세계가 아니라 계산이 틀린 것이다.

## Elevation & Depth

흐림이 없는 도트 깊이다. 창은 아래로 8px 떨어지는 반투명 잔디빛 그림자(`drop-shadow`)로 지도 위에 놓인 것처럼 보이고, 테두리 있는 작은 물체(이름표, 초상화, 썸네일, 말풍선)는 흰 4px 테두리 바깥에 4px 남색 링을 둘러 프레임과 같은 이중 윤곽을 만든다. 인벤토리 슬롯만 안쪽 위·왼쪽 빛과 아래·오른쪽 그늘로 파인 칸처럼 보인다. 눌림은 4px 아래로 내려앉는 것으로 표현한다.

### Shadow Vocabulary
- **잔디 위 그림자** (`filter: drop-shadow(0 8px 0 rgba(16, 40, 20, 0.35))`): 모든 RPG 창. 수직으로만 떨어지는 지면 그림자다.
- **남색 바깥 링** (`box-shadow: 0 0 0 4px #10183f`): 흰 4px 테두리를 두른 이름표·초상화·썸네일·말풍선.
- **파인 슬롯** (`box-shadow: inset -4px -4px 0 rgba(0,0,0,0.25), inset 4px 4px 0 rgba(255,255,255,0.15)`): 인벤토리 슬롯.

### Named Rules
**The No-Blur Rule.** 그림자와 윤곽은 흐림 반경 0이다. 깊이는 도트 칸으로 만든다.

## Shapes

모서리 반경은 어디에도 없다(0px). 둥근 느낌은 창 프레임의 모서리를 도트 한 칸(4px)씩 깎는 것으로만 낸다(12px `border-image`, 남색 윤곽 4px + 흰 띠 4px + 안쪽 남색). 테두리는 4px 단색, 구분선은 4px 점선(흰색 25~35%). 말풍선 꼬리도 8px 네모와 4px 그림자 칸으로 만든 계단 모양이다. 모든 도트 그림은 `shape-rendering: crispEdges` SVG다.

## Components

### RPG 창 (Signature)
지도 위에 놓인 고전 JRPG 창. 남색 바탕, 모서리가 깎인 흰 도트 프레임, 16px 안 여백, 아래 8px 잔디 그림자. 지역 배너, 상태창, 대화창, 게임 메뉴, 취미, TMI, 미니 퀘스트, 세이브 포인트, 퀘스트 결과 창이 모두 이 창이다.

### 이름표
창 왼쪽 위에 걸친 제목 칸(창 위로 32px 솟음, 창은 24px 아래로 밀림). `win-deep` 바탕, 노란 Title 글자, 흰 4px 테두리 + 남색 링, 앞에 2배 도트 아이콘. 섹션 제목(h2)이 곧 이름표다.

### 게임 선택 메뉴
- **줄 구조:** ▶ 커서(16px) · 썸네일(56px) · 이름+설명 · 칩, 간격 8px, 안 여백 8px.
- **선택:** 포인터가 올라가거나 누르거나 포커스가 오면 그 줄이 흰 바탕·남색 글자로 뒤집히고 ▶가 0.8s `steps(2)`로 깜박인다. 첫 줄이 기본 선택.
- **포커스:** 4px 노란 링. **눌림:** 4px 아래로.
- **썸네일:** 흰 테두리 + 남색 링 안에 그 게임 페이지의 세계를 짧게 빌려 온 바탕과 3배 도트 아이콘. 썸네일 바탕색은 각 게임 세계의 것이며 이 시스템의 팔레트가 아니다.

### 칩
- **레벨/날짜/카운트:** 노란 바탕, 남색 글자, 반경 0, 좌우 8px.
- **플레이:** `hp` 초록 바탕. **구경(준비 중):** `ink-soft` 바탕.

### 명령 창 (버튼)
- **모양:** `win-deep` 받침 안의 2열(넓은 화면 4열) 명령. 최소 높이 48px, 반경 0, 배경 없음.
- **상태:** 호버·포커스·눌림에서 흰 바탕·남색 글자로 뒤집히고 ▶ 커서가 나타난다. 주 명령("눌러줘!")은 평소 노란 글자에 노란 카운트 칩을 단다.

### 인벤토리 슬롯 (취미)
56px 남색 칸에 3배 도트 아이콘, 파인 슬롯 그림자. 호버 시 4px 노란 외곽선, 눌림 시 4px 내려앉음. 옆에 노란 이름 + Label 설명.

### 게이지
경험치 막대(16×8px 칸, 4px 틈)와 퀘스트 게이지(10칸, 16px 높이, `win-deep` 받침). 빈 칸 `slot`, 찬 칸 `hp`.

### 상태창 초상화
112px(좁은 화면 104px) 칸, 흰 테두리 + 남색 링, 파란 하늘과 아래 24px 잔디 띠 위의 96px 스프라이트. 1s `steps(2)`로 4px 숨쉬기. 누르면 표정이 바뀌고, 퀘스트 성공 시 별눈, 시간 초과 시 어지러운 표정으로 상태를 알린다.

### 대화창
화자 이름표 + Body-dialog 대사가 45ms 간격으로 한 글자씩 찍히고, 끝나면 오른쪽 아래 ▼가 깜박인다. 누르면(Enter/Space 포함) 다음 대사.

### 움직임
지역 배너는 0.9s `steps(6)`로 위에서 떨어진다. 배경 낙엽은 3배 도트 잎이 계단식으로 흔들리며 떨어지고, 잔디나 창 테두리를 누르면 잎 6장이 1.4s `steps(14)`로 흩날렸다 사라진다. 움직임 줄이기 설정에서는 애니메이션을 멈추고 떨어지는 낙엽을 숨긴다.

## Do's and Don'ts

### Do:
- **Do** 새 내용은 RPG 창(남색 바탕, 깎인 흰 도트 프레임, 16px 안 여백, 8px 잔디 그림자)에 담고 제목은 창 위 이름표로 단다.
- **Do** 모든 크기와 간격을 8px 타일의 배수로, 미세 단위는 4px로 맞춘다.
- **Do** 갈무리를 고유 크기로만 쓴다: Galmuri11 11·22·33px, Galmuri14 14px.
- **Do** 고른 것은 흰 바탕·남색 글자로 뒤집고 ▶ 커서로 가리킨다.
- **Do** 움직임은 `steps()`로 끊고, 움직임 줄이기 설정을 존중한다.
- **Do** UI 아이콘은 `crispEdges` 도트 SVG로 그리고, 이모지는 문구 속 말투로 둔다.

### Don't:
- **Don't** 모서리를 둥글리지 않는다. 둥근 느낌은 도트 한 칸 깎기로만 낸다.
- **Don't** 흐린 그림자, 그라데이션 광택, 반투명 유리 효과를 쓰지 않는다.
- **Don't** 부드러운 이징이나 연속 트랜지션을 쓰지 않는다.
- **Don't** 이모지를 UI 아이콘(버튼 아이콘, 섹션 아이콘)으로 쓰지 않는다.
- **Don't** 노랑을 큰 면이나 장식 배경으로 쓰지 않는다.
- **Don't** 다른 페이지(mole, rps, bo, arcade)를 이 시스템에 맞춰 바꾸지 않는다. 그 페이지들은 각자의 세계다.
