FROM node
WORKDIR /app

COPY package.json .

RUN npm i
COPY . .


## EXPOSE [Port you mentioned in the vite.config file]
EXPOSE 80
CMD ["npm", "run", "dev"]