FROM python:2.7
LABEL maintainer="Sohbet Dovranov"

WORKDIR /app
COPY . /app

# install the packages from requirements.txt and create database.db with the pre-defined posts
RUN pip install --no-cache-dir -r requirements.txt && python init_db.py

# the application listens on port 3111
EXPOSE 3111

# start TechTrends when the container starts
CMD [ "python", "app.py" ]
