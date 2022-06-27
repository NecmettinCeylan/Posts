# How to Add PostgreSQL as Backend to Airflow
## Guide to use postgres as backend for airflow and some useful commands

# 1. Create an admin user

Activate your virtual environment that airflow installed and then run:

    airflow users create \
        --username admin \
        --firstname name \
        --lastname surname \
        --role Admin \
        --email gigidy@gigidy.com


# 2. Set postgres connection string

First replace variables in the following code with your settings:

    postgresql+psycopg2://<user>:<password>@<host>/<db>

Then change following code in airflow.cfg in your $AIRFLOW_HOME folder 

    [database]
    sql_alchemy_conn = my_conn_string


# 3. Change to local executer as :

Set executer to LocalExecutor in airflow.cfg in your $AIRFLOW_HOME folder

    [core]
    executor = LocalExecutor


# 4. Restart airflow after changing settings:

You can use following script to kill airflow process:

    kill $(ps -ef | grep "airflow standalone" | awk '{print $2}')

and then start airflow using:

    airflow standalone

or start airflow in background:

    airflow standalone </dev/null &>/dev/null &


# Ref:

[https://airflow.apache.org/docs/apache-airflow/stable/howto/set-config.html](https://airflow.apache.org/docs/apache-airflow/stable/howto/set-config.html)

[https://airflow.apache.org/docs/apache-airflow/stable/howto/set-up-database.html#database-uri](https://airflow.apache.org/docs/apache-airflow/stable/howto/set-up-database.html#database-uri)