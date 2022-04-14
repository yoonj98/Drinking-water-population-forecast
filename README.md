# Dacon 구내식당 식수 인원 예측 AI 경진대회
#### 팀 꿈은 없지만 놀고 싶어요 / private 90th
---
      한국토지주택공사 구내식당의 요일별 점심과 저녁 식사를 하는 인원을 예측하는 분석 프로젝트

## 📌 전체 프로세스
#### 1. 데이터 파악 및 탐색적 자료분석 (EDA)
  - 데이터 기초 통계량 확인
  - 데이터 결측치 및 불균형 확인
  - 데이터 시각화
  
#### 2. 데이터 전처리
  - 일자 변수 분리 → 요일과 시간 관련 변수 생성
  - 파생변수 생성
    - 출근 변수 생성(본사정원수 - 본사휴가자수 - 본사출장자수 - 현본사소속재택근무자수)
    - 석식이 없는 자기계발의 날을 고려하기 위해 주차 변수 및 월말 변수 생성
    - 공휴일/연휴 전후 변수 생성
  - 중식/석식 메뉴 임베딩
    - 메뉴 변수 분리 후 gensim 라이브러리의 Word2Vec을 통해 임베딩
  - 변수 삭제 → 파생변수를 생성하는 데 사용한 일부 변수 제거

#### 3. 모델링
  - Lasso Regression 모델을 통해 변수 선택
  - GridSearchCV을 통해 최적의 하이퍼 파라미터 탐색
  - RandomForest, XGBoost, LGBM 모델을 활용한 모델 구축
  
<br>

## 📌 Contributors
<table>
  <tr>
    <td align="center"><a href="https://github.com/yoonj98"><b>이윤정</b></sub></td>
    <td align="center"><a href="https://github.com/jiwon4178"><b>박지원</b></sub></td>
    <td align="center"><a href="https://github.com/didwldn3032"><b>양지우</b></sub></td>
</table>

