# Project 1: HDI 계수 와 백신 접종률 사이의 상관관계
1. csv 파일을 다운로드 받고 pandas를 이용하여 불러오기
   1. 데이터 불러오기
   2. 'date'열의 데이터를 날짜 타입으로 변경하기
2. 한국과 일본의 코로나 상황 비교 시각화하기
   1. 날짜별 확진자 비율 시각화  
      ![날짜별 확진자 비율](https://github.com/user-attachments/assets/64466ed1-71da-4131-8c8b-e2869a635d35)
   2. 날짜별 신규 확진자 비율 시각화  
      ![날짜별 신규 확진자 비율](https://github.com/user-attachments/assets/086b0ee6-b9ab-4196-9e40-6453421799c1)
   3. 날짜별 백신 접종자 비율 시각화  
      ![날짜별 백신 접종자 비율](https://github.com/user-attachments/assets/ab4ec05b-80fc-44e6-b6d8-f7bc59385313)
   4. 날짜별 백신 접종 완료자 비율 시각화  
      ![날짜별 백신 접종 완료자 비율](https://github.com/user-attachments/assets/5bcaa554-655f-41c1-ac82-7120a31c76b8)
3. 백신 접종률과 확진자 비율 대비 사망자 비율 사이의 상관관계 알아보기
   1. 데이터에서 특정 열만 남긴 새로운 데이터프레임 생성하기
   2. 각 국가별로 가장 최근 날짜의 데이터 추출하기
   3. 백신 접종률(x축), 확진자 비율 대비 사망자 비율(y축) scatter plot  
      ![백신 접종률 vs 사망자 비율](https://github.com/user-attachments/assets/16d8b83f-58ac-4347-902f-c5eb91779361)
   4. 상관계수(Pearson Correlation Coefficient) 구하기
4. HDI 계수 와 백신 접종률 사이의 상관관계 알아보기
   1. Pearson Correlation Coefficient 구하기
   2. Linear Regression 학습
   3. HDI 계수(x축), 백신 접종률(y축) scatter plot + 회귀직선  
      ![HDI vs 백신 접종률](https://github.com/user-attachments/assets/8f5a4f34-905f-4300-830e-1af08990f799)

# Project 2: 514번 User에게 영화 추천
1. 데이터 준비하기
   1. 파일을 다운로드 받고, ratings.csv 파일을 읽어서 80% 20% 비율의 train, test 데이터로 나누기
   2. movies.csv 파일을 읽고, 장르를 집합으로 변환하기
   3. tags.csv 파일을 읽고, tag들을 모두 소문자로 변환 후, 영화별로 tag들을 묶어서 집합으로 변환하기
2. Latent Factor 모델을 이용하여 학습하기
   1. P, Q 등 파라미터 초기화 후, optimizer 등을 이용해서 학습하기
   2. 학습데이터와 검증데이터에 대해서 각각 RMSE값을 구하여 출력하기  
      ![RMSE 출력](https://github.com/user-attachments/assets/32fb7c1c-df78-41d4-be43-744298da1844)
3. 514번 User에게 추천하기
   1. 514번 user의 예상 별점이 가장 높은 영화 20개를 찾아서 id 및 영화 이름 출력하기
   2. 장르 및 tag를 기준으로, 514번 user가 5점을 준 영화들을 찾고, 각각의 영화와 가장 유사한 영화를 5개씩 찾아서 id, 영화 이름, 유사도 점수 출력하기
4. 영화 클러스터링하기
   1. cosine similarity를 기준으로 영화 벡터 (P혹은 Q)에서 k-means clustering
   2. Task 4-1에서 구한 결과를 matplotlib를 활용하여 그래프로 그린 후 가장 적절해 보이는 k값 선택하기  
      ![k-means clustering](https://github.com/user-attachments/assets/404e65d6-4fcc-4ebb-b007-5134c9db4bc4)
5. 차원 축소 및 시각화
   1. P 행렬와 Q 행렬을 합쳐 Z행렬 만들기
   2. Z 행렬에서 PCA 수행하여 2차원 데이터로 줄인 Zp 만들기
   3. matplotlib을 활용하여 Zp의 scatter plot 그리기  
      ![차원 축소 시각화](https://github.com/user-attachments/assets/2d7e85ae-3387-4d97-acee-3a6cf609d1cb)

