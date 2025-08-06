# 🛒 쿠팡 물티슈 데이터 크롤링 & 분석 프로젝트

## 📌 1. 프로젝트 개요
- **목적**: 쿠팡에서 '물티슈' 상품 데이터를 크롤링하여 가격, 리뷰수 분석 및 시각화를 통해 인기 상품과 가성비 상품 파악
- **기간**: 2025년 8월
- **기술 스택**: 
  - Python
  - Selenium (undetected-chromedriver)
  - BeautifulSoup
  - Pandas
  - Matplotlib

---

## 📌 2. 주요 기능
### 🔍 데이터 수집
- 쿠팡 검색 결과 **랭킹순(scoreDesc)** + **36개씩 보기(listSize=36)** 설정
- 1~5페이지 크롤링, 스크롤 끝까지 자동 로딩
- 수집 데이터: **제품명, 가격, 리뷰수, 상세페이지 링크**
- CSV 저장 및 중복 제거

### 📊 데이터 분석 & 시각화
1. 가격 분포 분석
2. 리뷰수 상위 10개 상품
3. 가성비 상위 10개 상품
4. 가격 vs 리뷰수 산점도 분석 (Top 5 강조)

---

## 📌 3. 실행 방법
```bash
# 필수 패키지 설치
pip install undetected-chromedriver beautifulsoup4 pandas matplotlib

# 크롤링 실행 (주피터 노트북)
jupyter notebook coupang_crawling.ipynb

# 분석 & 시각화 실행 (주피터 노트북)
jupyter notebook coupang_analysis_visualization.ipynb
```

---

## 📌 4. 결과 예시
> 각 항목을 클릭하면 **원본 이미지를 새 탭에서 확인**할 수 있습니다.

### [💰 **가격 분포**](https://raw.githubusercontent.com/gyunhwank/coupang-wet-tissue-analysis/main/images/price_distribution.png)

<img width="2053" height="1415" alt="Image" src="https://github.com/user-attachments/assets/c93ddaa8-046e-404f-ad44-4add01fe80a6" />

### [⭐ **리뷰수 TOP 10**](https://raw.githubusercontent.com/gyunhwank/coupang-wet-tissue-analysis/main/images/top10_reviews.png)

<img width="3939" height="1645" alt="Image" src="https://github.com/user-attachments/assets/b4923e0a-e458-42bb-a98d-b1b973806efd" />

### [📈 **가성비 TOP 10**](https://raw.githubusercontent.com/gyunhwank/coupang-wet-tissue-analysis/main/images/top10_value.png)

<img width="3939" height="1646" alt="Image" src="https://github.com/user-attachments/assets/72c0fe6e-07fc-4a56-aed9-dba2401d72f5" />

### [🔍 **가격 vs 리뷰수 산점도**](https://raw.githubusercontent.com/gyunhwank/coupang-wet-tissue-analysis/main/images/scatter_price_reviews.png)

<img width="2145" height="1646" alt="Image" src="https://github.com/user-attachments/assets/852e8f5c-1873-47f8-90d3-4081e1264308" />


---

## 📌 5. 분석 인사이트
1. 리뷰수 상위권은 대부분 1~2만원대 제품
2. 가성비 상위권과 리뷰수 상위권이 상당 부분 일치
3. 고가 제품은 리뷰수가 적어 틈새시장에 해당

---

## 📌 6. 향후 확장 아이디어
- 키워드별 카테고리 비교 분석
- 기간별 가격 변동 추적
- 머신러닝 기반 판매량 예측 모델 개발

---

📂 **데이터 파일**: [`coupang_wet_tissue_rank36_pages1to5.csv`](coupang_wet_tissue_rank36_pages1to5.csv)  
📊 **이미지**: [`images/`](images/)
