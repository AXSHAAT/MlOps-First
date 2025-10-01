

# 🚗 Vehicle Data MLOps Project

A **production-grade MLOps project** demonstrating the full lifecycle of a machine learning system — from **data ingestion** to **model training, deployment, and CI/CD automation** using **AWS, Docker, MongoDB, and GitHub Actions**.

This project showcases my ability to design, implement, and deploy ML pipelines using **modern DevOps/MLOps best practices**.

---

## 📌 Features

* ✅ **Automated Project Structure** with `template.py`
* ✅ **Local Package Management** via `setup.py` & `pyproject.toml`
* ✅ **Environment & Dependencies** managed using Conda + `requirements.txt`
* ✅ **MongoDB Atlas Integration** for dataset storage & retrieval
* ✅ **Custom Logging & Exception Handling**
* ✅ **End-to-End ML Pipeline**

  * Data Ingestion
  * Data Validation
  * Data Transformation
  * Model Training
  * Model Evaluation
  * Model Pushing to AWS S3
* ✅ **AWS Integration**

  * S3 for model storage
  * IAM for secure authentication
* ✅ **Prediction API with Flask (`app.py`)**
* ✅ **CI/CD with GitHub Actions**
* ✅ **Containerization & Deployment**

  * Dockerized application
  * AWS ECR for image registry
  * AWS EC2 for deployment
* ✅ **Scalable Inference Service** exposed via public endpoint

---

## ⚙️ Project Setup

### 🔹 Step 1: Project Initialization

```bash
python template.py
```

### 🔹 Step 2: Setup Local Packages

* `setup.py` and `pyproject.toml` configured for local imports.

### 🔹 Step 3: Virtual Environment & Dependencies

```bash
conda create -n vehicle python=3.10 -y
conda activate vehicle
pip install -r requirements.txt
pip list
```

---

## 🗄️ MongoDB Setup

1. Create a **MongoDB Atlas project & cluster (M0 tier)**
2. Configure **username/password & network access (0.0.0.0/0)**
3. Obtain **connection string** for Python driver
4. Push dataset to MongoDB via Jupyter Notebook (`mongoDB_demo.ipynb`)
5. Validate data using MongoDB Atlas collections

---

## 📊 ML Pipeline Workflow

### 🔹 Data Handling

* **Data Ingestion**: Fetch & transform data from MongoDB → DataFrame
* **Data Validation**: Schema-driven validation (`config/schema.yaml`)
* **Data Transformation**: Feature engineering + preprocessing

### 🔹 Model Lifecycle

* **Model Trainer**: Train ML model with pipeline architecture
* **Model Evaluation**: Compare new model vs. existing model with thresholding
* **Model Pusher**: Push best model → AWS S3 bucket (`my-model-mlopsproj`)

---

## ☁️ AWS Integration

* **IAM Users & Roles** for secure access
* **S3 Buckets** for model registry
* **Environment Variables** for credentials

---

## 🐳 CI/CD & Deployment

### 🔹 Dockerization

* `Dockerfile` & `.dockerignore` for container builds

### 🔹 GitHub Actions

* Workflow YAML for CI/CD
* AWS credentials stored as GitHub Secrets
* Push → Build → Deploy automatically

### 🔹 AWS EC2 Deployment

* **Ubuntu Server (24.04)**
* Self-hosted GitHub Runner
* Exposed app on **port 5080**

---

## 🚀 Usage

### Run Locally

```bash
python app.py
```

Access app at: `http://localhost:5080`

### Train Model

```bash
http://<public-ip>:5080/training
```

---

## 🛠️ Tech Stack

* **Languages**: Python, YAML, Bash
* **ML**: Scikit-learn, Pandas, Numpy
* **DB**: MongoDB Atlas
* **Cloud**: AWS (S3, EC2, IAM, ECR)
* **MLOps Tools**: Docker, GitHub Actions, CI/CD Pipelines
* **Visualization**: Jupyter Notebook (EDA & Feature Engineering)

---

## 📌 Project Architecture

```bash
├── src/
│   ├── components/        # Data ingestion, validation, transformation, trainer
│   ├── configuration/     # MongoDB & AWS connections
│   ├── entity/            # Config, Artifact, Estimator classes
│   ├── pipeline/          # Training & Prediction pipelines
│   ├── utils/             # Utilities (logging, exception handling, helpers)
│
├── notebook/              # Jupyter notebooks (EDA, MongoDB demo)
├── requirements.txt
├── setup.py
├── pyproject.toml
├── app.py                 # Flask app entry point
├── Dockerfile
├── .dockerignore
├── .github/workflows/     # GitHub Actions CI/CD configs
```

---

## 🌟 Highlights for Recruiters

* Implemented **full-stack MLOps pipeline** from scratch.
* Used **MongoDB Atlas + AWS S3** for hybrid data & model storage.
* Automated deployment via **GitHub Actions → Docker → AWS EC2**.
* Designed **modular & scalable architecture** for production ML systems.

---

🔥 This project demonstrates not just ML model building but **end-to-end production deployment and automation** — the core of modern **MLOps practices**.

---

