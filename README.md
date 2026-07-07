**Predict the fare amount of future rides using regression analysis**

This project provides a comprehensive analysis of historical trip and ride-sharing data, combining exploratory data analysis (EDA), data preprocessing, and machine learning to uncover insights and build predictive regression models. The goal is to understand the key factors influencing ride pricing—such as distance, time, and traffic—and develop a robust system to accurately predict the fare amount of future rides.

**Objectives**

1.	Identify key patterns and relationships in pricing data (e.g., peak hours, high-demand zones).

2.	Prepare the data for machine learning by handling missing values, filtering outliers, and engineering features like distance metrics.

3.	Build and compare multiple regression models to accurately estimate continuous target fares.

4.	Interpret model results to understand which variables (like peak hours or weekdays) heavily drive fare prices.


**Dataset**

The project is based on a structured dataset (uber.csv) with features such as:

1.	Trip distance, pickup and dropoff latitudes/longitudes, pickup datetimestamp

2.	Passenger count, Fare amount, distance_km, DayofWeek, Month, Hour & Year

**Exploratory Data Analysis**

Identified the outliers using box plot

Code:

<img width="419" height="218" alt="image" src="https://github.com/user-attachments/assets/8e26c682-5f62-4802-b022-8f98945f4c92" />

<img width="876" height="461" alt="image" src="https://github.com/user-attachments/assets/ad52263f-f342-400c-bc18-0080110dfec0" />

Identfying the correlation by means of using Heatmap

<img width="384" height="92" alt="image" src="https://github.com/user-attachments/assets/74f566c1-d56b-42c3-914f-960005682446" />

<img width="897" height="523" alt="image" src="https://github.com/user-attachments/assets/5a0a8ff5-f512-4304-9b88-4fca0d44bc92" />


**Model Implementation**:

<img width="256" height="98" alt="image" src="https://github.com/user-attachments/assets/bfd23ade-6571-4aaa-b882-3d6fb2d0c761" />

**Evaluating the model**:

<img width="577" height="346" alt="image" src="https://github.com/user-attachments/assets/91fd1f42-6aa3-4f5c-90f3-ac719b773e80" />

To improve the Train and test scores, implementing the Random Forest Regressor:

<img width="430" height="133" alt="image" src="https://github.com/user-attachments/assets/2947af37-9643-4d14-8948-645178338425" />

<img width="695" height="437" alt="image" src="https://github.com/user-attachments/assets/fb27f34a-9f20-4ac2-9440-b4c9f72a8932" />

<img width="475" height="368" alt="image" src="https://github.com/user-attachments/assets/4f4b3032-ff2a-41dd-85fb-06400e6a3f4a" />

<img width="548" height="125" alt="image" src="https://github.com/user-attachments/assets/08ff7e5c-a371-46b3-9be5-a091a7b78b57" />

**Drawing the Inference**:

By utilising the RandomForestReg the Train score has been drastically reduced with a slight increase in Test score

Overfitting is minimized using RandomizeSearchCV.

**Executive Summary**

The objective of this analysis was to evaluate two machine learning models—Linear Regression (LR) and Random Forest (RF)—to predict Uber fare amounts based on GPS coordinates, time of day, and trip distance. After testing across various time-frames (4 AM, 2 PM, 6 PM, and 9 PM), the Random Forest Regressor is the recommended model for deployment due to its superior ability to handle non-linear temporal patterns and realistic price scaling.

<img width="407" height="242" alt="image" src="https://github.com/user-attachments/assets/4ad66c4c-4121-4c58-b6f6-3ec10b82b282" />

**Insights & Outcomes**

Clear visualization of feature importance

It confirms that "**distance**" is the primary engine of regression model

**Conclusion**

Comparatively the Non-Linear Regression (RandomForest) utilises the decision-tree buckets to treat each hour as specific context whereas the Linear Regression predicts that prices always decrease as the hour increases, assuming the time is being continuous in nature. 
Henceforth the RandomForest would be recommended for realistic price scaling.








