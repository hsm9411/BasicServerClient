FROM python:3.10-slim

WORKDIR /app

COPY requirements.txt .
COPY run_client.py .

RUN pip install -r requirements.txt

CMD ["python", "-u","run_client.py"]
