FROM debian:jessie

RUN apt-get update -q && apt-get install -q -y \
        curl apt-transport-https apt-utils dialog

COPY . /home/download
WORKDIR /home/download
ARG NODEREPO="node_6.x"
ARG DISTRO="jessie"
# Only newest package kept in nodesource repo. Cannot pin to version using apt!
# See https://github.com/nodesource/distributions/issues/33
RUN curl -sSO https://deb.nodesource.com/gpgkey/nodesource.gpg.key
RUN apt-key add nodesource.gpg.key
RUN echo "deb https://deb.nodesource.com/${NODEREPO} ${DISTRO} main" > /etc/apt/sources.list.d/nodesource.list
RUN echo "deb-src https://deb.nodesource.com/${NODEREPO} ${DISTRO} main" >> /etc/apt/sources.list.d/nodesource.list
RUN apt-get update  
RUN apt-get install -y nodejs
RUN npm cache clean
RUN npm install
RUN npm install -g gulp-cli
RUN npm rebuild node-sass
RUN gulp sass
EXPOSE 3000
CMD ["npm","run","start"]
