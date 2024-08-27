# Step 1: Start with the latest Ubuntu image
FROM ubuntu:latest

# Step 2: Update APT package list
RUN apt-get update

# Step 3: Upgrade installed packages
RUN apt-get upgrade -y

RUN apt-get install -y python3 python3-pip    
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED
RUN pip3 install flask

RUN mkdir -p /app

WORKDIR /app

COPY ./api.py /app/api.py 

CMD python3 api.py
