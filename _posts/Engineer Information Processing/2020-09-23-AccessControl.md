---
title: Access Control Model
tag: 정처기
---



## 접근 제어 / 접근 통제

### 접근 제어 절차

- 식별
- 인증
- 인가( Authorization )



### 접근 통제 정책

주체가 어떻게 객체에 접근하는지 규정하는 프레임 워크

모든 운영시스템은 reference monitor 개념이 구현된 보안 커널을 가지고 있으며, 이는 스스템에 따라 (접근 통제 정책의 유형에 따라) 다르다.

주체가 객체와 통신하기 전에 보안 커널은 요청이 허가되어 있는지 판단하기 위해 접근 통제 정책을 검토해야 한다.



#### 임의적 접근 통제, DAC , Discretionary Access Control

주체가 속해 있는 그룹의 신원에 근거하여 객체에 대한 접근을 제한한다.

대부분 OS는 DAC에 기반함.

개인 기반 정책과 그룹기반 정책을 포함한다.

> 장단점

- 필요에 따른 접근 제어가 가능해서 시스템이 융통성을 가짐.

- MAC에 비해 상대적으로 보안성이 떨어짐.

- 다른 사람의 신분을 도용하는 경우, 통제할 방법이 없음



#### 강제적 접근 통제, MAC, Mandatroy Access Control

보안 레벨, 규칙, 관리에 기반한 접근 통제 방식

기밀성 강조되는 조식에서 사용

 주체가 객체에 접근할 때, 보안 레이블과 보안 허가증을 참고하여 접근 통제한다. 쉽게, 관리자는 모든 주체, 객체 보안 레벨을 부여하고 해당 보안 레벨에 따라 접근을 허용하거나 통제하는 것이다.

> 장단점

- 확실한 규칙에 따라 통제하기 때문에 DAC보다 높은 보안성을 가진다.
- 매우 제한적인 사용자 기능과 많은 관리자 부담을 요구하며, 비용이 많이 소요된다.
- 모든 접근에 대해 보안 정책을 확인해야 하기 때문에 시스템 성능에 영향을 끼친다.
- 상업적인 환경에서 적용이 힘들다.



#### 역할기반 접근 통제, RBAC, Role Based Access Control

사용자에게 할당된 역할에 기반하여 접근을 통제하며 중앙에서 집중적으로 관리한다.

RBAC의 핵심 개념은 권한을 역할과 연관시키고, 사용자들이 적절한 역할을 할당받도록 하여 권한 관리를 용이하게 하는 것이다. 역할은 다양한 작업 기능을 ㅋ바탕으로 정의도며 사용자들은 직무에 의한 책임과 자질에 따라 역할을 할당받는다.



[정리1](https://skogkatt.tistory.com/65), [정리2](https://peemangit.tistory.com/191)