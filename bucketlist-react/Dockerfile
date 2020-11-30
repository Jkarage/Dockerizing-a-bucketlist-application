FROM node:12.20

RUN npm install -g gulp-cli serve
COPY . /app
WORKDIR /app
RUN npm rebuild node-sass
RUN npm install --loglevel=error
RUN gulp sass 
CMD ["npm","start"]
