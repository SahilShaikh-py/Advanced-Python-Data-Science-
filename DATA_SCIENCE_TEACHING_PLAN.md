# Data Science Master Bootcamp Teaching Plan

**Course Format:** Live Interactive Classroom and Self-Paced Modules  
**Classroom Teaching Formula (2+ Hours Deep Class):**  
- **Part 1 (Concept, Theory and Intuition):** Definition, Key Features, and Real-World Uses in short bullet points.  
- **Part 2 (Live Code-Along):** Step-by-step live demonstration of Python/Scikit-Learn/TensorFlow code with line-by-line comments.  
- **Part 3 (Student Hands-On Lab):** Live practice exercises for students in Google Colab.  
- **Part 4 (Advanced Edge Cases and Q&A):** Real-world industry pitfall resolution and student doubt clearing.

---

## Phase 1: Advanced Python and Data Science Foundations

### Lecture 1: Python Memory Model, Objects and Advanced Data Structures
- **Part 1:** Mutable vs Immutable objects, memory allocation (`id()`), deep vs shallow copy.
- **Part 2:** Code-Along: Efficient dictionary comprehensions and custom tuple/set operations.
- **Part 3:** Student Lab: Practice exercises parsing nested JSON responses from APIs.
- **Part 4:** Q&A: Memory optimization techniques in Python.

### Lecture 2: Object-Oriented Programming (OOPs) in Python
- **Part 1:** Classes, Objects, `__init__`, `self`, Inheritance, Encapsulation, Dunder methods (`__str__`, `__repr__`, `__len__`).
- **Part 2:** Code-Along: Building a custom `DataPreprocessor` class.
- **Part 3:** Student Lab: Building a custom `DatasetEvaluator` class with summary methods.
- **Part 4:** Q&A: When to use functional programming vs OOPs in Data Science.

### Lecture 3: Advanced Generators, Decorators and Context Managers
- **Part 1:** Memory-efficient iteration using `yield`, custom decorators (`@timer`, `@logger`), `with` statements.
- **Part 2:** Code-Along: Building an execution timing decorator and memory chunk generator.
- **Part 3:** Student Lab: Writing a CSV stream reader generator for large datasets.
- **Part 4:** Q&A: Avoiding memory overflow during big data loading.

### Lecture 4: Vectorized NumPy 1D/2D Array Operations
- **Part 1:** Contiguous memory architecture, why NumPy is 100x faster than standard Python lists.
- **Part 2:** Code-Along: 2D array indexing, slicing, masking, and reshape operations.
- **Part 3:** Student Lab: Calculating moving averages and boolean masks on financial series.
- **Part 4:** Q&A: Indexing mistakes and dimension mismatch errors.

### Lecture 5: Matrix Math and Linear Systems with NumPy
- **Part 1:** Dot products (`np.dot`), Matrix multiplication (`@`), Matrix transpose (`.T`), Inverse (`np.linalg.inv`).
- **Part 2:** Code-Along: Solving systems of linear equations ($Ax = b$) using NumPy.
- **Part 3:** Student Lab: Computing portfolio dot product returns for multiple assets.
- **Part 4:** Q&A: Singular matrices and determinant edge cases.

---

## Phase 2: Mathematics, Statistics and Interactive EDA

### Lecture 6: Linear Algebra and Vector Spaces for Data Science
- **Part 1:** Vector spaces, Cosine Similarity, Norms ($L_1, L_2$), Eigenvalues and Eigenvectors intuition.
- **Part 2:** Code-Along: Calculating cosine similarity between user preference vectors.
- **Part 3:** Student Lab: Computing Euclidean vs Manhattan distance metrics.
- **Part 4:** Q&A: Dimensionality reduction intuition via eigenvalues.

