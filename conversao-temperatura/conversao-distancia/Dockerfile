FROM python:3.8.12-slim-buster
EXPOSE 5000
COPY requirements.txt .
RUN python -m pip install -r requirements.txt
WORKDIR /app
COPY . /app
CMD ["gunicorn", "--bind", "0.0.0.0:5000", "-c", "app.py", "app:app"]

# docker build -t isaacgiordani/conversao-distancia:v1 .
# docker login
# docker push isaacgiordani/conversao-distancia:v1
# docker tag isaacgiordani/conversao-distancia:v1 isaacgiordani/conversao-distancia:latest
# docker image ls
# docker push isaacgiordani/conversao-distancia:latest
# docker container run -d -u 1000 -p 5000:5000 --cpus="0.5" isaacgiordani/conversao-distancia:v1