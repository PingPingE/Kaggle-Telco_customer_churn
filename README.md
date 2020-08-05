<strong>*만약 위 파일의 로딩에 실패한다면-> https://nbviewer.jupyter.org/github/PingPingE/Kaggle-Telco_customer_churn/blob/master/telco-customer-churn.ipynb </strong>

# 통신사 고객의 가입 해지 여부 예측 모델

## 현재 진행 상황
- 데이터 확인
- 전처리
    - 결측값 처리 (TotalCharges의 결측값 -> MonthlyCharges*Contract)
    - Binning
            - TotalCharges
            - MonthlyCharges
    - 타입변환
    
- 파생컬럼 생성
    - 백업, 보안, 다양한 서비스 이용 여부 등으로 디지털 친화도 측정 -> familiar_with_ digital

- EDA
    - 각 컬럼과 Churn컬럼(결과값)의 상관관계 분석
    - 분석을 토대로 구체적인 가설을 세우고 검증하기 (진행 중)
    
- 모델 적용 및 평가
    - One-hot encoding vs Label encoding
    - Under sampling(random) vs Over sampling(random) vs Over sampling(smote)
    - EDA를 토대로 Feature selection (진행 중)
    - ML모델 적용(LightGBM,Logistic regression,SVM 등) (진행 중)
    - 평가(진행 중)
        - cross validation
        - ROC curve
        - AUC
        - classification report

- 최적화 (진행 중)
    - Grid Search cv

- 최종 결과 분석 (진행 중)
<br>

## 데이터
- gender(성별)<br>
    Whether the customer is a male or a female


- SeniorCitizen(고령자 여부)<br>
    Whether the customer is a senior citizen or not (1, 0)


- Partner(배우자 유무)<br>
    Whether the customer has a partner or not (Yes, No)


- Dependents(부양가족 유무)<br>
    Whether the customer has dependents or not (Yes, No)


- tenure(근속월수)<br>
    Number of <strong>months</strong> the customer has stayed with the company


- PhoneService(휴대폰 유무)<br>
    Whether the customer has a phone service or not (Yes, No)


- MultipleLines(휴대폰 2개 이상 여부)<br>
    Whether the customer has multiple lines or not (Yes, No, No phone service)


- InternetService(인터넷 이용 여부 + 종류)<br>
    Customer’s internet service provider (DSL, Fiber optic, No)


- OnlineSecurity(보안 설정 여부)<br>
    Whether the customer has online security or not (Yes, No, No internet service)
    
    
- OnlineBackup(온라인 백업 여부)<br>
    Whether the customer has online backup or not (Yes, No, No internet service)

 
- DeviceProtection(단말기 보안 설정 여부)<br>
    Whether the customer has device protection or not (Yes, No, No internet service)


- TechSupport(기술 지원 여부)<br>
    Whether the customer has tech support or not (Yes, No, No internet service)


- StreamingTV(TV 시청 여부) <br>
    Whether the customer has streaming TV or not (Yes, No, No internet service)


- StreamingMovies(영화 시청 여부) <br>
    Whether the customer has streaming movies or not (Yes, No, No internet service)


- Contract(약정 기간) <br>
    The contract term of the customer (Month-to-month, One year, Two year)


- PaperlessBilling(디지털 청구서 수신 여부) <br>
    Whether the customer has paperless billing or not (Yes, No)


- PaymentMethod(결제 방식)<br>
    The customer’s payment method (Electronic check, Mailed check, Bank transfer (automatic), Credit card (automatic))


- MonthlyCharges(월 지불 금액)  <br>
    The amount charged to the customer monthly


- TotalCharges(지불할 총 금액) <br>
    The total amount charged to the customer


- Churn (가입 해지 여부)<br>
    Whether the customer churned or not (Yes or No)
