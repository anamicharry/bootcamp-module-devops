FROM python:3.7-alpine

EXPOSE 8000/tcp

WORKDIR /opt/app
# Backend directory / Workdir
COPY . .

RUN pip install -r requirements.txt

ENTRYPOINT ["gunicorn", "-w", "3", "-b", "0.0.0.0:8000", "app:app"]