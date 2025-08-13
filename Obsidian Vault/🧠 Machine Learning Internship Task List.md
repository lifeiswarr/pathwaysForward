# [[VANITY]]. [[PROJECTS]]. 
#urgent 

Complete **at least 3 tasks** for 2-week internship  
Complete **at least 4 tasks** for 1-month internship  
Choose tasks from **any level**.

---

## ✅ Level 1 Tasks

### 🔹 Task 1: Student Score Prediction (Regression)
- [ ] Load and explore the dataset.
- [ ] Handle missing/null values.
- [ ] Visualize data: distributions, scatterplot (Study Hours vs. Score).
- [ ] Split data into training/testing (80/20).
- [ ] Train a `LinearRegression` model.
- [ ] Evaluate using MAE, RMSE, R².
- [ ] Visualize predictions vs actuals.
- [ ] BONUS:
  - [ ] Try polynomial regression.
  - [ ] Add/remove features (e.g., sleep, participation).
  - [ ] Use regularization (Ridge/Lasso).

---

### 🔹 Task 2: Customer Segmentation (Clustering)
- [ ] Load Mall Customer dataset.
- [ ] Check nulls, describe basic stats.
- [ ] Apply feature scaling (`StandardScaler`).
- [ ] Visualize Income vs Spending Score.
- [ ] Use Elbow method to find optimal `k`.
- [ ] Train and fit `KMeans`.
- [ ] Visualize clusters using 2D scatter plots.
- [ ] Analyze spending behavior by cluster.
- [ ] BONUS:
  - [ ] Try DBSCAN or hierarchical clustering.
  - [ ] Cluster by age/gender/income jointly.

---

## ✅ Level 2 Tasks

### 🔹 Task 3: Forest Cover Type Classification (Multi-class)
- [ ] Load Covertype dataset.
- [ ] Clean data and handle categorical features.
- [ ] Scale numerical features.
- [ ] Train `RandomForestClassifier` or `XGBoost`.
- [ ] Evaluate with confusion matrix, accuracy.
- [ ] Plot feature importances.
- [ ] BONUS:
  - [ ] Compare Random Forest vs XGBoost.
  - [ ] Perform hyperparameter tuning.

---

### 🔹 Task 4: Loan Approval Prediction (Binary Classification)
- [ ] Load Loan Approval dataset.
- [ ] Handle missing values.
- [ ] Encode categorical variables.
- [ ] Train `LogisticRegression` and `DecisionTree`.
- [ ] Evaluate: Precision, Recall, F1-score.
- [ ] Plot confusion matrix.
- [ ] BONUS:
  - [ ] Use SMOTE to fix class imbalance.
  - [ ] Try Random Forest or XGBoost.

---

## ✅ Level 3 Tasks

### 🔹 Task 5: Movie Recommendation System (Similarity-based)
- [ ] Load MovieLens 100K dataset.
- [ ] Create user-item rating matrix.
- [ ] Clean sparse users/items.
- [ ] Compute user-user cosine similarity.
- [ ] Recommend unseen movies based on top-k similar users.
- [ ] Evaluate with Precision@K.
- [ ] BONUS:
  - [ ] Try item-based filtering.
  - [ ] Implement matrix factorization (SVD).

---

### 🔹 Task 6: Music Genre Classification (Audio)
- [ ] Load GTZAN audio dataset.
- [ ] Extract MFCCs or chroma features using `librosa`.
- [ ] Train classifier (Random Forest, XGBoost).
- [ ] Evaluate using accuracy, confusion matrix.
- [ ] BONUS:
  - [ ] Convert to spectrograms and use CNN.
  - [ ] Apply transfer learning (e.g., ResNet).

---

### 🔹 Task 7: Sales Forecasting (Time Series)
- [ ] Load Walmart Sales dataset.
- [ ] Create time-based features (lag, day, month, holiday).
- [ ] Split train/test using time-aware strategy.
- [ ] Train `XGBoost` or `LightGBM`.
- [ ] Plot actual vs. predicted sales.
- [ ] Evaluate using RMSE.
- [ ] BONUS:
  - [ ] Apply seasonal decomposition.
  - [ ] Try Prophet/ARIMA for comparison.

---

## ✅ Industry-Level Task

### 🔹 Task 8: Traffic Sign Recognition (Computer Vision CNN)
- [ ] Load GTSRB dataset.
- [ ] Preprocess images (resize, normalize).
- [ ] Train custom CNN using `Keras`.
- [ ] Use data augmentation.
- [ ] Evaluate using accuracy, confusion matrix.
- [ ] BONUS:
  - [ ] Compare with pre-trained model (e.g., MobileNet).
  - [ ] Try OpenCV for preprocessing pipeline.

---

## ⚙️ Tools & Libraries Used

- Python
- Pandas, NumPy, Matplotlib, Seaborn
- Scikit-learn, XGBoost, LightGBM
- Keras, TensorFlow
- OpenCV, Librosa
