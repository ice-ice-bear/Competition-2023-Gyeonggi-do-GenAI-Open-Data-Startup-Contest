## 💡 2023 경기도 GenAI·공공데이터 창업경진대회

### 🖥️ 활용 언어 및 패키지
<p align="left">
  <a href="https://www.python.org/" target="_blank" rel="noreferrer"> 
    <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="python"/> 
  </a>
  <a href="https://numpy.org/" target="_blank" rel="noreferrer"> 
    <img src="https://img.shields.io/badge/Numpy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="numpy"/> 
  </a>
  <a href="https://pandas.pydata.org/" target="_blank" rel="noreferrer"> 
    <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="pandas"/> 
  </a>
  <a href="https://opencv.org/" target="_blank" rel="noreferrer"> 
    <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white" alt="opencv"/> 
  </a>
  <a href="https://scikit-learn.org/" target="_blank" rel="noreferrer"> 
    <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="scikit-learn"/> 
  </a>
</p>

### 🧑 조 구성원
| 역할 | 이름 |
| ---- | ---- |
| 조장 | 오태훈 |
| 조원 | 이승렬, 김현수, 조민선 |

### 📊 조 이름
- 와차

## 프로젝트 개요
### 프로젝트 명
앗!차: 차량 및 인원 식별을 통한 교통 데이터 분석 시스템

### 프로젝트 주제
교통 데이터 수집과 분석을 통한 최적 루틴 추천 및 보행자 안전성 강화

### 주제 선정 배경
1. **교통 혼잡 문제 해결**: 출퇴근 시간대의 교통 혼잡도를 분석하여 최적의 교통 흐름을 제공
2. **보행자 안전성 강화**: 어린이 보호구역 등에서의 보행자 분포 데이터를 활용하여 안전한 교통 환경 조성
3. **공공 데이터 활용**: 경기도의 다양한 공공 데이터를 활용하여 교통 관련 문제를 해결

### 프로젝트 요약
- **데이터 수집 및 분석**: 경기도 공공 데이터를 활용하여 도로, 보호구역, 정류장 관련 정보 수집 및 분석
- **객체 검출 및 추적**: YOLO V8 모델을 활용한 실시간 교통 상황 모니터링
- **보행자 안전성 시스템**: 어린이 보호구역의 횡단보도 보행자 분포 데이터 수집 및 혼잡 시간 알림 시스템 구현

## 📈 활용 데이터 셋
| Dataset | 설명 | 출처 |
| ------- | ---- | ---- |
| 판교제로시티 CCTV 데이터 2D 바운딩박스 조회 | 판교제로시티의 CCTV 데이터를 활용하여 교통 흐름 분석 | 경기데이터드림 |
| 판교제로시티 CCTV 데이터 제로셔틀 경로추적 조회 | 제로셔틀의 경로 추적 데이터를 통해 이동 패턴 분석 | 경기데이터드림 |

## 👨‍💻 데이터 전처리
1. **데이터셋 준비:**
   - CCTV 영상 데이터에서 객체 검출을 위한 바운딩 박스(annotation) 데이터 추출
   - 바운딩 박스 데이터를 YOLO V8 학습 형식에 맞게 변환
2. **데이터 증강:**
   - 특수차량 이미지 데이터를 합성이미지 생성 모델을 통해 증강

## 👩‍💻 기능 구현
### 객체 검출 및 추적
- YOLO V8을 이용한 차량 및 보행자 검출
- DeepSORT를 이용한 객체 추적
- 실시간 교통 상황 모니터링

### 장기 주차 차량 식별 및 알림 시스템
- 시내 도로 및 고속도로의 주차 차량 분포 모니터링
- 시간대별 혼잡도 측정 및 관련 당국에 알림 전송

### CCTV 지능형 교통관제 시스템 확장
- 기존 교통관제 시스템에 추가 기능 탑재

## 💪 모델 학습
### YOLO V8 모델 학습
- **데이터셋 준비:** CCTV 영상에서 추출한 이미지와 바운딩 박스 라벨 데이터
- **모델 학습:** YOLO V8 사전학습 모델을 기반으로 추가 학습 수행
- **성능 개선:** 특수차량 이미지 생성을 통해 검지율 향상

### 특수차량 이미지 생성
- **모델 활용:** Inpaint Anything 및 Stable Diffusion을 활용하여 특수차량 이미지 합성
- **학습 데이터 증강:** 특수차량 이미지 데이터를 생성하여 모델 성능 개선

## 🌟 기대효과 및 실효성
### 기대효과
- 도로 안전 및 교통 효율 개선
- 교통 통계 시계열 데이터 수집 및 분석
- 장기 주차 차량에 대한 실시간 모니터링 및 알림 시스템 구축

### 실효성
- 실시간 데이터 처리와 분석을 통해 교통 효율 증대
- 특수차량 검지율 향상을 통해 다양한 교통 문제 해결
- 지역사회 안전 및 편의성 증진

## 결론
본 프로젝트는 장기 주차 차량 문제를 해결하기 위해 첨단 객체 검출 및 이미지 합성 기술을 활용한 혁신적인 솔루션을 제공합니다. 교통 안전성과 효율성을 동시에 개선할 수 있는 장기 주차 차량 단속 시스템을 통해 실질적인 교통 문제 해결을 기대합니다.
