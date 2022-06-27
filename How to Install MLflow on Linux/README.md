# How to Install MLflow on Linux
## Simple steps to start mlflow server

# 1. Create a virtual environment and then install MLflow using pip 

    pip install mlflow

# 2. Start server with the back end uri

    mlflow server --backend-store-uri sqlite:///mydb.sqlite


# Extra

You can start using a postgres backend and local artifact store

    mlflow server \
        --backend-store-uri postgresql+psycopg2://<username>:<password>@<host>:<port>/<database>\
        --default-artifact-root /home/user/mlflow_artifacts \
        --host 0.0.0.0 \
        --port 5000 

or you can start using a postgres backend and s3 artifact store


    mlflow server \
        --host 0.0.0.0 \
        --port 5000 \
        --serve-artifacts \
        --artifacts-destination s3://my-mlflow-bucket/ \


# ref:

[https://www.mlflow.org/docs/latest/quickstart.html](https://www.mlflow.org/docs/latest/quickstart.html)

[https://www.mlflow.org/docs/latest/tracking.html#scenario-3-mlflow-on-localhost-with-tracking-server](https://www.mlflow.org/docs/latest/tracking.html#scenario-3-mlflow-on-localhost-with-tracking-server)