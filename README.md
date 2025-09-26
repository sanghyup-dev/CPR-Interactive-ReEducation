# interactive-online-CPR-education
interactive online CPR education
SKKU AI EDUCATION HACKERTHON

> **목표:** 이동 없이 집에서 효율적으로 심폐소생술(CPR) 재교육을 받을 수 있는 웹 플랫폼  
> **핵심:** 이론 → 실습(음성/마우스/키보드/카메라) → 최종 인증까지 이어지는 몰입형 학습

---

## 프로젝트 개요

멀티미디어 기반으로 구성된 **온라인 CPR 재교육 시스템**입니다.  
기존 오프라인 강의의 불편함(장소·시간 제약, 실습 부족)을 해소하고,  
사용자가 **즉각적 피드백**을 받으며 **정확한 절차·속도·자세**로 CPR을 수행할 수 있도록 설계했습니다.

---

## 프로젝트 동기

- **대상:** 심폐소생술 경험은 있으나 시간이 지나 기억이 흐려진 대학생·성인
- **문제:** 오프라인 교육 참여 시간·비용 부담 → 재교육율 낮음
- **해결:** 웹 브라우저에서 단계별 이론 + 실습 + 피드백 제공 → **언제든, 어디서든, 짧은 시간 내 재교육 가능**

---

## 주요 기능

| 단계 | 설명 | 기술 스택 |
|------|------|-----------|
| **이론 가이드** | CPR 기본 절차·주의사항 안내 | HTML + CSS |
| **동영상 학습** | YouTube IFrame API로 교육 영상 시청, 완료 시 자동 이동 | JavaScript |
| **음성 인터랙션** | "주황색", "119" 음성 인식 → 다음 단계 버튼 생성 | TensorFlow.js Speech-Commands |
| **마우스 실습** | 손 이미지를 올바른 위치에 Drag & Drop | HTML5 Drag & Drop API |
| **키보드 실습** | 10초 동안 ‘H’ 입력 → 100~120 타/분 속도 판정 | JS 이벤트 핸들러 |
| **카메라 자세 교정** | Teachable Machine Pose 모델로 올바른 자세 인식 | TensorFlow.js Pose |
| **수료 화면** | 최종 완료 메시지 + 이미지 | HTML/CSS |

모든 단계에서 **즉각 피드백** 제공 → 사용자가 성공 시에만 다음 단계로 진행

---

## 사용 기술

- **Frontend:** HTML5, CSS3, JavaScript (Vanilla)
- **ML 모델:** [Teachable Machine](https://teachablemachine.withgoogle.com/) Pose & Speech 모델
- **외부 API:** YouTube IFrame API
- **UI/UX:** Flexbox, Progress Steps UI, 모달(dialog) 피드백
- **실습 인터랙션:** Drag & Drop, Keydown Event, Webcam Capture

---

## 실행 방법

1. **프로젝트 클론**
   ```bash
   git clone https://github.com/sanghyup-dev/CPR-Interactive-ReEducation.git
   ```

2. **실행**
   - `guide_page.html` 브라우저에서 열기
