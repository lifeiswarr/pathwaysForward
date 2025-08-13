# [[PROJECTS]]. [[VANITY]].
> Complete 3 out of 5 projects by **24th July 2025**

---

## 🚀 Task 1: News Topic Classifier Using BERT

### 🔧 Project Goal
Fine-tune BERT to classify news headlines using the AG News dataset.

### ✅ Task List
- [ ] Define problem statement and objectives
- [ ] Load AG News dataset from Hugging Face
- [ ] Explore and understand class distribution
- [ ] Tokenize dataset using `bert-base-uncased` tokenizer
- [ ] Split dataset into train/validation/test
- [ ] Create PyTorch Dataset and Dataloader
- [ ] Fine-tune BERT model using Hugging Face `Trainer`
- [ ] Use metrics: Accuracy and F1-score
- [ ] Visualize confusion matrix and classification report
- [ ] Deploy model using Streamlit or Gradio
- [ ] Write `README.md` with objective, approach, and results
- [ ] Push final code to GitHub

---

## 🔁 Task 2: End-to-End ML Pipeline (Scikit-learn)

### 🔧 Project Goal
Build a customer churn prediction pipeline with scikit-learn.

### ✅ Task List
- [ ] Define objective and overview of churn prediction
- [ ] Load Telco Churn Dataset
- [ ] Analyze features and data imbalance
- [ ] Create preprocessing pipeline (handle missing values, encode categoricals, scale numerics)
- [ ] Create full scikit-learn pipeline with `Pipeline` API
- [ ] Train baseline models: Logistic Regression & Random Forest
- [ ] Use `GridSearchCV` for hyperparameter tuning
- [ ] Evaluate using accuracy, precision, recall, F1-score
- [ ] Export pipeline with `joblib`
- [ ] Document pipeline and results in `README.md`
- [ ] Push final code to GitHub

---

## 🏘 Task 3: Multimodal ML – Housing Price Prediction

### 🔧 Project Goal
Use images + structured data to predict housing prices.

### ✅ Task List
- [ ] Define multimodal objective
- [ ] Gather/Download structured + image dataset
- [ ] Preprocess tabular features (e.g., scaling, encoding)
- [ ] Resize and normalize images for CNN input
- [ ] Create CNN model to extract image features
- [ ] Extract image features and concatenate with tabular features
- [ ] Build regression model combining both modalities
- [ ] Train and evaluate using MAE and RMSE
- [ ] Visualize predictions vs actual
- [ ] Document model architecture and data fusion approach in `README.md`
- [ ] Push project to GitHub

---

## 💬 Task 4: Context-Aware Chatbot (LangChain or RAG)

### 🔧 Project Goal
Build a chatbot that retrieves knowledge and remembers context.

### ✅ Task List
- [ ] Define the chatbot use-case
- [ ] Prepare custom corpus (e.g., Wikipedia pages or PDFs)
- [ ] Preprocess text and generate document chunks
- [ ] Embed text using OpenAI, SentenceTransformers, or similar
- [ ] Create vector store using FAISS or ChromaDB
- [ ] Use LangChain or RAG to build the retrieval pipeline
- [ ] Implement conversational memory
- [ ] Integrate everything in Streamlit app
- [ ] Test chatbot on real-world queries
- [ ] Document approach and vector store setup in `README.md`
- [ ] Push chatbot repo to GitHub

---

## 🏷 Task 5: Auto Tagging Support Tickets Using LLM

### 🔧 Project Goal
Classify and rank support ticket tags using LLMs.

### ✅ Task List
- [ ] Load and clean support ticket dataset
- [ ] Explore data structure and common labels
- [ ] Implement zero-shot classification using an LLM (e.g., OpenAI, Cohere, Hugging Face)
- [ ] Test few-shot learning with better examples
- [ ] Fine-tune LLM on ticket dataset (optional, advanced)
- [ ] Compare accuracy across zero-shot, few-shot, and fine-tuned setups
- [ ] Generate top 3 probable tags for each ticket
- [ ] Visualize tag prediction confidence
- [ ] Document prompt engineering strategy and comparison results in `README.md`
- [ ] Push all notebooks/scripts to GitHub

---

# 📦 Submission Checklist (For Each Task)
- [ ] Jupyter Notebook or Python script
- [ ] Dataset preprocessing and loading
- [ ] Model training + evaluation
- [ ] Deployment (if applicable)
- [ ] Visualizations (if applicable)
- [ ] Summary/Insights section
- [ ] Clear, commented code
- [ ] GitHub repo with clean structure
- [ ] `README.md` with objective, approach, and key results
- [ ] Submit GitHub link via Google Classroom
