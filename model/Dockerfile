FROM python:3.10
LABEL authors="egorgeller"

WORKDIR /usr/src/app/flask-app
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY . .
EXPOSE 3000
ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0
CMD ["flask", "app.py"]
