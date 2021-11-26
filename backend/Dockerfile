### network ###
# docker network create goals-net   

### mongodb ###
# docker run --name mongodb -v goals-data:/data/db --rm -d --network goals-net -e MONGO_INITDB_ROOT_USERNAME=john -e MONGO_INITDB_ROOT_PASSWORD=secret mongo

### backend ###
FROM node

WORKDIR /app

COPY package.json .

RUN npm install

COPY . /app

EXPOSE 80

CMD [ "node", "app.js" ]

# docker build -t goals-backend .
# docker run -d --name goals-backend --network goals-net -p 80:80 --rm goals-backend