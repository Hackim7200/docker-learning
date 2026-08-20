# this is the slim version which means the minimum
FROM python:3.8-slim

# work dir is set to /app this is inside container
WORKDIR /app

# copy everthing in the current directrory to the current directory of the container
COPY . .

# updating apt and installing dependencies for mysql
RUN apt-get update && apt-get install -y \
    gcc \
    python3-dev \
    libmariadb-dev \
    pkg-config

# installing flask and mysql
RUN pip install flask mysqlclient

#The port your exposing in container
EXPOSE 5002


CMD ["python", "app.py"]

