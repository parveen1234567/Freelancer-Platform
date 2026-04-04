Freelancer Job Postings Analysis

📌 Project Overview
This project analyzes a dataset of freelancer job postings to uncover insights about job titles, client behavior, pricing, and tags. The workflow includes data preprocessing, exploratory data analysis (EDA), visualization, and dimensionality reduction (PCA).

The goal is to clean the dataset, handle missing values, encode categorical variables, and perform statistical and visual analysis to better understand freelancing trends.

📂 Dataset
Source: freelancer_job_postings0.csv

Size: 9,193 rows × 13 columns (expanded to 197 columns after preprocessing)

Key Features:

projectId – Unique identifier for each project

job_title, job_description, tags – Textual information about the job

client_state, client_country – Location details

client_average_rating, client_review_count – Client credibility metrics

min_price, max_price, avg_price – Pricing details

currency, rate_type – Payment information

⚙️ Preprocessing Steps
Missing Values Handling

Filled client_state and client_country with "Unknown".

Data Type Conversion

Converted price columns (min_price, max_price, avg_price) to numeric.

Tags Transformation

Converted string-based lists in tags column into actual Python lists.

Categorical Encoding

One-hot encoded client_country, currency, and rate_type.

Feature Engineering

Added price_range = max_price - min_price.

Rounded client_average_rating to one decimal place.

Text Normalization

Converted job_title and job_description to lowercase and removed special characters.

📊 Exploratory Data Analysis (EDA)
Univariate Analysis

Distribution of client ratings and review counts

Frequency of job titles and tags

Price distributions (min, max, avg)

Bivariate Analysis

Rate type vs average price

Client state vs average price and review count

Min price vs max price correlations

Multivariate Analysis

Pair plots for ratings, reviews, and pricing

Correlation heatmap

🔬 Advanced Analysis
Principal Component Analysis (PCA)

Reduced numerical features into 2 principal components for visualization.

Outlier Detection

Used Interquartile Range (IQR) method to identify anomalies in pricing and ratings.

📈 Visualizations
Histograms for ratings, reviews, and prices

Bar plots for job titles, tags, client states, and currencies

Scatter plots for price relationships

Box plots for client states vs reviews/ratings

Heatmaps for correlation analysis

PCA scatter plot

💾 Output
Preprocessed dataset saved as:

processed_dataset.csv

Updated original file with cleaned data

🚀 How to Run
Clone the repository:

bash
git clone https://github.com/parveen1234567/Freelancer-Platform.git
Navigate to the project folder:

bash
cd Freelancer-Platform
Run the notebook:

bash
jupyter notebook freelancing_platform_FINAL.ipynb
Ensure required libraries are installed:

bash
pip install pandas numpy matplotlib seaborn scikit-learn
📜 Requirements
Python 3.8+

Libraries: pandas, numpy, matplotlib, seaborn, scikit-learn

🏆 Key Learnings
Handling missing values and categorical encoding

Text normalization for NLP tasks

Feature engineering for price ranges

Visualizing client and job trends

Applying PCA for dimensionality reduction

Detecting outliers in freelancing data