### Lecture 7: Differential Calculus and Gradient Descent Math
- **Part 1:** Derivatives, Partial derivatives, Slope intuition, Cost functions (MSE), Gradient Descent algorithm ($w = w - \alpha \nabla L$).
- **Part 2:** Code-Along: Writing Gradient Descent from scratch in Python to find minimum of a loss function.
- **Part 3:** Student Lab: Implementing learning rate experimentation and plotting loss curve.
- **Part 4:** Q&A: Exploding and vanishing gradients intuition.

### Lecture 8: Descriptive and Inferential Statistics
- **Part 1:** Central Limit Theorem (CLT), Normal Distribution, Skewness, Kurtosis, Z-Score.
- **Part 2:** Code-Along: Simulating Central Limit Theorem with random samples in Python.
- **Part 3:** Student Lab: Standardizing continuous features using Z-score formula.
- **Part 4:** Q&A: Parametric vs Non-parametric statistical assumptions.

### Lecture 9: Hypothesis Testing and A/B Testing Engine
- **Part 1:** Null Hypothesis ($H_0$), Alternative ($H_1$), p-value threshold ($\alpha = 0.05$), One-sample t-test, Two-sample t-test, Chi-Square.
- **Part 2:** Code-Along: Conducting a full A/B testing analysis on website conversion rates using `scipy.stats`.
- **Part 3:** Student Lab: Evaluating whether a new checkout design significantly increased revenue per user.
- **Part 4:** Q&A: Type I vs Type II errors and statistical power.

### Lecture 10: Interactive Storytelling with Seaborn and Plotly
- **Part 1:** Visual encoding principles, Seaborn heatmaps, Plotly interactive 3D scatter plots.
- **Part 2:** Code-Along: 5-Step Exploratory Data Analysis (EDA) on housing dataset.
- **Part 3:** Student Lab: Identifying multi-collinearity via correlation matrix heatmaps.
- **Part 4:** Q&A: Selecting effective chart types for non-technical stakeholders.

---

## Phase 3: Machine Learning Engineering

### Lecture 11: Supervised Learning Framework and Simple Linear Regression
- **Part 1:** Supervised vs Unsupervised learning, Cost Function (MSE), Ordinary Least Squares (OLS).
- **Part 2:** Code-Along: Fitting `LinearRegression` from Scikit-Learn, plotting regression line.
- **Part 3:** Student Lab: Predicting housing prices from square footage.
- **Part 4:** Q&A: Interpreting slope coefficients and intercepts.

### Lecture 12: Multiple Linear Regression and Regularization (Ridge and Lasso)
- **Part 1:** Multicollinearity, Overfitting vs Underfitting, Ridge ($L_2$) vs Lasso ($L_1$) feature selection.
- **Part 2:** Code-Along: Comparing Linear, Ridge, and Lasso regression using `housing_prices.csv`.
- **Part 3:** Student Lab: Tuning regularization hyperparameter $\alpha$ with `RidgeCV`.
- **Part 4:** Q&A: When to choose Lasso for feature elimination.

### Lecture 13: Logistic Regression and Classification Evaluation Metrics
- **Part 1:** Sigmoid function ($\sigma(z)$), Odds Ratio, Binary Cross-Entropy Loss, Confusion Matrix, Precision, Recall, F1-Score, ROC-AUC curve.
- **Part 2:** Code-Along: Training Logistic Regression on `customer_churn_ds.csv` and plotting ROC curve.
- **Part 3:** Student Lab: Calculating Precision-Recall trade-offs for high-risk churn customers.
- **Part 4:** Q&A: Dealing with imbalanced classification datasets.

### Lecture 14: Non-Linear Models: Decision Trees and Hyperparameter Tuning
- **Part 1:** Information Gain, Gini Impurity, Entropy, Tree Depth, Hyperparameter Search (GridSearchCV vs RandomizedSearchCV).
- **Part 2:** Code-Along: Visualizing a Decision Tree classifier and tuning `max_depth` & `min_samples_split`.
- **Part 3:** Student Lab: Pruning an overfitted decision tree model.
- **Part 4:** Q&A: Decision tree instability and variance reduction.

