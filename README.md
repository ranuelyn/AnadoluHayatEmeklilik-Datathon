# Anadolu Hayat Emeklilik Datathon
Anadolu Hayat Emeklilik Datathon 2024

Anadolu Hayat Emeklilik, a pioneer in Individual Retirement and Life Insurance, is hosting its second Datathon. This event challenges you to develop the best predictive methods for real-world problems using real data, showcasing your data science skills.

# Evaluation

The competition's success metric will be the weighted F1 Score. The top 10 participants on the Private Leaderboard will be invited to present their work in the final presentation to the jury on April 4, 2024, if their notebooks are positively evaluated by Anadolu Hayat Emeklilik and Coderspace.

# Dataset Description

The dataset provides detailed features about customers' retirement and insurance policies:

Dataset Description
MUSTERI_ID : Müşterileri ayırt eden unique ID'ler.
LABEL: Müşterinin aldığı Hayat sigortası ürününün çeşidi.
FLAG:Verinin ait olduğu ay.
PP_CINSIYET: Sözleşme sahibinin cinsiyeti.
1: Erkek
2: Kadın
PP_YAS : Sözleşme sahibinin ay bazlı olarak yaşı.
PP_MESLEK : Sözleşme sahibinin mesleği.
PP_MUSTERI_SEGMENTI : Sözleşme sahibinin müşteri segmenti.
101: A segment
102: B segment
103: C segment
104: D segment
105: E segment
106: F segment
PP_UYRUK: Sözleşme sahibinin uyruk bilgisi.
1:TC Vatandaşı
2:Mavi Kart
3:Yabancı Uyruklu
IL:Sözleşme sahiplerinin yaşadığı illere ait plaka kodu.( 0 = Yurtdışı)
SORU_YATIRIM_KARAKTERI_CVP: Sözleşme sahibinin ankete verdiği cevaplara göre belirlenen yatırım karakteri.
SORU_YATIRIM_KARAKTERI_RG: Sözleşme sahibinin ankette verdiği cevabın üstünden geçen süre (ay).
SORU_MEDENI_HAL_CVP: Sözleşme sahibinin ankete verdiği cevaba göre medeni durumu.
SORU_MEDENI_HAL_RG: Sözleşme sahibinin ankette verdiği cevabın üstünden geçen süre (ay).
SORU_EGITIM_CVP: Sözleşme sahibinin ankete verdiği cevaplara göre eğitim durumu.
SORU_EGITIM_RG: Sözleşme sahibinin ankette verdiği cevabın üstünden geçen süre (ay).
SORU_GELIR_CVP: Sözleşme sahibinin ankete verdiği cevaba göre gelir durumu.
SORU_GELIR_RG: Sözleşme sahibinin ankette verdiği cevabın üstünden geçen süre (ay).
SORU_COCUK_SAYISI_CVP: Sözleşme sahibinin ankete verdiği cevaba göre çocuk sayısı.
SORU_COCUK_SAYISI_RG: Sözleşme sahibinin ankette verdiği cevabın üstünden geçen süre (ay).
BES_AYRILMA_TALEP_ADET : Sözleşme sahibinin BES hesabından ayrılmak için açtığı talep sayısı.
ODEMEME_TALEP_ADET : Sözleşme sahibinin son 1 sene içerisinde kaç kez ödememe talimatı verdiğini gösterir.
HAYAT_AYRILMA_TALEP_ADET : Sözleşme sahibinin Hayat sigortasından ayrılmak için açtığı talep sayısı.
BILGI_TALEP_ADET : Sözleşme sahibinin sözleşmesi için kaç kez bilgi talep ettiğini gösterir.
VADE_TUTAR_0 - VADE_TUTAR_11 : Sözleşme sahibinin sahip olduğu ürünlerin son 12 aya ait toplam vade tutarları
ODEME_TUTAR_0 - ODEME_TUTAR_11 : Sözleşme sahibinin sahip olduğu ürünler için son 12 ayda yaptığı ödeme tutarları
SON_AY_KATKI_MIKTARI : Sözleşme sahibinin son bir ay içinde yaptığı ek katkı ödemelerinin TL cinsinden toplam miktarı
SON_AY_KATKI_ADET : Sözleşme sahibinin son bir ay içinde yaptığı ek katkı ödemelerinin adedi
SON_CEYREK_KATKI_MIKTARI : Sözleşme sahibinin son üç ay içinde yaptığı ek katkı ödemelerinin TL cinsinden toplam miktarı
SON_CEYREK_KATKI_ADET : Sözleşme sahibinin son üç ay içinde yaptığı ek katkı ödemelerinin adedi
SON_SENE_KATKI_MIKTARI : Sözleşme sahibinin son bir sene içinde yaptığı ek katkı ödemelerinin TL cinsinden toplam miktarı
SON_SENE_KATKI_ADET : Sözleşme sahibinin son bir sene içinde yaptığı ek katkı ödemelerinin adedi
ANAPARA: Sözleşme sahibinin TL cinsinden toplam yatırdığı para miktarı.
GETIRI : Sözleşme sahibinin TL cinsinden yatirdiği paradan elde ettiği getiri.
BU1 - BU24: BES ÜRÜN 1 - 24, Kişinin kolonda belirtilen BES ürününe sahip olup olmama durumu (Ürün özellikleri ayrı bir dokumanda verilmiştir)
HU1 - HU19: HAYAT ÜRÜN 1 - 19, Kişinin kolonda belirtilen Hayat ürününe sahip olup olmama durumu (Ürün özellikleri ayrı bir dokumanda verilmiştir)
AKTIF_ILK_POLICE_RG: Sözleşme sahibinin aktif olan poliçeleri arasından en eskisinin üstünden geçen süre (ay).

