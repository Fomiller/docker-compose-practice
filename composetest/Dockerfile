# build from python image
FROM python:3.7-alpine
# create the directory and cd into ./code
WORKDIR /code

ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0
# run command
RUN apk add --no-cache gcc musl-dev linux-headers
# copy requirements.txt into image at ./code/requirements
COPY requirements.txt requirements.txt
# run command
RUN pip install -r requirements.txt
# expose port 5000
EXPOSE 5000
# copy all files from here down the tree to ./code
COPY . .
# execute commands
CMD ["flask", "run"]