### Lecture 15: Ensemble Methods: Random Forests and Boosting (XGBoost)
- **Part 1:** Bagging (Bootstrap Aggregation), Out-of-Bag (OOB) Score, Boosting intuition (Gradient Boosting & XGBoost).
- **Part 2:** Code-Along: Building an XGBoost classifier with early stopping on customer churn dataset.
- **Part 3:** Student Lab: Plotting Feature Importance graphs for Random Forests vs XGBoost.
- **Part 4:** Q&A: XGBoost hyperparameters (`learning_rate`, `n_estimators`, `subsample`).

### Lecture 16: Unsupervised Learning: K-Means Clustering and Hierarchical
- **Part 1:** Centroid-based clustering, Distance metrics, Elbow Method, Silhouette Score, Dendrograms.
- **Part 2:** Code-Along: Segmenting customers into behavioral clusters using `KMeans`.
- **Part 3:** Student Lab: Finding optimal $K$ clusters using Silhouette analysis.
- **Part 4:** Q&A: Sensitivity to scaling (`StandardScaler` requirement).

### Lecture 17: Dimensionality Reduction: Principal Component Analysis (PCA)
- **Part 1:** Curse of Dimensionality, Covariance matrix, Variance explained, PCA projection.
- **Part 2:** Code-Along: Reducing high-dimensional features to principal components for visualization.
- **Part 3:** Student Lab: Plotting Cumulative Variance Explained ratio curve.
- **Part 4:** Q&A: Loss of feature interpretability in PCA.

---

## Phase 4: Deep Learning and Neural Networks

### Lecture 18: Artificial Neural Networks (ANN) and Perceptron Math
- **Part 1:** Biological vs Artificial Neuron, Forward Propagation, Activation Functions (Sigmoid, Tanh, ReLU, Softmax).
- **Part 2:** Code-Along: Building a single neuron from scratch in NumPy.
- **Part 3:** Student Lab: Implementing forward propagation matrix math.
- **Part 4:** Q&A: Why ReLU avoids vanishing gradients.

### Lecture 19: Deep Neural Networks with TensorFlow and Keras
- **Part 1:** Multi-layer Perceptron (MLP) architecture, Categorical Cross-Entropy, Optimizers (Adam, SGD).
- **Part 2:** Code-Along: Training a Keras Sequential ANN model on structured data.
- **Part 3:** Student Lab: Adding Dropout layers and EarlyStopping callbacks.
- **Part 4:** Q&A: Learning rate scheduling and batch size selection.

### Lecture 20: Convolutional Neural Networks (CNN) Foundations
- **Part 1:** Image tensors ($H \times W \times C$), Convolution operation, Kernels/Filters, Stride, Padding (`same` vs `valid`).
- **Part 2:** Code-Along: Visualizing feature map outputs of a 2D Convolution layer.
- **Part 3:** Student Lab: Designing a custom filter for edge detection.
- **Part 4:** Q&A: Receptive field expansion across deep layers.

### Lecture 21: Deep CNN Architectures and Transfer Learning
- **Part 1:** Pooling layers (Max Pooling), Flattening, Dense layers, Transfer Learning concept (ResNet, MobileNet).
- **Part 2:** Code-Along: Training a CNN image classifier with data augmentation (`ImageDataGenerator`).
- **Part 3:** Student Lab: Fine-tuning a pre-trained model for medical image classification.
- **Part 4:** Q&A: Freezing vs unfreezing pre-trained backbone layers.

### Lecture 22: Model Diagnostics and Regularization in Deep Learning
- **Part 1:** Overfitting vs Underfitting in Neural Networks, Batch Normalization, Weight Regularization ($L_2$).
- **Part 2:** Code-Along: Plotting Training vs Validation Loss & Accuracy curves.
- **Part 3:** Student Lab: Tuning Batch Normalization positions in deep architectures.
- **Part 4:** Q&A: Debugging non-converging loss curves.

---

