FROM ubuntu:20.04
LABEL maintainer="Ben Smith <Benjamin.Smith.23@labmda.compute.cmc.edu>"

RUN apt-get update -y && \
    apt-get install -y python3 python3-pip python3-dev

COPY ./requirements.txt /app/requirements.txt

WORKDIR /app

RUN pip3 install --upgrade pip
RUN pip3 install -r requirements.txt

COPY . /app

ENTRYPOINT ["python3"]
CMD ["app.py"]

