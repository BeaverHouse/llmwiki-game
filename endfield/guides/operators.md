---
title: 오퍼레이터 개요
type: hub
status: ai-draft
aliases: [오퍼레이터, 오퍼레이터 목록, 캐릭터 목록, 직군, 속성, 능력치]
sources:
  - https://namu.wiki/w/명일방주:%20엔드필드/오퍼레이터 (2026-09-02 수정본, CC BY-NC-SA 2.0 KR)
  - user-feedback: 사·명하 출시 확인 (2026-10-19)
created: 2026-10-14
updated: 2026-10-19
---

# 오퍼레이터 개요

오퍼레이터의 등급, 능력치, 직군을 정리하고 전체 명단을 속성·무기·직군으로 나눈다. 개별 오퍼레이터의 스킬과 운용은 operators/ 아래 문서에서, 전투 규칙은 [전투 기본 체계](combat_basics.md)와 [아츠 이상과 물리 이상](status_anomalies.md)에서, 파티 사이클은 [전기 파티](../parties/electric.md)·[물리 파티](../parties/physical.md)에서 다룬다. 고유명사 표기는 [glossary.md](../glossary.md)를 따른다.

## 등급

4성부터 6성까지 있다. 등급이 높을수록 기본 능력치가 조금 더 높고, 육성에 드는 재료는 등급과 관계없이 같다.

## 능력치

모든 오퍼레이터는 힘, 민첩, 지능, 의지 가운데 하나를 주요 능력치, 하나를 보조 능력치로 가진다. 어느 것이 주요·보조인지는 오퍼레이터마다 다르며, 오퍼레이터 상태창에서 주요 능력치는 노란색, 보조 능력치는 흰색으로 표시된다. 주요 능력치는 1당 공격력을 0.5%, 보조 능력치는 1당 약 0.2% 올린다.

주요·보조 여부와 관계없이 네 능력치는 각자 다른 효과도 가진다.

| 능력치 | 효과 |
|---|---|
| 힘 | 1당 최대 생명력 +5 |
| 민첩 | 물리 저항 증가. 증가량은 100 − 100 / (민첩 × 0.001 + 1) |
| 지능 | 아츠 저항 증가. 증가량은 100 − 100 / (지능 × 0.001 + 1) |
| 의지 | 1당 받는 치유 효율 +0.1% (주는 치유량이 아니다) |

저항 1은 받는 피해 1% 감소에 해당한다. 그 밖의 전투 능력치는 다음과 같다.

- 방어력: 기본 0이며 장비로 올린다. 높을수록 받는 모든 피해가 비율로 줄어든다. 5성 장비 4개를 끼면 방어력 140, 받는 피해 58.33% 감소.
- 치명타 확률 기본 5%, 치명타 피해 기본 50%.
- 오리지늄 아츠 강도: 물리 이상, 아츠 이상, 아츠 폭발의 효과를 키운다. 증가 효과는 모두 곱연산으로 적용된다.

## 직군

| 직군 | 역할 |
|---|---|
| 가드 | 방어 불능 피해와 물리 이상 부여에 능하고, 공격 능력도 어느 정도 갖췄다 |
| 캐스터 | 아츠 부착 피해와 아츠 이상 부여에 능하고, 공격 능력도 어느 정도 갖췄다 |
| 스트라이커 | 다른 오퍼레이터의 물리 공격과 아츠 효과를 활용해 결정적인 피해를 준다 |
| 뱅가드 | 스킬 게이지 회복에 능해 팀원이 스킬을 더 자주 쓰게 돕는다 |
| 디펜더 | 생존력이 뛰어나고 팀원 보호·치료와 반격에 능하다 |
| 서포터 | 각종 제어 효과로 적을 약화하고 다른 오퍼레이터에게 버프와 지원을 준다 |

## 무기와 장비

무기는 한손검, 양손검, 장병기, 권총, 아츠 유닛의 다섯 종류이며, 오퍼레이터마다 쓸 수 있는 종류가 하나로 정해져 있다. 5~6성 무기에는 전용 무기 개념이 있지만, 게임 안에 어느 오퍼레이터의 전용인지 적혀 있지 않다. 무기의 능력치 옵션이 오퍼레이터의 주요 능력치와 일치하는지로 대략 판단하며, 작전 매뉴얼 → 훈련 → 오퍼레이터 가이드의 훈련 모드(4차 정예화 레벨 80, 무기 3차 돌파 레벨 80 고정)에 장착된 무기로도 확인할 수 있다.

장비는 방어구, 보호 장갑, 부품 두 칸으로 이루어진다. 공장에서 부품을 제작해야 해서 소홀하기 쉽지만 효과가 크다.

## 명단

나무위키 오퍼레이터 틀(2026-09-02 기준)의 34명이다. 사와 명하는 출시되었다 (Austin 확인, 2026-10-19); 두 사람의 오퍼레이터 문서는 작성 대기 중이다.

