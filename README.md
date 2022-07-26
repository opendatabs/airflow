Follow the steps outlined [here](https://airflow.apache.org/docs/apache-airflow/stable/start/docker.html#docker-compose-yaml):
~~~ 
[Mac V. 2.3.4] brew install docker-compose
curl -LfO 'https://airflow.apache.org/docs/apache-airflow/2.2.4/docker-compose.yaml'
echo "AIRFLOW_UID=50000" > .env
docker-compose up airflow-init
docker-compose up

~~~
- Open [http://localhost:8080](http://localhost:8080)
- Success.
- To stop AirFlow: 
~~~
docker-compose down
~~~
- To tear down and delete everything:
~~~
docker-compose down --volumes --rmi all
rm -rf dags
rm -rf logs
rm -rf plugins
~~~