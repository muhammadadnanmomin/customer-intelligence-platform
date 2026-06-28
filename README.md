# Customer Intelligence Platform

## Objective

An end-to-end customer analytics platform for **RFM segmentation**, **churn prediction**, and **customer lifetime value (CLV) forecasting**.

---

## Folder Structure

```
customer-intelligence-platform/
│
├── README.md
├── requirements.txt
├── .gitignore
├── Dockerfile
├── docker-compose.yml
├── setup.py
├── LICENSE
│
├── configs/
│   ├── config.yaml
│   └── logging_config.yaml
│
├── data/
│   ├── raw/
│   ├── interim/
│   ├── processed/
│   └── external/
│
├── notebooks/
│   ├── 01_data_understanding.ipynb
│   ├── 02_eda.ipynb
│   ├── 03_feature_engineering.ipynb
│   ├── 04_rfm_segmentation.ipynb
│   ├── 05_churn_model.ipynb
│   ├── 06_clv_prediction.ipynb
│   └── 07_model_explainability.ipynb
│
├── sql/
│   ├── schema.sql
│   ├── data_loading.sql
│   ├── business_queries.sql
│   └── interview_questions.sql
│
├── src/
│   ├── ingestion/
│   ├── preprocessing/
│   ├── features/
│   ├── segmentation/
│   ├── churn/
│   ├── clv/
│   ├── analytics/
│   ├── visualization/
│   ├── utils/
│   └── pipelines/
│
├── models/
│   ├── churn/
│   ├── clv/
│   └── segmentation/
│
├── reports/
│   ├── figures/
│   ├── metrics/
│   └── business_reports/
│
├── powerbi/
│   ├── dax_measures/
│   └── dashboards/
│
├── streamlit_app/
│   ├── Home.py
│   ├── pages/
│   ├── components/
│   └── assets/
│
├── tests/
│   ├── test_preprocessing.py
│   ├── test_features.py
│   └── test_models.py
│
├── logs/
│
└── docs/
    ├── architecture/
    ├── data_dictionary/
    └── api_docs/
```

---

## Setup Instructions

### Prerequisites

- Python 3.10+
- Git
- Docker & Docker Compose (optional)
- PostgreSQL (optional)

### 1. Clone the Repository

```bash
git clone https://github.com/<your-username>/customer-intelligence-platform.git
cd customer-intelligence-platform
```

### 2. Create & Activate Virtual Environment

```bash
python -m venv .venv

# Windows
.venv\Scripts\activate

# macOS / Linux
source .venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Configure Environment

```bash
cp .env.example .env
# Edit .env with your credentials
```

### 5. Run Tests

```bash
pytest tests/ -v
```

### 6. Docker Deployment

```bash
docker-compose up --build
```

---

## License

MIT License — see [LICENSE](LICENSE) for details.
