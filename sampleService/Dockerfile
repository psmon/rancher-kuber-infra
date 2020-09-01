FROM node:6.9.2
RUN mkdir /app
WORKDIR /app
COPY ./node/app.js .
COPY ./node/package.json .
#RUN npm install --save​
EXPOSE 8080
CMD [ "node", "app.js" ]
