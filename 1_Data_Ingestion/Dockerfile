FROM python:3.9
RUN pip config set global.trusted-host \
    "pypi.org files.pythonhosted.org pypi.python.org" \
    --trusted-host=pypi.python.org \
    --trusted-host=pypi.org \
    --trusted-host=files.pythonhosted.org
RUN pip install pandas  sqlalchemy psycopg2
RUN apt-get install wget

WORKDIR /app
COPY ingest_data.py ingest_data.py

#ENTRYPOINT ["bash"]
ENTRYPOINT ["python","ingest_data.py"]