Custom Metric Katsayıları:

+----+-------+
|ÜRÜN|KATSAYI|
+----+-------+
|HU06|0.0385 |
|HU07|0.0328 |
|HU11|0.2791 |
|HU12|0.1812 |
|HU14|0.0113 |
|HU15|0.2952 |
|HU19|0.1614 |
| UA |0.0001 |
+----+-------+


# Solution Approach and Models

Our strategy for tackling the challenges presented by the Anadolu Hayat Emeklilik Datathon 2024 was comprehensive, employing advanced machine learning techniques to predict customer preferences for retirement and life insurance products accurately. Below is an overview of our approach and the sophisticated models we utilized:

Data Preprocessing
We began with meticulous data cleaning and preparation, which is crucial for the success of any data science project. This included:

Handling Missing Data: Techniques were applied to manage missing values without compromising the integrity of the dataset.
Feature Engineering: We derived new features from the existing dataset to better capture the nuances of customer behavior and preferences, enhancing our models' predictive capabilities.
Exploratory Data Analysis (EDA)
An extensive EDA phase allowed us to gain deep insights into the dataset, uncovering patterns and relationships that would inform our modeling decisions. This step was critical for identifying key features and understanding the target variable distribution across different segments.

Models Employed
Unlike traditional approaches, we focused on leveraging state-of-the-art machine learning models known for their effectiveness in classification tasks and handling complex datasets.

XGBoost

XGBoost stands out for its performance and speed. We tuned various hyperparameters to optimize its performance for our specific dataset, aiming to maximize the weighted F1 Score, which is crucial for addressing the class imbalance present in our dataset.

CatBoost

CatBoost was selected for its ability to handle categorical data effortlessly, providing a significant advantage given the nature of our dataset. Its advanced algorithms for dealing with categorical variables allowed us to bypass extensive preprocessing steps, directly impacting our model's efficiency and effectiveness.

LightGBM

LightGBM was another cornerstone of our approach, known for its speed and efficiency at scale. This model was particularly useful in iterating quickly through model versions and exploring different feature sets.

# Evaluation and Custom Metrics
Our evaluation was primarily based on the Weighted F1 Score, ensuring a balanced approach to precision and recall across our imbalanced dataset. Additionally, we developed custom metrics to align closely with Anadolu Hayat Emeklilik's business objectives, focusing on product-specific importance as indicated by their provided coefficients.

# Optimization and Hyperparameter Tuning
Significant efforts were made in optimizing our models and fine-tuning hyperparameters to enhance performance. Techniques such as cross-validation and grid search were employed to find the optimal settings for each model.

# Conclusion
The use of advanced machine learning models like XGBoost, CatBoost, and LightGBM enabled us to achieve significant predictive performance. Our approach not only highlighted the potential of these models in handling complex, real-world datasets but also underscored the importance of a rigorous, data-driven methodology in solving business challenges.

# Contributing

Your contributions can help further improve the project. We encourage you to share your ideas, enhancements, or improvements by forking this repository and submitting pull requests. For discussions or suggestions, please open an issue in the repository.
