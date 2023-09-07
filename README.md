# Airflow-Docker-compose.yml

Fetching docker-compose.yaml >> curl -LfO 'https://airflow.apache.org/docs/apache-airflow/2.7.0/docker-compose.yaml'

Initializing Environment >> mkdir -p ./dags ./logs ./plugins ./config >> echo -e "AIRFLOW_UID=$(id -u)" > .env >> AIRFLOW_UID=50000

Initialize the database >> docker compose up airflow-init

Running Airflow >> docker compose up -d (Recommended to Run in Detach-Mode)

Shutting Down & Cleaning up >> docker compose down --volumes --rmi all