## Phase 5: Modern AI, GenAI and LLM Fundamentals

### Lecture 23: Natural Language Processing (NLP) and Text Preprocessing
- **Part 1:** Text Tokenization, Stopwords removal, Lemmatization, TF-IDF Vectorization, N-grams.
- **Part 2:** Code-Along: Preprocessing customer reviews using NLTK and `TfidfVectorizer`.
- **Part 3:** Student Lab: Training a Naive Bayes classifier on sentiment text data.
- **Part 4:** Q&A: Limitations of Bag-of-Words vs Contextual Embeddings.

### Lecture 24: Modern Word Embeddings and HuggingFace Models
- **Part 1:** Dense Vector Embeddings (Word2Vec, HuggingFace Sentence Transformers), Cosine Similarity search.
- **Part 2:** Code-Along: Extracting 384-dimensional dense embeddings using HuggingFace models in Python.
- **Part 3:** Student Lab: Building a semantic similarity search engine across customer queries.
- **Part 4:** Q&A: Dimensionality of embeddings and spatial clustering.

### Lecture 25: Vector Databases (ChromaDB and FAISS)
- **Part 1:** Why traditional relational databases fail at vector search, Approximate Nearest Neighbors (ANN), Vector Indexing.
- **Part 2:** Code-Along: Creating a ChromaDB collection, inserting text embeddings, and querying top-$k$ results.
- **Part 3:** Student Lab: Persisting vector database collections locally.
- **Part 4:** Q&A: Distance metrics in Vector DBs (Cosine vs L2 vs Inner Product).

### Lecture 26: Retrieval-Augmented Generation (RAG) Architecture
- **Part 1:** Large Language Models (LLMs), Context Windows, Prompt Engineering, RAG Framework (Document Chunking -> Embedding -> Vector Search -> LLM Prompting).
- **Part 2:** Code-Along: Building a simple RAG document Q&A pipeline in Python.
- **Part 3:** Student Lab: Experimenting with document chunk size and overlap strategies.
- **Part 4:** Q&A: Handling hallucination and verifying source attribution.

---

## Phase 6: MLOps, Model Deployment and Production Capstone

### Lecture 27: Model Serialization and FastAPI REST Endpoint
- **Part 1:** Model persistence (`joblib`, `pickle`), REST API concepts (GET, POST, JSON payloads), Pydantic data validation.
- **Part 2:** Code-Along: Building a FastAPI REST endpoint that serves predictions from a trained ML model.
- **Part 3:** Student Lab: Testing API endpoints using Swagger UI and Postman.
- **Part 4:** Q&A: Handling API error codes and input validation exceptions.

### Lecture 28: Interactive Web App Dashboard with Streamlit
- **Part 1:** Rapid UI prototyping with Streamlit (`st.title`, `st.sidebar`, `st.file_uploader`, `st.plotly_chart`).
- **Part 2:** Code-Along: Developing an interactive web dashboard for real-time model predictions.
- **Part 3:** Student Lab: Adding interactive sliders and dynamic feature input widgets.
- **Part 4:** Q&A: State management (`st.session_state`) in Streamlit.

### Lecture 29: Full-Stack Production AI Capstone Integration
- **Part 1:** Combining ML Predictive Engine + Vector DB + Streamlit UI into a single production application.
- **Part 2:** Code-Along: Integrating the end-to-end AI Capstone codebase.
- **Part 3:** Student Lab: Executing end-to-end integration tests.
- **Part 4:** Q&A: Debugging multi-tier AI applications.

### Lecture 30: MLOps Deployment and Student Portfolio Showcase
- **Part 1:** Publishing web apps to Streamlit Cloud, GitHub repository optimization, resume building for Data Science roles.
- **Part 2:** Code-Along: Deploying the Capstone project live on the web.
- **Part 3:** Student Lab: Finalizing student GitHub README portfolio links.
- **Part 4:** Q&A: Mock technical interview questions and career guidance.
