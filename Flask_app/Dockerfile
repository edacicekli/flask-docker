# start from base

FROM python:3.8.10


# We copy just the requirements.txt first to leverage Docker cache

RUN apt-get update -y
RUN apt-get install python3-pip -y

COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt


WORKDIR /app
COPY . .

CMD [ "python3", "./app.py" ]
