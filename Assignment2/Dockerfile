FROM ubuntu:20.04
RUN apt-get update -y \
    && apt-get install -y python3-pip mysql-client
COPY . /app
WORKDIR /app
RUN pip install --upgrade pip \
    && pip3 install flask \
    && pip install -r requirements.txt
EXPOSE 8080
ENTRYPOINT ["python3"]
CMD ["app.py"]
