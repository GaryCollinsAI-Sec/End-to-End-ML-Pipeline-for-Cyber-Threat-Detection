<h1>End-to-End ML Pipeline for Cyber Threat Detection</h1>

<h2>Objective</h2>
<p>
This project builds a machine learning–based Network Intrusion Detection System (NIDS) using the NSL-KDD dataset.
</p>

<p>
The pipeline processes raw network traffic data, applies preprocessing and feature engineering, and trains a Random Forest classifier to detect malicious activity (Normal vs. Attack).
</p>

<hr>

<h2>Skills Developed</h2>
<ul>
  <li>Trained and evaluated a Random Forest classifier on a high-dimensional security dataset</li>
  <li>Built preprocessing pipelines for mixed categorical and numerical features</li>
  <li>Applied label encoding and feature scaling</li>
  <li>Interpreted confusion matrix, precision, recall, and F1-score</li>
  <li>Analyzed feature importance to understand model behavior</li>
  <li>Debugged datatype and column-selection errors using dynamic feature handling</li>
</ul>

<hr>

<h2>Tools</h2>
<ul>
  <li><strong>Python</strong></li>
  <li><strong>Pandas</strong></li>
  <li><strong>NumPy</strong></li>
  <li><strong>Scikit-learn</strong></li>
  <li><strong>Matplotlib</strong></li>
  <li><strong>Seaborn</strong></li>
  <li><strong>Jupyter Notebook</strong></li>
  <li><strong>VS Code</strong></li>
</ul>

<hr>

<h2>Implementation Overview</h2>

<h3>Ref 1 – Dataset Loading & Inspection</h3>
<p>
Loaded the NSL-KDD dataset:
</p>
<ul>
  <li>Training set: 125,973 records</li>
  <li>Test set: 22,544 records</li>
  <li>42 features (categorical and numerical)</li>
</ul>

<p>
Initial inspection confirmed feature types and dataset structure before preprocessing.
</p>

<img width="830" height="264" src="https://github.com/user-attachments/assets/762ee818-bb60-40a5-8999-62ec06e3b992" />

<br><br>

<h3>Ref 2 – Data Validation</h3>
<p>
Validated dataset integrity:
</p>
<ul>
  <li>Checked for missing values (none found)</li>
  <li>Confirmed final training and test shapes</li>
  <li>Verified feature consistency</li>
</ul>

<img width="323" height="575" src="https://github.com/user-attachments/assets/276dd730-8365-46ce-bb4e-d21fbbe5c570" />

<br><br>

<h3>Ref 3 – Model Evaluation</h3>
<p>
Evaluated model performance using:
</p>
<ul>
  <li>Confusion Matrix</li>
  <li>Precision, Recall, and F1-score</li>
  <li>Feature Importance analysis</li>
</ul>

<p>
The model achieved high accuracy on this benchmark dataset and correctly classified attack traffic.
</p>

<img width="233" height="180" src="https://github.com/user-attachments/assets/193b3b62-cb5f-4e38-ac6f-bca700feb5c7" />

<br><br>

<h3>Ref 4 – Preprocessing Pipeline</h3>
<p>
Preprocessing steps included:
</p>
<ul>
  <li>Label Encoding for categorical variables (protocol_type, service, flag)</li>
  <li>Standard Scaling for numerical traffic metrics</li>
</ul>

<p>
These steps allowed the model to process mixed feature types effectively.
</p>

<img width="242" height="76" src="https://github.com/user-attachments/assets/35f3ad6e-a1e0-4b25-9493-770ada6118bc" />

<br><br>

<h3>Ref 5 – Classification Metrics</h3>
<p>
Generated a classification report including:
</p>
<ul>
  <li>Accuracy</li>
  <li>Precision</li>
  <li>Recall</li>
  <li>F1-score</li>
</ul>

<p>
The model achieved near-perfect performance on this dataset.
</p>

<img width="451" height="345" src="https://github.com/user-attachments/assets/475d8290-40c9-4609-b39e-d65641161594" />

<br><br>

<h3>Ref 6 – Attack Type Distribution</h3>
<p>
Visualized the distribution of attack types to understand dataset imbalance and class representation.
</p>

<img width="868" height="479" src="https://github.com/user-attachments/assets/160b26cf-ea4f-4ff0-9cd9-0ad2d9a2d1bb" />

<br><br>

<h3>Ref 7 – Binary Label Distribution</h3>
<p>
Confirmed the volume of attack vs. normal traffic prior to model training.
</p>

<img width="566" height="393" src="https://github.com/user-attachments/assets/565aa724-d2d2-4127-9c85-8577da559df2" />

<hr>

<h2>Note</h2>
<p>
NSL-KDD is a benchmark dataset and does not fully represent real-world production traffic. 
Additional validation would be required before deploying a similar model in live network environments.
</p>
