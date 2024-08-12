# Analysing Healthcare Dataset using SQL

- SELECT COUNT(*) FROM Healthcare;
  <img width="110" alt="Count" src="https://github.com/ShivamNIT/Data-Analysis-SQL/assets/97026504/c3c94835-2f4a-4616-8994-5d4c206a9629">

- select max(age) as Maximum_Age from Healthcare;
<img width="119" alt="Maximum_Age" src="https://github.com/ShivamNIT/Data-Analysis-SQL/assets/97026504/73edeeb6-9f5c-4b09-af9b-e98780974a51">

- Select round(avg(age),0) as Average_Age from Healthcare;
<img width="119" alt="Avg_Age" src="https://github.com/ShivamNIT/Data-Analysis-SQL/assets/97026504/89e7229e-f216-4347-bec4-2ca21b81d2f1">

- SELECT AGE, COUNT(AGE) AS Total
FROM Healthcare
GROUP BY age
ORDER BY AGE DESC;
<img width="379" alt="image" src="https://github.com/ShivamNIT/Data-Analysis-SQL/assets/97026504/a95500f9-a680-4fc6-936d-73fdd450bcbb">

- SELECT AGE, COUNT(AGE) AS Total
FROM Healthcare
GROUP BY age
ORDER BY Total DESC,age DESC;
<img width="389" alt="Age_Count2" src="https://github.com/ShivamNIT/Data-Analysis-SQL/assets/97026504/a46302ab-b1ba-4296-b2df-a26c81fded7a">

- SELECT AGE, COUNT(AGE) As Total, dense_RANK() OVER(ORDER BY COUNT(AGE) DESC, age DESC) as Ranking_Admitted 
FROM Healthcare
GROUP BY age
HAVING Total > Avg(age);
<img width="564" alt="Ranking" src="https://github.com/ShivamNIT/Data-Analysis-SQL/assets/97026504/0bcfd2c5-808d-4f5f-9aca-2df5b0c0cf1c">

- SELECT Insurance_Provider, COUNT(Insurance_Provider) AS Total 
FROM Healthcare
GROUP BY Insurance_Provider
ORDER BY Total DESC;
<img width="164" alt="image" src="https://github.com/ShivamNIT/Data-Analysis-SQL/assets/97026504/c5deb274-7a68-4499-8014-457ef0cd06bc">

- SELECT Hospital, COUNT(hospital) AS Total 
FROM Healthcare
GROUP BY Hospital
ORDER BY Total DESC;
<img width="617" alt="image" src="https://github.com/ShivamNIT/Data-Analysis-SQL/assets/97026504/af77bfc7-2529-4be7-a7d8-915815b0a957">

- SELECT Medical, ROUND(AVG(BillingAmount),2) AS Avg_Billing_Amount
FROM Healthcare
GROUP BY Medical;
<img width="281" alt="image" src="https://github.com/ShivamNIT/Data-Analysis-SQL/assets/97026504/8a8b535f-e928-4889-bbee-b56134ea15b2">

- SELECT Name, Medical, ROUND(BillingAmount,2) as BillingAmount, Hospital, DATEDIFF(DischargeDate, AdmissionDate) as Total_Hospitalized_days
FROM Healthcare;
 <img width="578" alt="image" src="https://github.com/ShivamNIT/Data-Analysis-SQL/assets/97026504/a28e3e75-a911-459f-b404-02bf96000842">




- This dataset is taken from Kaggle (https://www.kaggle.com/datasets/prasad22/healthcare-dataset).

















