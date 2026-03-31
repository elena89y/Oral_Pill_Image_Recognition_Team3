# Oral_Pill_Image_Recognition_Team3
[Entry-Level] AI-based Oral Pill Image Recognition and Classification System (Team 3)

[협업노트/회의록 및 진행상황](https://www.notion.so/AI8-_-_3-Pill-3251fffab02c80e696c0f492120e3012)
[📄 팀 보고서 PDF](https://github.com/elena89y/Oral_Pill_Image_Recognition_Team3/blob/main/%5BProject_1%5DTeam_3_Pill-%ED%84%B0%EB%A7%81_Report.pdf)

## 팀원

| 이름 | 역할 |
|------|------|
| 유연정 (팀장) | PM / 데이터 전처리 / 모델 설계 및 실험 |
| 김현숙 | 데이터 전처리 / 모델 설계 및 실험 |
| 이현진 | 모델 설계 및 실험 / PPT 작성 |
| 송우현 | 모델 설계 및 실험 / 하이퍼파라미터 적용 |
| 은광성 | 데이터 전처리 / 모델 실험 |

---

## 프로젝트 설명

경구용 알약 이미지를 인식하고 분류하는 객체 탐지 모델을 개발하는 프로젝트입니다.  
캐글 대회 형식으로 진행되었으며, mAP(Mean Average Precision) 및 캐글 최종 점수를 기준으로 모델 성능을 평가했습니다.

---

## 실험 과정 및 사용 모델

1. **Faster R-CNN (Baseline)** — 데이터 증강 및 WeightedRandomSampler 적용 실험
2. **Faster R-CNN backbone 교체** — ResNet50 → ResNet101 / ResNet34 시도, 성능 개선 없어 중단
3. **YOLO 도입** — YOLOv8 / YOLOv11 기반으로 전환
4. **YOLOv8s 채택** — YOLOv8s 코드가 가장 높은 점수를 기록하여 최종 채택
   - 초기: 0.989 → 개선: 0.993 → 최종: 0.994
5. **추가 실험** — YOLOv8n, YOLOv8m, YOLOv11n, YOLOv11s 비교 실험 진행, 모두 YOLOv8s보다 낮은 성능으로 포기

---

## 최종 결과

| 지표 | 점수 |
|------|------|
| Kaggle mAP | **0.99451** |
| 최종 순위 | **1등** |

---

## 파일 구조

Oral_Pill_Image_Recognition_Team3/  
├── Project_1_Team3_Final.ipynb          # 최종 제출 코드 (YOLOv8s 기반)  
├── Team_3_Pill-터링_Report.pdf          # 팀 보고서  
├── Team_3_Pill-터링_Presentation.pptx   # 발표 자료  
└── README.md                            # 데이터셋 경로 및 환경 설정 안내 포함  
                                         # (학습 데이터는 Google Drive에서 별도 다운로드)  
