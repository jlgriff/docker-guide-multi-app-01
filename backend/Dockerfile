### mongodb ###
# docker run --name mongodb --rm -d -p 27017:27017 mongo


### backend ###
FROM node

WORKDIR /app

COPY package.json .

RUN npm install

COPY . /app

EXPOSE 80

CMD [ "node", "app.js" ]

# docker build -t goals-backend .
# docker run -d --name goals-backend -p 80:80 --rm goals-backend