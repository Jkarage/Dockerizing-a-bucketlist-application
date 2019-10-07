# build image on top of node
#FROM node:9

#RUN npm install

#EXPOSE 3000

#CMD ["npm", "run", "start"]

FROM node:9

WORKDIR /app

COPY package.json /app

RUN npm install

# RUN npm install gulp -D

RUN npm install --global gulp-cli
# RUN npm install gulp-cli

COPY . /app

RUN gulp sass


CMD ["npm", "run", "start"]

EXPOSE 8081
