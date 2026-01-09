THE UNPROCESSED DATASET FEATURING THE ON TIME AIRLINE PERFORMANCE REPORT IS OBTAINED FROM BTS USA CAN BE DOWNLOADED AT THE FOLLOWING LINK:- https://transtats.bts.gov/PREZIP/On_Time_Reporting_Carrier_On_Time_Performance_1987_present_2025_1.zip

After thorough analysis of the dataset, all "useless data" was removed. So were irrelevant and redundant columns.
The reasons for the same are as follows:
1. There were leakage variables present that doesn't let the machine learning algorithms learn properly and might have led to memorisation of flights that caused delays and flag accordingly.
2. Flights might have to undergo diversions from the primary airport where it was supposed to land due to multiple reasons including extreme airport congestion, poor weather conditions at destination airport, etc. There were 5 such "Div" columns each of which were 99% empty. Similarly, upon checking how much percentage of missing values were missing from each column, if it had more than 90-95% missing, we would remove the column becuase imputation in such scenarios harm the originality of the data. The number of columns reduced significantly.
3. All "Post Departure" variables were removed since the model only knows of already occured flights and tries to learn from the 8 primary variables selected for the same.

The file "jan_2025_sanitized.csv" at the link: https://github.com/pmandalegend1/Flight_delay_prediction_without_over-relying_on_meteorological_data/blob/main/jan_2025_sanitized.csv  is the file after pre-processing and the one that has been used for predictions.
The dataset was pre-processed, anaylized and visualized, aaccording to the MLDLC steps in order. 

The file: https://github.com/pmandalegend1/Flight_delay_prediction_without_over-relying_on_meteorological_data/blob/main/Jan_2025_data_cleaning_and_pre-processing_with_analysis.ipynb is the notebook where preprocessing and analysis was conducted.

Research Project Name:-  Flight_delay_prediction_without_over-relying_on_meteorological_data

I aim to bring in a paradigm shift by prioritizing systemic human factors over meteorological determinism.
Research in plenty of papers rely heaviily to a certain extent on "weather" or "meteorological variables" consideration / integration for predicting flight delays. When pondered upon, one can easily realise how if a flight is ready to fly at the scheduled time only certainly depends on the duration (+ or -) 5 minutes of takeoff. But reports from reputable organisations like McKinsey & Company and IATA, in their reports, clearly reveal how weather was found to be the least affecting factor in a flights delay. The actual delay arises from Previous Departure delays and inefficient management / insufficient buffer time in between 2 flights for a flight with the same tail number. Focusing more on predicting the non- weather variables leading to delays helps in revealing the systemic chain of delays and underlying causes. 

While atmospheric conditions offer a convenient, visible scapegoat for schedule disruptions, this research asserts that the core of predictive accuracy lies in the deconvolution of human-centric and systemic operational variables. Despite the apparent simplicity of weather-based forecasting, the true frontier of aviation resilience is the deep analysis of the interconnected human elements within the operational chain—ranging from ground-handling logistics to labour-force synchronization.

The discrepancy between current industry standards and the world’s most punctual carriers suggests that high-tier On-Time Performance (OTP) is not a result of favourable weather, but of superior modelling of internal delay catalysts. Had the industry historically prioritized the modelling of high-contribution systemic features over exogenous weather data, operational efficiency would be significantly more robust. The model proposed in this study deliberately pivots away from these transient environmental factors to capture the latent, high-impact features of the operational ecosystem. By isolating and analysing the non-weather drivers that dictate the majority of delay variances, this framework provides a high-fidelity diagnostic tool for the issues that genuinely govern airline performance.

This is the Version 2 of the project with 2 removed features and a better performance in terms of roc auc and brier scores indicating better research and moe accurate delay prediction focusing on all the non - meteorological factors involved.

Version 1 will be uploaded only after work progresses in Version 2.