| 오퍼레이터 | 속성 | 무기 | 직군 | 문서 |
|---|---|---|---|---|
| 관리자 | 물리 | 한손검 | 가드 | [operators/endministrator.md](../operators/endministrator.md) |
| 카치르 | 물리 | 양손검 | 디펜더 | [operators/catcher.md](../operators/catcher.md) |
| 진천우 | 물리 | 한손검 | 가드 | [operators/chen_qianyu.md](../operators/chen_qianyu.md) |
| 판 | 물리 | 양손검 | 스트라이커 | [operators/da_pan.md](../operators/da_pan.md) |
| 여풍 | 물리 | 장병기 | 가드 | [operators/lifeng.md](../operators/lifeng.md) |
| 포그라니치니크 | 물리 | 한손검 | 뱅가드 | [operators/pogranichnik.md](../operators/pogranichnik.md) |
| 로시 | 물리 | 한손검 | 가드 | [operators/rossi.md](../operators/rossi.md) |
| 미브 | 물리 | 양손검 | 가드 | [operators/mi_fu.md](../operators/mi_fu.md) |
| 푸치나 | 물리 | 한손검 | 디펜더 | [operators/purrchena.md](../operators/purrchena.md) |
| 에스텔라 | 냉기 | 장병기 | 가드 | [operators/estella.md](../operators/estella.md) |
| 자이히 | 냉기 | 아츠 유닛 | 서포터 | [operators/xaihi.md](../operators/xaihi.md) |
| 알레쉬 | 냉기 | 한손검 | 뱅가드 | [operators/alesh.md](../operators/alesh.md) |
| 스노우샤인 | 냉기 | 양손검 | 디펜더 | [operators/snowshine.md](../operators/snowshine.md) |
| 라스트 라이트 | 냉기 | 양손검 | 스트라이커 | [operators/last_rite.md](../operators/last_rite.md) |
| 이본 | 냉기 | 권총 | 스트라이커 | [operators/yvonne.md](../operators/yvonne.md) |
| 탕탕 | 냉기 | 권총 | 캐스터 | [operators/tangtang.md](../operators/tangtang.md) |
| 사 | 냉기 | 양손검 | 서포터 | 문서 작성 대기 |
| 아케쿠리 | 열기 | 한손검 | 뱅가드 | [operators/akekuri.md](../operators/akekuri.md) |
| 울프가드 | 열기 | 권총 | 캐스터 | [operators/wulfgard.md](../operators/wulfgard.md) |
| 엠버 | 열기 | 양손검 | 디펜더 | [operators/ember.md](../operators/ember.md) |
| 레바테인 | 열기 | 한손검 | 스트라이커 | [operators/laevatain.md](../operators/laevatain.md) |
| 카뮤 | 열기 | 장병기 | 뱅가드 | [operators/camille.md](../operators/camille.md) |
| 플루라이트 | 자연 | 권총 | 캐스터 | [operators/fluorite.md](../operators/fluorite.md) |
| 아델리아 | 자연 | 아츠 유닛 | 서포터 | [operators/ardelia.md](../operators/ardelia.md) |
| 질베르타 | 자연 | 아츠 유닛 | 서포터 | [operators/gilberta.md](../operators/gilberta.md) |
| 결 | 자연 | 아츠 유닛 | 캐스터 | [operators/arcane.md](../operators/arcane.md) |
| 티프로스 | 자연 | 아츠 유닛 | 스트라이커 | [operators/typhoeus.md](../operators/typhoeus.md) |
| 안탈 | 전기 | 아츠 유닛 | 서포터 | [operators/antal.md](../operators/antal.md) |
| 펠리카 | 전기 | 아츠 유닛 | 캐스터 | [operators/perlica.md](../operators/perlica.md) |
| 아비웨나 | 전기 | 장병기 | 스트라이커 | [operators/avywenna.md](../operators/avywenna.md) |
| 아크라이트 | 전기 | 한손검 | 뱅가드 | [operators/arclight.md](../operators/arclight.md) |
| 장방이 | 전기 | 아츠 유닛 | 스트라이커 | [operators/zhuang_fangyi.md](../operators/zhuang_fangyi.md) |
| 리노 | 전기 | 장병기 | 서포터 | [operators/liino.md](../operators/liino.md) |
| 명하 | 전기 | 한손검 | 가드 | 문서 작성 대기 |

## 기타

- 모든 오퍼레이터에게 특정 카메라 앵글에 대응하는 특수 대기 모션이 있다.
- 모든 오퍼레이터는 수영을 하지 못해, 물에 빠지면 쓰러진 뒤 근처에서 다시 나타난다.

## 확인하지 못한 것

- 오퍼레이터별 등급. 개별 문서를 쓰면서 채운다.

## 히스토리

- 2026-10-18: 전투 체계·이상 상태·파티 문서 링크 추가.
- 2026-10-15: 카치르·판·여풍·푸치나 문서 연결. 관리자를 제외한 출시 오퍼레이터 문서가 모두 연결됨.
- 2026-10-19: 사와 명하가 출시되었음을 표시 (Austin 확인). 문서는 작성 대기.
- 2026-10-14: 사와 명하가 아직 출시되지 않았음을 표시 (Austin 확인). 리노·안탈·아비웨나 문서 연결.
- 2026-10: 최초 작성. 나무위키 오퍼레이터 문서 2026-09-02 수정본 기준.
