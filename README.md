# TikTok-Claims-Regression-Model.

<h3>Overview</h3>

Context: Building an ML model to classify videos as claims or opinions to reduce report backlogs.

Objective: Analyzing how video characteristics relate to an author's verification status at the request of Operations Lead Maika Abadi.

Methodology: Utilized a baseline Logistic Regression model to predict verification status and discover key feature trends.

<h3>project statues</h3>  

EDA & Cleaning: Capped engagement outliers and addressed a severe $93.7% class imbalance using a 50/50 upsampling technique.

Feature Engineering: Created a text_length character counter and dropped video_like_count to avoid severe multicollinearity due to its strong 0.86 correlation with video views. 

Data Split: Divided data into a 75/25 train/test split and applied One-Hot Encoding to categorical features.



<h3>next steps</h3>

Pipeline Integration: Port video duration weights into the main claim-vs-opinion model to refine classification.

Model Upgrades: Test advanced algorithms (e.g., Random Forest, XGBoost) to improve precision beyond the current 61% baseline.

Queue Automation: Deploy a high-recall 84% threshold to automatically filter trusted accounts from urgent moderation queues.

<h3>key insights</h3> 

Video Duration Matters: Longer videos increase the log-odds of a user being verified 0.0086 coefficient for video_duration_sec).
Engagement Disconnect: High video view, share, and comment counts show a negligible independent correlation with an author's verification status, proving that viral engagement metrics alone do not inherently dictate whether an account gets verified. 

Text Length Patterns: Unverified accounts write slightly longer video scripts on average 89.4 characters) than verified accounts 84.6 characters. 

Balanced Performance: The baseline model achieved 61% Precision, 84% Recall, and 65% Accuracy on validation data. 
(Note: 0 = Unverified, 1 = Verified). 


