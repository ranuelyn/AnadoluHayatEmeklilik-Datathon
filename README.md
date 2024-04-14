# Anadolu Hayat Emeklilik Datathon 2024

Welcome to the official repository for the Anadolu Hayat Emeklilik Datathon 2024, an initiative by Anadolu Hayat Emeklilik to harness the predictive prowess of data science in real-world scenarios. This repository documents the methodologies and models developed throughout the competition.

**Disclaimer**: Data sharing is restricted due to the competition's confidentiality agreement.

## Evaluation Criteria

Participants are evaluated based on the weighted F1 Score. Finalists are those ranking in the top 10 on the Private Leaderboard, contingent on a positive evaluation of their notebooks by Anadolu Hayat Emeklilik and Coderspace. Final presentations to the jury are scheduled for April 4, 2024.

## Dataset Description

Participants were provided with a dataset containing comprehensive information about the customers' retirement and insurance policies. The features include:

- `MUSTERI_ID`: Unique identifier for customers.
- `LABEL`: Type of Life Insurance product purchased by the customer.
- `FLAG`: Month to which the data belongs.
- `PP_CINSIYET`: Gender of the policyholder (1: Male, 2: Female).
- `PP_YAS`: Age of the policyholder on a monthly basis.
- `PP_MESLEK`: Profession of the policyholder.
- `PP_MUSTERI_SEGMENTI`: Customer segment of the policyholder (101: A segment, 102: B segment, etc.).
- `PP_UYRUK`: Nationality of the policyholder (1: Turkish Citizen, 2: Blue Card, 3: Foreign National).
- `IL`: Province code where the policyholder resides (0 for abroad).
- ... and many more detailed features regarding the policyholders' profiles, investment characteristics, marital status, education, income level, number of children, and their interactions with the retirement system and life insurance policies.

## Custom Metric Coefficients

The competition introduces custom coefficients for the metric calculation, emphasizing the importance of certain products:

| Product | Coefficient |
|---------|-------------|
| HU06    | 0.0385      |
| HU07    | 0.0328      |
| ...     | ...         |
| HU19    | 0.1614      |
| UA      | 0.0001      |


## Dataset Synopsis

The dataset encompasses extensive features related to customers' retirement and insurance policies, such as demographics, policy details, and customer interactions. Due to confidentiality, we can't provide the dataset but can share insights into its structure and the type of information it includes.

## Solution Approach

Our analytical strategy is built on a multi-layered machine learning framework, aiming to accurately predict customer preferences for insurance products. We have employed several sophisticated models to achieve this:

### Data Preprocessing
- **Missing Data**: Implemented strategies to address missing values while preserving data integrity.
- **Feature Engineering**: Enhanced the dataset with newly derived features to encapsulate customer behavior effectively.

### Exploratory Data Analysis (EDA)
- Conducted a thorough EDA to identify pivotal patterns and relationships, informing our subsequent modeling efforts.

### Models Deployed
- **XGBoost**: Optimized for performance with careful hyperparameter tuning to address the dataset's class imbalance.
- **CatBoost**: Chosen for its superior handling of categorical variables, streamlining our modeling process.
- **LightGBM**: Utilized for its quick processing and model iteration capabilities, facilitating rapid experimentation.

## Evaluation and Custom Metrics
Our primary evaluation metric, the Weighted F1 Score, reflects a comprehensive measure of model precision and recall. We also introduced custom metrics tailored to the specific products and business goals of Anadolu Hayat Emeklilik, guided by their coefficient framework.

## Optimization and Hyperparameter Tuning
We engaged in extensive model optimization and hyperparameter adjustments, utilizing techniques like cross-validation and grid search to refine our models to their utmost potential.

## Conclusion
The application of cutting-edge models such as XGBoost, CatBoost, and LightGBM has resulted in notable predictive accuracy. Our methodology demonstrates the impact of a structured and data-centric approach in tackling complex business challenges.

## Contributing
We invite the community to contribute to the continual improvement of this project. To propose enhancements:

1. Fork this repository.
2. Create your feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a pull request.

For any discussions or suggestions, please initiate an issue in the repository.

We are excited to see your innovative approaches and contributions to this project!
