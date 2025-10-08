# Airbnb-Analysis-📊 Strategic Host Portfolio Analysis: Mitigating Operational Friction
Project Overview
This project implements an advanced business intelligence strategy to segment and predict the success of host portfolios using a publicly available Airbnb dataset. The analysis moves beyond simple descriptive statistics to identify key operational "blind spots" and pricing inconsistencies that drive marketplace performance.

The core deliverable is a Precision Host Management Strategy supported by predictive modeling insights.

🎯 Critical Business Problem
The challenge addressed is the trade-off between host control (operational rigidity) and guest experience (market success). We aim to quantify this tension to answer:

How can the platform guide hosts to optimize their operational rigor and pricing strategy to maximize a balanced Host Success Metric (HSM), thereby enhancing overall platform yield?

✨ Unique Findings & Engineered Metrics
To solve this problem, three critical, unique metrics were engineered and used in the predictive model:

Metric Name

Description

Strategic Value

Host Success Metric (HSM)

A composite target variable: HSM=(0.6×Review Rate)+(0.4×Normalized Reviews/Month).

Balances quality (rating) and volume (bookings) for holistic success measurement.

Operational Friction Index (OFI)

A scaled score combining Minimum Nights and Cancellation Policy Strictness.

Quantifies the barriers hosts impose on guests, revealing sources of friction.

Price Deviation Score

Listing Price−Region Median Price.

Unique Insight: Identifies listings that are significantly over- or under-priced relative to their local market median, highlighting pricing blind spots.

🛠️ Methodology & Models
Feature Engineering: Creation of HSM, OFI, Price Deviation Score, and Yield Efficiency Score.

Host Segmentation (K-Means Clustering): Applied to the full feature set to identify 4 distinct host archetypes (e.g., "The Friction Masters," "The Over-Priced Operators").

Predictive Modeling (Random Forest Regressor): Trained to predict the Host Success Metric (HSM). The resulting Feature Importance analysis reveals which factors truly matter.

📈 Key Visualizations
The analysis generates three high-impact visualizations to support strategic recommendations:

Feature Importance Chart: Ranks drivers of HSM, showing that operational factors (like OFI and Yield) often outweigh basic metrics like price.

Price-Volume Trade-off Plot: Maps host segments onto a scatter plot of Price vs. Normalized Reviews/Month to illustrate market positioning and identify low-performing high-price outliers.

Geospatial Success Map: Plots HSM distribution geographically, highlighting regions where success clusters occur.

🚀 Getting Started
Prerequisites
You need Python installed, along with the following libraries (all installed via pip):

pip install pandas numpy scikit-learn matplotlib seaborn

Running the Analysis
Data File: Ensure the input CSV file 1730285881-Airbnb_Open_Data.xlsx - in.csv is located in the same directory as the Python script.

Execute Script: Run the main analysis file from your terminal:

python data_analysis.py

The script will print the Segment Profiles, Feature Importance rankings, Model Evaluation (MSE), and automatically display the three generated plots.

📁 Repository Structure
├── data_analysis.py      # Main Python script for data processing, modeling, and visualization
├── 1730285881-Airbnb_Open_Data.xlsx - in.csv # Raw input dataset
└── README.md             # This document
