# Phishing URL Detection

This project uses Machine Learning to classify URLs as phishing or legitimate based on structural and content features. 

**Dataset Source:** [PhiUSIIL Phishing URL Dataset](https://archive.ics.uci.edu/dataset/967/phiusiil+phishing+url+dataset)

## Environment Setup
The necessary libraries can be installed using the `requirements.txt` file or by running the installation cell at the top of the notebook.

Command:
```bash
pip install -r requirements.txt
```

Libraries used: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`.

## Workflow
- **Preprocessing:** Metadata columns were removed, and the TLD feature was encoded into numeric values.
- **Feature Selection:** Redundant features with a correlation higher than 0.75 were dropped to prevent multicollinearity.
- **Training:** Performance of Logistic Regression, KNN, Naive Bayes, and Random Forest models was compared.
- **Optimization:** Hyperparameter tuning was performed via GridSearchCV to find the best model parameters.

## Key Results
- **Top Accuracy:** 99.97% was achieved using the Random Forest classifier.
- **Error Analysis:** Sophisticated phishing attacks were found to copy legitimate sites.
- **Robustness:** An additional experiment confirmed that URL-only features are sufficient for high detection rates, even without website content analysis.

## Files
- [phishingURLDetectionModelTraining.ipynb](./phishingURLDetectionModelTraining.ipynb): Full analysis and code.
- [Machine_Learning_Final_Project_Paper.pdf](./Machine_Learning_Final_Project_Paper.pdf): Detailed project paper.
- [requirements.txt](./requirements.txt): List of environment dependencies.
