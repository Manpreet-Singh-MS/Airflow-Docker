# Airflow-Docker-compose.yml

Fetching docker-compose.yaml >>  <code>curl -LfO 'https://airflow.apache.org/docs/apache-airflow/2.7.0/docker-compose.yaml'</code>

Initializing Environment >> <code>mkdir -p ./dags ./logs ./plugins ./config</code> >> <code>echo -e "AIRFLOW_UID=$(id -u)" > .env</code> >> <code>AIRFLOW_UID=50000</code>

Initialize the database >> <code>docker compose up airflow-init</code>

Running Airflow >> <code>docker compose up -d</code> (Recommended to Run in Detach-Mode)

Shutting Down & Cleaning up >> <code>docker compose down --volumes --rmi all</code>

P.S. [Sample DAG's](https://github.com/Manpreet-Singh-MS/Airflow-DAGs)







