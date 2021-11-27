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

ENV MONGODB_USERNAME=root
ENV MONGODB_PASSWORD=password

CMD [ "npm", "start" ]

# docker build -t goals-backend .
# docker run -d --name goals-backend -p 80:80 --network goals-net -v "C:\Users\banza\git\docker-guide-multi-app-01\backend:/app" -v /app/node_modules -v goals-logs:/app/logs -e MONGODB_USERNAME=john -e MONGODB_PASSWORD=secret --rm goals-backend