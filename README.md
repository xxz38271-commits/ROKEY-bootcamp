# ROKEY Bootcamp Projects 🤖
**두산로보틱스 ROKEY 부트캠프 프로젝트 모음**

> ROS2 기반 로봇 시스템 개발 | 두산로보틱스 ROKEY 부트캠프 수료

---

## 부트캠프 개요

- **주관**: 두산로보틱스
- **내용**: ROS2 기반 협동로봇 시스템 설계 및 구현
- **사용 기술**: ROS2, Python, C++, Ubuntu

---

## 프로젝트 목록

###  Project 1. ROBURGER - 버거 조립 자동화 시스템
두산 협동로봇 M0609를 활용한 햄버거 전 공정 자동화

**나의 역할**: ROS 환경 통합, 예외 처리 로직 구현, Firebase DB 구축

**핵심 구현 내용**
- ROS2 기반 버거 조립 시퀀스 전체 제어 (`/burger_job`, `/robot_stop`, `/robot_recovery`)
- Firebase 실시간 DB 연동으로 주문 데이터 수신 및 로봇 상태 동기화
- 긴급 정지 및 복구 모드 예외 처리 로직 구현
- ROS Bridge를 통한 ROS2 ↔ Firebase ↔ React UI 통합
- 커스텀 3D 프린팅 그리퍼 및 뒤집개, 집게 툴 체인지 시스템 적용

**사용 기술**
`ROS2` `Python` `Firebase` `ROS Bridge` `React` `Ubuntu 22.04`

**링크**: [GitHub](https://github.com/rokey5-cobot/cobot1_roburger)

---

###  Project 2. Auto Valet Garage - TurtleBot4 기반 무인 자동 주차 시스템
TurtleBot4 2대가 협동하여 입차부터 출차까지 자동화하는 무인 주차 관제 시스템

**나의 역할**: AMR 자율 주행 제어, 이중주차 협동 제어 FSM 구현

**핵심 구현 내용**
- Nav2 + AMCL 기반 TurtleBot4 자율 주행 미션 실행 시스템 구현
- HSV 필터 + Contour 검출 기반 라인 트레이싱으로 주차 구역 정밀 정렬
- SINGLE / DOUBLE 출차 판별 및 4-Phase FSM으로 2대 협동 제어
- Dock / Undock 비동기 액션 처리 및 idle 시 자동 도킹

**사용 기술**
`ROS2` `Python` `Nav2` `TurtleBot4` `YOLOv8` `OpenCV` `Supabase`

**링크**: [GitHub](https://github.com/xxz38271-commits/AutoValetGarage)
---

###  Project 3. Smart Surgical Assistant - 지능형 수술 보조 협동로봇
음성 인식과 AI 비전 기반 수술 도구 자동 전달 시스템

**나의 역할**: 로봇 제어(Pick & Place) 로직 구현, 예외 처리, 시스템 통합

**핵심 구현 내용**
- YOLOv11-pose로 수술 도구 위치 및 Keypoint 인식 후 Pick & Place 로직 구현
- MediaPipe 손 추적으로 의료진 손 위치 감지, 안전한 도구 전달 로직 구현
- OpenAI Whisper 음성 인식으로 수술 도구 요청 및 긴급 정지 명령 처리
- ROS2 기반 전체 시스템 통합 및 예외 처리
- Supabase 연동으로 수술 도구 사용 현황 실시간 모니터링

**사용 기술**
`ROS2` `Python` `YOLOv11` `MediaPipe` `OpenAI Whisper` `Flask` `Supabase`

**링크**: [GitHub](https://github.com/rokey5-cobot/cobot2_surgeon)

---

## 기술 스택

![ROS2](https://img.shields.io/badge/ROS2-22314E?style=flat&logo=ros&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=cplusplus&logoColor=white)
![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=flat&logo=ubuntu&logoColor=white)

---

## 레포지토리 구조

```
rokey-bootcamp/
├── burger_assembly/      # 버거 조립 로봇
│   ├── src/
│   ├── launch/
│   └── README.md
├── autonomous_vehicle/   # 자율주행 ERP42
│   ├── src/
│   ├── launch/
│   └── README.md
└── multi_robot/          # 멀티 로봇 협업
    ├── src/
    ├── launch/
    └── README.md
```

---


