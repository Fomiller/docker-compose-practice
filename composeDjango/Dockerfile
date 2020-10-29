FROM python:3
# create enviornment variable
ENV PYTHONUNBUFFERED=1
# create ./code
RUN mkdir /code
# cd into ./code
WORKDIR /code
# copy/pase requirements.txt to ./code/requirements.txt
COPY requirements.txt /code/
# run install command
RUN pip install -r requirements.txt
# copy all code to ./code
COPY . /code/