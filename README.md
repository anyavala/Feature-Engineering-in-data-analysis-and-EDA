# Feature-Engineering-in-data-analysis-and-EDA
### TOPICS

1. Handling missing values
2. Handling Imbalanced Dataset
3. Handling Imbalanced Dataset using Smote
4. Handling outliers 
5. Data encoding-Nominal or OHE
6. Label and Ordinal Encoding 
7. Target Guided Ordinal Encoding


### Feature Engineering in Data Analysis
Feature engineering is the process of transforming raw data into meaningful inputs that improve model performance. Here are the key steps:

#### 1. Understanding the Data

- Explore the dataset (EDA) — distributions, correlations, missing values
- Understand the domain context to know which features are meaningful
- Identify target variable and its relationship with input features


#### 2. Handling Missing Values

- Imputation — fill with mean, median, mode, or a model prediction
- Indicator variables — add a binary column flagging where data was missing
- Dropping — remove rows/columns with too many missing values


#### 3. Encoding Categorical Variables

- Label encoding — assign integers to categories (ordinal data)
- One-hot encoding — create binary columns per category (nominal data)
- Target encoding — replace category with mean target value
- Frequency encoding — replace category with its occurrence count


#### 4. Scaling & Normalization

- Standardization (Z-score) — mean=0, std=1; good for algorithms sensitive to scale
- Min-Max scaling — compress values into [0, 1]
- Log/Power transforms — reduce skewness in heavily skewed distributions


#### - 5. Creating New Features

- Interaction features — multiply or combine two variables (e.g., height × width = area)
- Polynomial features — add squared or cubed versions of features
- Aggregations — group-level stats (mean, max, count per category)
- Date/time decomposition — extract hour, day, month, weekday, quarter from timestamps


#### 6. Handling Outliers

- Detect using IQR, Z-score, or visualization (box plots)
- Cap/floor (winsorizing), transform, or remove extreme values


#### 7. Feature Transformation

- Binning/Discretization — convert continuous values into buckets (e.g., age groups)
- Log transform — compress wide-ranging values
- Rank transform — replace values with their rank


#### 8. Feature Extraction (from complex data types)

- Text — TF-IDF, word embeddings, bag-of-words
- Images — pixel stats, edge detection, CNN-based embeddings
- Time series — rolling averages, lag features, FFT components


#### 9. Feature Selection
Remove irrelevant or redundant features to reduce noise and overfitting:

- Filter methods — correlation, chi-square, variance threshold
- Wrapper methods — recursive feature elimination (RFE)
- Embedded methods — LASSO regularization, feature importance from tree models


#### 10. Validation

- Check that engineered features don't cause data leakage (future info leaking into training)
- Verify feature distributions are consistent between train and test sets
- Re-run model to confirm features actually improve performance