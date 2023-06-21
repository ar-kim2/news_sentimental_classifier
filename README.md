# news_sentimental_classifier
뉴스기사 감성분류 및 KOSPI 연관성 분석


## 프로젝트 소개
KLUE-Bert 모델기반 증시뉴스 긍/부정 감성분류.
뉴스 긍/부정 분류 결과와 KOSPI 지수와의 연관성 분석.
<br>

### 개발 기간
* 23.05.29일 - 23.06.30일

### 적용기술
- **분석 및 프로그래밍**: Python, Pandas, Tensorflow, Jupyter lab
- **데이터 시각화**: Plotly, Seaborn
- **예측 및 분류 모델**: KLUE-Bert, LSTM, Bi-LSTM
- **데이터 수집** : : BeautifulSoup, Selenium

### 데이터 출처 및 참고
- KRX 정보데이터 시스템
- FinancialPhraseBank Dataset (Malo et al., 2014)  
  ref: https://github.com/ukairia777/finance_sentiment_corpus
- 한국경제, 인포스탁, 연합인포맥스, 서울경제, inews, paxnet (data crawling)

## 분석결과
### 활용데이터
- 기간: 2021.01.01-2023.05.31
- 총 133511개
  - 긍정뉴스: 47,042개, 부정뉴스: 13,736개, 중립뉴스: 72,733개

### 분석 Feature
- 긍부정 뉴스 비율 (부정 뉴스 가중치 적용)
  - (긍정뉴스-(부정뉴스*2))/일별 총 뉴스개수

### 시간에 따른 KOSPI(등락률)와 긍부정 뉴스 비율의 관계
- 뉴스 긍부정 비율과 KOSPI 등락률이 어느정도 유사하게 움직임.
![20230621_115638](https://github.com/ar-kim2/news_sentimental_classifier/assets/60689555/4d2791c8-5aa6-49e7-b10d-97d4dec43888)

### 장외 (15:00-9:00) 긍부정 뉴스 비율과 KOSPI 등락률 과의 관계
- 긍부정 뉴스 비율이 KOSPI(등락률)을 후행하는 성향이 나타남.
![20230621_115932](https://github.com/ar-kim2/news_sentimental_classifier/assets/60689555/89a16dfa-526b-4501-ba44-4986c3e66f1e)

