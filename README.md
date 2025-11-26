# spotify_de_project_


# 🎧 Spotify Data Engineering Pipeline

Projet complet de Data Engineering construit pour un **portfolio professionnel**.  
Il combine GCP, Airflow, Snowflake, Python, Docker, FastAPI, Grafana et Power BI pour créer une plateforme analytique end-to-end.

---

## 🏗️ Architecture du Projet


---

## 🚀 Technologies Utilisées

### Infrastructure & Orchestration
- Docker & Docker Compose  
- Apache Airflow  
- Google Cloud Storage (GCS)

### Data Warehouse
- Snowflake  

### Data Engineering
- Python  
- Snowflake Connector  
- FastAPI  
- Airflow Operators  

### Business Intelligence
- Grafana (JSON API Datasource)  
- Power BI  

---

## 📦 Structure du Projet


spotify_de_project/
├── dags/
│ └── spotify_dag.py
├── etl/
│ └── spotify_etl.py
├── api/
│ ├── main.py
│ └── requirements.txt
├── config/
│ ├── airflow.env
│ └── snowflake.env
├── gcp/
│ └── airflow-service-key.json
├── docker-compose.yml
└── Dockerfile

yaml
Copier le code

---

## 🔧 Installation et Lancement

### 1️⃣ Cloner le projet
```bash
git clone <URL_DU_REPO>
cd spotify_de_project
2️⃣ Configurer Snowflake
Dans config/snowflake.env :

ini
Copier le code
SNOWFLAKE_USER=xxx
SNOWFLAKE_PASSWORD=xxx
SNOWFLAKE_ACCOUNT=xxx
SNOWFLAKE_WAREHOUSE=COMPUTE_WH
SNOWFLAKE_DATABASE=SPOTIFY_DB
SNOWFLAKE_SCHEMA=ANALYTICS
3️⃣ Lancer toute la stack
bash
Copier le code
docker-compose up --build
🌬️ Pipeline Airflow
Le DAG spotify_etl_pipeline :

Extrait les fichiers JSON depuis GCS

Transforme les données (Python)

Charge les tables Snowflake

## Lancer le pipeline :

nginx
Copier le code
Airflow UI → http://localhost:8080
⚡ API FastAPI
Utilisée par Grafana pour consulter Snowflake.

Endpoints :
/tracks_count

/top_artists

/top_albums

/tracks_by_playlist/{id}

Test :

bash
Copier le code
http://localhost:9000/top_artists
📊 Dashboard Grafana
Disponible sur :

arduino
Copier le code
http://localhost:3000
Panels recommandés :

KPI total des tracks

Top artistes

Top albums

Répartition par playlist

📈 Dashboard Power BI
Power BI peut se connecter :

directement à Snowflake

ou via API FastAPI

ou via fichiers exportés

🎓 Compétences Développées
Architecture Data End-to-End

Orchestration Airflow

ETL Python

Snowflake (modélisation + SQL)

API FastAPI

Docker

GCP

Grafana (JSON API)

Monitoring ETL

🔮 Améliorations Futures
Ajouter Spark pour gros volumes

Ajouter dbt pour les transformations SQL

Ajouter CI/CD GitLab

Ajouter monitoring Prometheus

Dashboard Streamlit

👩‍💻 Auteure
Sabrina (SBN)
Data Engineer Junior
Projet portfolio – 2025
