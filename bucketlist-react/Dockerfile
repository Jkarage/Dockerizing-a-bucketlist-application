# build image on top of node
FROM node

# install environment dependencies
RUN apt-get update -yqq \
  && apt-get install -yqq --no-install-recommends apt-utils\
    netcat \
  && apt-get -q clean

RUN apt-get install npm

RUN  npm install -g gulp-cli

RUN npm install

RUN gulp sass

RUN npm start


