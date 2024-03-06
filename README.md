# Home Credit Default Risk Prediction

## Dataset Description
The dataset `train.csv` contains information about loans, sourced from Kaggle: [Home Credit Default Risk](https://www.kaggle.com/c/home-credit-default-risk).

Each record corresponds to a specific dossier, uniquely identified by the ID variable. The TARGET variable represents the payment performance with values:
- 1: Customer with difficulties in repaying debt
- 0: Otherwise

The goal is to build a model predicting payment performance for the next loan requests based on various predictors.

## Predictors

### Socio-demo Info
- GENDER/ NAME_FAMILY_STATUS/ CNT_CHILDREN/ CNT_FAM_MEMBERS: Client's gender / family status / number of children / number of family members
- OCCUPATION_TYPE/ ORGANIZATION_TYPE: Client's occupation and employer's organization type
- DAYS_AGE: Client's age in days at the time of application
- DAYS_EMPLOYMENT: Days before the application the person started their current employment
- DAYS_ID_PUBLISH: Days before the application client changed identity document
- NAME_EDUCATION_TYPE: Level of the highest education the client achieved
- FLAG_PHONE/ FLAG_MOBIL/ FLAG_WORK_PHONE/ FLAG_EMP_PHONE: If client provided home / mobile / work / employer's phones
- FLAG_CONT_MOBILE: Was the mobile phone reachable
- FLAG_EMAIL: Did client provide an email
- REG_REGION_NOT_LIVE_REGION/ REG_REGION_NOT_WORK_REGION/ LIVE_REGION_NOT_WORK_REGION/ REG_CITY_NOT_LIVE_CITY/ REG_CITY_NOT_WORK_CITY/ LIVE_CITY_NOT_WORK_CITY: Various region and city-related flags

### Income Info
- NAME_HOUSING_TYPE: Housing situation of the client (renting, living with parents, etc.)
- AMT_INCOME_TOTAL and NAME_INCOME_TYPE: Income of the client and client's income type
- FLAG_OWN_CAR (OWN_CAR_AGE) and FLAG_OWN_REALTY: Flag if the client owns a car (and its age) or a house (flat)

### Behavioral Info
- NAME_TYPE_SUITE: Who was accompanying the client when applying for the loan
- WEEKDAY_APPR_PROCESS_START / HOUR_APPR_PROCESS_START: Day of the week / hour the client applied for the loan

### Residence Info
The various _TAG suffixes correspond to the average (_AVG), modus (_MODE), and median (_MEDI) of:
- APARTMENTS_TAG: Apartments size
- YEARS_BUILD_TAG: Age of buildings
- ELEVATORS_TAG: Number of elevators
- ENTRANCES_TAG: Number of entrances
- FLOORSMIN_TAG / FLOORSMAX_TAG: Number of floors
- HOUSETYPE_MODE: House type
- TOTAL_AREA_MODE: Total area
- WALLSMATERIAL_MODE: Walls material
- REGION_RATING_CLIENT / REGION_RATING_CLIENT_W_CITY: Home Credit's rating of the region where the client lives / accounting for the city

### Loan Info
- AMT_CREDIT: Amount of the loan
- AMT_ANNUITY: Loan annuity
- NAME_CONTRACT_TYPE: Indicates if the loan is cash or revolving
- AMT_GOODS_PRICE: For consumer loans, it is the price of the goods for which the loan is given

### Bureau Scores
- EXT_SOURCE_1 / EXT_SOURCE_2 / EXT_SOURCE_3 / EXT_SOURCE_4: Normalized scores from an external data source
- AMT_REQ_CREDIT_BUREAU_tag: Number of enquiries to Credit Bureau about the client one hour (day, week, etc.) before application
- OBS_30_CNT_SOCIAL_CIRCLE / DEF_30_CNT_SOCIAL_CIRCLE: Number of observations of the client's social surroundings observed 30 days past due and how many defaulted
- OBS_60_CNT_SOCIAL_CIRCLE / DEF_60_CNT_SOCIAL_CIRCLE: Number of observations of the client's social surroundings observed 60 days past due and how many defaulted

## Tools and Libraries Used
- `numpy`, `pandas`, `seaborn`, `matplotlib`, `scikit-learn`, `imblearn`
