![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/sklearn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)
### Project Overview (프로젝트 개요)

This project integrates FastAPI and Streamlit to create a web application for predicting car prices based on specific features. (이 프로젝트는 특정 기능을 기반으로 자동차 가격을 예측하기 위해 FastAPI와 Streamlit을 통합하여 웹 애플리케이션을 만듭니다.) The dataset includes information about various cars, including their name, year of manufacture, price, kilometers driven, and fuel type. (데이터셋에는 자동차 이름, 제조 연도, 가격, 주행 거리, 연료 종류에 대한 정보가 포함되어 있습니다.)

---

### Dataset (데이터셋)

The dataset contains the following columns: (데이터셋에는 다음 열이 포함되어 있습니다:)

- **name:** The model name of the car. (모델 이름)
- **year:** The year the car was manufactured. (제조 연도)
- **Price:** The price of the car. (가격)
- **kms_driven:** The total kilometers the car has been driven. (주행 거리)
- **fuel_type:** The type of fuel the car uses (Petrol/Diesel). (연료 종류 (휘발유/디젤))

Example data: (예시 데이터:)

| name                                   | year | Price    | kms_driven  | fuel_type |
|----------------------------------------|------|----------|-------------|-----------|
| Hyundai Santro Xing XO eRLX Euro III   | 2007 | 80,000   | 45,000 kms  | Petrol    |
| Mahindra Jeep CL550 MDI                | 2006 | 4,25,000 | 40 kms      | Diesel    |
| Maruti Suzuki Alto 800 Vxi             | 2018 | Ask For Price | 22,000 kms | Petrol    |
| Hyundai Grand i10 Magna 1.2 Kappa VTVT | 2014 | 3,25,000 | 28,000 kms  | Petrol    |
| Ford EcoSport Titanium 1.5L TDCi       | 2014 | 5,75,000 | 36,000 kms  | Diesel    |

---

### Implementation Details (구현 세부 사항)

1. **FastAPI:** The backend API framework used to create the RESTful service. (백엔드 API 프레임워크)
2. **Streamlit:** The frontend framework used for user interaction and displaying results. (프론트엔드 프레임워크)
3. **Data Processing:**
   - **column_transformer:** Used for transforming categorical and numerical data. (범주형 및 수치 데이터 변환)
   - **pipeline:** A sequence of data transformation and model application steps. (데이터 변환 및 모델 적용 단계)
   - **joblib:** Used for saving and loading the trained model. (모델 저장 및 로드)

4. **Model Performance:** 
   - **R2 Score:** The model achieved an R2 score of 0.92, indicating good predictive performance. (모델의 R2 점수 0.92, 우수한 예측 성능)

---

### Application Flow (애플리케이션 흐름)

1. **User Input:** Users enter car features in the Streamlit interface. (사용자 입력: Streamlit에서 자동차 기능 입력)
2. **API Call:** The Streamlit app sends a request to the FastAPI endpoint with the entered features. (API 호출: FastAPI에 요청 전송)
3. **Prediction:** The FastAPI endpoint uses the trained model to predict the car price. (예측: 훈련된 모델로 가격 예측)
4. **Result Display:** The predicted price is displayed on the Streamlit interface. (결과 표시: 예측된 가격 표시)
![prediction_result](/streamlitcar.png)

