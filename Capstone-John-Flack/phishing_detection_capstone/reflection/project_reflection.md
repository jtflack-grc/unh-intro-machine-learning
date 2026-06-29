# Project Reflection

This capstone showed how supervised machine learning can support phishing website detection by classifying websites as legitimate or phishing based on structured website characteristics.

The main learning point was that model evaluation in cybersecurity cannot rely on accuracy alone. False negatives are especially important because they represent phishing websites that would be incorrectly treated as legitimate. False positives also matter because they can create unnecessary analyst workload or block legitimate sites.

The biggest challenge was organizing the project so that the notebook, documentation, dataset, and GitHub repository all supported the same final story. This was addressed by using a CRISP-DM-style workflow, comparing Logistic Regression and Random Forest models, and documenting both model performance and responsible AI limitations.

With more time, this project could be improved by testing additional models, tuning thresholds, exporting figures as separate files, evaluating model drift over time, and adding explainability tools such as SHAP or LIME.
