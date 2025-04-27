# Fraud_Detection
ეს პროექტი ეხებოდა თაღლითობის ამოცნობას მანქანული სწავლების ფაიფლაინების გამოყენებით. გამოვიყენე 4 სხვადასხვა მოდელი:
1. XGBoost (experiment_xg)
2. adaBoost (experiment_ada)
3. Logistic Regression (experiment_log)
4. Random Forest (experiment_rand_forest)
მათ შორის ყველაზე კარგი შედეგი - 0.938 - დადო XGBoost-მა, model_inference-ში გამოვიყენე ეს მოდელი

მონაცემების დამუშავება:
1. ამოვშალე სვეტები ზედმეტი ფარდობითი რაოდენობის null მნიშვნელობებით.
2. ამოვშალე მაღალი კორელაციის მქონე თვისებები.
3. კატეგორიული ცვლადების თავიდან მოსაშრებლად გამოვიყენე WOEEncoding, OneHotEncoding.
4. გამოვიყენე ყოველი მოდელისთვის ერთ შემთხვევაში მაინც StandardScaler.
5. model_inference ფაილში, ტესტების მონაცემებში არსებული ხარვეზის გამო (ტესტების სვეტების სახელების ნაწილი განსხვავდებოდა ტრეინის სვეტების სახელებისგან) ტრეინის მონაცემების სტილს მოვარგე სვეტების სახელები.

საუკეთესო მოდელი აღმოჩნდა XGBoost standardScaler-ის გამოყენებით - 0.9380098243599908 - ამ მოდელმა ძალიან მცირე განსხვავება მომცა ტრეინ და ტესტ მონაცემებს შორის, დაახლოებით 0.01.
https://dagshub.com/electrolizzys/Fraud_Detection.mlflow/#/experiments/0?searchFilter=&orderByKey=attributes.start_time&orderByAsc=false&startTime=ALL&lifecycleFilter=Active&modelVersionFilter=All+Runs&datasetsFilter=W10%3D

https://dagshub.com/electrolizzys/Fraud_Detection.mlflow/#/models/XGBoost_final
