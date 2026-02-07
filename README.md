# End-to-End ML Pipeline for Cyber Threat Detection


## Objective


This project implements a robust Machine Learning-based Network Intrusion Detection System (NIDS) using the NSL-KDD dataset. The pipeline automates the journey from raw network traffic data to actionable security insights, achieving high-accuracy binary classification (Normal vs. Attack).

### Skills Learned


- Supervised Machine Learning: You gained hands-on experience with the Random Forest algorithm, understanding how to train, test, and evaluate an ensemble model on a high-dimensional security dataset.
- Model Evaluation & Analytics: You learned to interpret a Confusion Matrix and Feature Importance plots to verify if a model is truly learning or simply overfitting.
- Cybersecurity Domain Knowledge: You worked with the NSL-KDD benchmark, giving you insight into how network features (like src_bytes and service_flags) correlate with malicious activity.
- Feature Engineering & Data Preprocessing: You learned how to handle a mix of categorical and numerical data by implementing Label Encoding for strings (like protocol types) and Standard Scaling for traffic metrics.
- Defensive Programming in Python: You mastered techniques to resolve complex ValueErrors by using dynamic column selection (select_dtypes), ensuring your code doesn't crash when encountering unexpected data types.

### Tools Used


- Development Environment: VS Code (Integrated Development Environment) and Jupyter Notebooks (Interactive prototyping and documentation).
- Data Manipulation: Pandas (DataFrame management) and NumPy (Numerical operations and array handling).
- Machine Learning: Scikit-learn (Implementation of Random Forest, Label Encoding, Feature Scaling, and Evaluation Metrics).
- Visualization: Matplotlib and Seaborn (Generating Confusion Matrices and Feature Importance plots).




*Ref 1: ML pipeline*

<img width="830" height="264" alt="Screenshot 2026-02-06 202448" src="https://github.com/user-attachments/assets/762ee818-bb60-40a5-8999-62ec06e3b992" />


The initial stage of this project involved loading and inspecting the NSL-KDD dataset, a benchmark for network intrusion detection. The training set contains 125,973 records, while the test set comprises 22,544 records, each structured with 42 features ranging from connection duration to protocol types like TCP and UDP. This high-dimensional data includes both numerical metrics (source bytes) and categorical variables (e.g., service flags), necessitating a comprehensive preprocessing pipeline—including Label Encoding and Standard Scaling—to prepare the raw network traffic for classification by the machine learning model.




*Ref 2: ML pipeline*

<img width="323" height="575" alt="Screenshot 2026-02-06 202523" src="https://github.com/user-attachments/assets/276dd730-8365-46ce-bb4e-d21fbbe5c570" />



The project began with a rigorous audit of the dataset to ensure a clean foundation for the machine learning model. Initial inspection revealed a training set of 125,973 records and a test set of 22,544 records, both containing 42 distinct features. A comprehensive check for missing values across key network metrics—such as duration, protocol_type, service, and src_bytes—returned a count of zero missing entries for all columns. Following this validation, the final data shape was confirmed at 125,973 rows for training and 22,544 for testing, providing a robust and complete dataset for subsequent preprocessing and model training.




*Ref 3: ML pipeline*

<img width="233" height="180" alt="Screenshot 2026-02-06 202537" src="https://github.com/user-attachments/assets/193b3b62-cb5f-4e38-ac6f-bca700feb5c7" />


the pipeline focuses on assessing the model's effectiveness in identifying malicious traffic. By generating a Confusion Matrix, the system provides a granular breakdown of True Positives and Negatives, allowing for a clear visualization of detection accuracy versus false alarms. Additionally, the Feature Importance analysis ranks the impact of each network attribute, revealing which specific behaviors—such as connection duration or data volume—the model identifies as the primary indicators of an attack. This dual-insight approach not only validates the model’s 99%+ accuracy but also provides actionable intelligence for security analysts to understand the underlying nature of detected threats.





*Ref 4: ML pipeline*

<img width="242" height="76" alt="Screenshot 2026-02-06 202723" src="https://github.com/user-attachments/assets/35f3ad6e-a1e0-4b25-9493-770ada6118bc" />



The Preprocessing phase is the engine of the pipeline, where raw, unstructured network logs are meticulously transformed into a clean format that machine learning algorithms can interpret. By implementing Label Encoding to convert categorical strings (like protocol and service types) into numerical identifiers and applying Standard Scaling to normalize high-variance traffic metrics (like byte counts), the system eliminates mathematical bias and ensures the model can identify subtle malicious patterns across diverse features. This critical stage not only optimizes the Random Forest’s training speed but also directly enhances the system's ability to distinguish between legitimate user activity and complex, multi-stage cyber threats.



*Ref 5: ML pipeline*

<img width="451" height="345" alt="Screenshot 2026-02-06 202751" src="https://github.com/user-attachments/assets/475d8290-40c9-4609-b39e-d65641161594" />


In this Model Evaluation phase, the system's predictive performance is quantified through a detailed classification report and core accuracy metrics. The output reveals that the model achieved an Accuracy, Precision, Recall, and F1-score of 1.0000, indicating a perfect classification of the test dataset. The classification report further validates these results, showing a support count of 22,544 instances for the "attack" class, all of which were correctly identified. This high level of precision demonstrates the model's exceptional ability to distinguish malicious traffic patterns from normal activity within this specific dataset.


*Ref 6: ML pipeline*

<img width="868" height="479" alt="output" src="https://github.com/user-attachments/assets/160b26cf-ea4f-4ff0-9cd9-0ad2d9a2d1bb" />




This screenshot illustrates the Distribution of Attack Types within the training dataset through a categorical bar chart. By visualizing the "Top 10 Attack Types," the project provides a clear look at the class imbalance and specific threat profiles present in the NSL-KDD dataset, where certain labels (such as '21') show a significantly higher frequency exceeding 60,000 samples—compared to others. This exploratory data visualization is crucial for understanding the diversity of the training data, as it ensures the model is exposed to a wide range of malicious behaviors before moving into the final classification phase.





*Ref 7: ML pipeline*


<img width="566" height="393" alt="output-binary-label" src="https://github.com/user-attachments/assets/565aa724-d2d2-4127-9c85-8577da559df2" />


This final visualization provides a high-level summary of the dataset's target variable through a Binary Label Distribution bar chart. It illustrates the total volume of network traffic analyzed in the training set, specifically highlighting the "attack" class which comprises over 120,000 samples. By confirming the presence of these malicious records, the chart demonstrates that the model has been trained on a substantial volume of threat data, ensuring it is well-equipped to recognize the patterns of network intrusions during the classification phase.





