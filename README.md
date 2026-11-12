# 🖐️ Hi, I am UDAY D.K
AI/ML enthusiast focused on Deep Learning, NLP, Generative AI, and LLMs. Interested in understanding modern AI systems from the fundamentals of neural networks and Transformers to fine-tuning, retrieval-augmented generation, and intelligent agents.


## 🌐 Socials:
![ LinkedIn ](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white) www.linkedin.com/in/udaydk2319.
 ![ email ](https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white) udaydk587@gmail.com
## 💻 Tech Stack:

![Python](https://img.shields.io/badge/Python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)
![Transformers](https://img.shields.io/badge/Transformers-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)
![PEFT](https://img.shields.io/badge/PEFT-FF6F00?style=for-the-badge)
![LoRA](https://img.shields.io/badge/LoRA-8A2BE2?style=for-the-badge)
![QLoRA](https://img.shields.io/badge/QLoRA-6A5ACD?style=for-the-badge)
![LLMs](https://img.shields.io/badge/LLMs-412991?style=for-the-badge)
![RAG](https://img.shields.io/badge/RAG-00A67E?style=for-the-badge)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=for-the-badge)
![XGBoost](https://img.shields.io/badge/XGBoost-FF6600?style=for-the-badge)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-336791?style=for-the-badge)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=matplotlib&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)
![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=for-the-badge&logo=mlflow&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=white)

### 🚀 Featured Projects

> Click any project to expand it.

<details>
<summary><b>🤖 AssistIQ: AI Customer Support Agent</b> · an agent that can safely refund and cancel orders</summary>
<br/>

Most support bots either only answer FAQs or call backend actions directly, which lets a customer trick them into refunding the wrong order. AssistIQ resolves refunds and cancellations itself, but **the AI decides what the customer wants and the code decides what is allowed.**

- Every action passes **ownership checks, policy rules written in code, customer confirmation and staff approval**
- **64-case safety test suite:** 50 attacks (prompt injection, impersonating staff, policy bypass, double refunds) and 14 normal requests
- **Result:** blocks **50/50 attacks** even when the AI is replaced by a worst-case model that falls for everything
- Deployed to **Google Cloud Run** with CI/CD

**Stack:** LangGraph · Gemini · FastAPI · PostgreSQL · Streamlit · Cloud Run

🔗 [View repository](https://github.com/uday2319/AssistIQ-AI_Powered-Customer_Support-Agent)
</details>

<details>
<summary><b>💰 Financial LLM Fine-Tuning</b> · TinyLlama 1.1B adapted for finance with LoRA and QLoRA</summary>
<br/>

General-purpose LLMs often give weak answers in specialized domains. This project fine-tunes **TinyLlama 1.1B Chat** to answer finance questions about **inflation, SIP, mutual funds, stocks, bonds, income tax, GST, insurance, PPF and NPS**.

- **LoRA:** freezes the base model and trains only small adapter layers
- **QLoRA:** loads the model in **4-bit NF4** to cut GPU memory use even further
- Compares both approaches on memory use and training loss
- Shows that domain-specific LLM fine-tuning is possible on limited GPUs

**Stack:** Hugging Face · Transformers · PEFT · bitsandbytes · PyTorch

🔗 [View repository](https://github.com/uday2319/Fintuned-LLm_on_Financial-domain_Lora-QLora)
</details>

<details>
<summary><b>📄 MultiRAG</b> · question answering over research papers</summary>
<br/>

A Retrieval-Augmented Generation system that answers questions about research papers **using only the retrieved text as evidence**, which reduces hallucinated answers.

- **Pipeline:** question → embedding → FAISS vector search → top-K chunks → local LLM → answer
- Configurable chunk size and overlap
- Runs the **Phi-3 model locally through Ollama**, so no paid API is needed
- REST API with Swagger docs, source metadata, latency measurement and logging

**Stack:** Sentence Transformers · FAISS · Ollama (Phi-3) · FastAPI

🔗 [View repository](https://github.com/uday2319/Multi-RAG-Application)
</details>

<details>
<summary><b>🧭 CityWise</b> · AI travel planner from a single sentence</summary>
<br/>

Describe your trip in your own words, for example *"I love ancient forts and local street food"*, and CityWise builds a full **day-by-day plan** with real places, road routes, restaurants and hotels.

- **Semantic search** with Sentence-BERT matches your preferences to real places
- A **FAISS index** is built for each request from live place data
- **XGBoost learning-to-rank** re-ranks the candidate places
- Plans trips of **1–14 days** within a daily budget in Indian Rupees
- Includes **voice translation** for travelers

**Stack:** Sentence-BERT · FAISS · XGBoost · FastAPI · React · TypeScript · Tailwind · Leaflet

🔗 [View repository](https://github.com/uday2319/CityWise)
</details>

<details>
<summary><b>🧠 Mini-GPT from Scratch</b> · a GPT-style language model built from scratch</summary>
<br/>

A minimal GPT built in PyTorch **without high-level LLM libraries**, to understand how modern language models work internally.

- Custom **tokenizer**, token embeddings and a causal Transformer decoder
- **Multi-head self-attention**, GELU feed-forward layers, layer normalization and residual connections
- Full training loop and **autoregressive text generation**
- **Config:** 4 layers, 8 heads, 256-dim embeddings, 128-token context

**Stack:** PyTorch

🔗 [View repository](https://github.com/uday2319/Mini-GPT-from-Scratch)
</details>

<details>
<summary><b>💼 Job Recommendation System</b> · skill-based job matching as a production-style API</summary>
<br/>

An end-to-end ML application that recommends relevant jobs based on a user's skills. It focuses on **building, testing, containerizing and deploying** a model, not just training one.

- **Content-based filtering:** TF-IDF on skills and job descriptions, ranked by cosine similarity
- Returns the **top-K matching jobs** through a REST API
- **CI/CD with GitHub Actions** and automated tests
- **Dockerized** for easy deployment

**Stack:** Scikit-learn · FastAPI · Docker · GitHub Actions

🔗 [View repository](https://github.com/uday2319/Recommendation-System)
</details>

<details>
<summary><b>🏥 Health Insurance Premium Predictor</b> · predicts medical insurance cost</summary>
<br/>

A regression model that estimates insurance premiums from **age, BMI, gender, number of children, region and smoking status**, served in a Streamlit app.

- Data cleaning, exploratory analysis, feature engineering and one-hot encoding
- Compared a **Decision Tree** with a **Random Forest**, then tuned the Random Forest with GridSearchCV
- **Results:** R² **0.87** · MAE **2356** · RMSE **4386**

**Stack:** Scikit-learn · Pandas · Joblib · Streamlit

🔗 [View repository](https://github.com/uday2319/Health-Insurance-Premium-Predictor)
</details>

<details>
<summary><b>👥 Employee Attrition Tracker</b> · predicts which employees are likely to leave</summary>
<br/>

An ML model that predicts employee attrition, served through a FastAPI `/predict` endpoint and **deployed live on Render**.

- REST API built with FastAPI
- Production setup with **Gunicorn + Uvicorn workers**
- 🌐 [Live demo](https://employee-attrition-performancefastapi-1.onrender.com)

**Stack:** Scikit-learn · Pandas · FastAPI · Render

🔗 [View repository](https://github.com/uday2319/Employee-Attrition-performance-Tracker)
</details>

<details>
<summary><b>🖼️ CNN Image Classification from Scratch</b> · CIFAR-10 classifier</summary>
<br/>

A convolutional neural network built from scratch to classify **CIFAR-10** images into 10 classes.

- **Convolution layers** extract features, **pooling** reduces spatial size, and **fully connected layers** classify
- Trained with backpropagation to minimize loss
- Builds understanding of feature learning, optimization and evaluation in deep learning

**Stack:** Python · Deep Learning · CNN

🔗 [View repository](https://github.com/uday2319/CNN-Image-Classification-from-scratch)
</details>

<details>
<summary><b>📈 Search Query Anomaly Detection</b> · finds unusual spikes in Google search data</summary>
<br/>

Detects **sudden changes** in what people search for, which helps identify trending topics, news events, errors or abnormal behavior.

- Analyzes search query trends over time
- Uses an ML model to separate **normal from unusual** search patterns

**Stack:** Python · Pandas · Scikit-learn · Jupyter

🔗 [View repository](https://github.com/uday2319/Google-Search-Queries-Anomalies-Detection)
</details>

<details>
<summary><b>🌍 Air Quality Analysis</b> · global 2025 AQI trends</summary>
<br/>

Analysis of **2025 air quality data** across global cities, focusing on **PM2.5 and PM10** pollutants.

- Data cleaning and statistical analysis of large datasets
- Time-series analysis to find **pollution spikes** from traffic, industry and wildfires
- Seasonal and regional trend visualizations
- Compared cities against **WHO standards** to flag critical pollution levels

**Stack:** Pandas · NumPy · Matplotlib

🔗 [View repository](https://github.com/uday2319/Air-Quality-Analysis)
</details>

