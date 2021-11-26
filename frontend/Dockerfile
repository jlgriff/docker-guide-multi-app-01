FROM node

WORKDIR /app

COPY package.json .

RUN npm install

COPY . /app

EXPOSE 3000

CMD [ "npm", "start" ]

# docker build -t goals-frontend .
# docker run -d --name goals-frontend --rm -p 3000:3000 --network goals-net -it goals-frontend