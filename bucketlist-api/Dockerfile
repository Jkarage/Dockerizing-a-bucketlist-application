# build image on top of python 3.6
FROM python:3.6

# install environment dependencies
RUN apt-get update -yqq \
  && apt-get install -yqq --no-install-recommends apt-utils\
    netcat \
  && apt-get -q clean

# Creating a folder named /app
RUN mkdir /app

# copying all contents of the current folder where the Dockerfile resides to the folder /app
COPY . /app


# this is changing the current working directory to /app
# since it has the requirement.txt file which contains the API dependencies
WORKDIR /app

# installing API dependencies
RUN pip install -r requirements.txt


RUN nosetests --with-coverage --cover-package=bucketlist

# making the script executable
RUN chmod +x start_postgres.sh

# exposing the application default port
EXPOSE 5000

# this will execute this bash script named start_postgres.sh when a container is
# created from this image
CMD ["./start_postgres.sh"]


