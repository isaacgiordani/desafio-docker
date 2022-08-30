FROM python:3.8.12-slim-buster
WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY . /app
CMD ["gunicorn", "--bind", "0.0.0.0:5000", "-c", "config.py", "app:app"]

# cd rotten-potatoes/src/
# docker build -t isaacgiordani/rotten-potatoes:v1 .
# docker login
# docker push isaacgiordani/rotten-potatoes:v1
# docker tag isaacgiordani/rotten-potatoes:v1 isaacgiordani/rotten-potatoes:latest
# docker image ls
# docker push isaacgiordani/rotten-potatoes:latest
# docker-compose up -d
# http://localhost:5000/