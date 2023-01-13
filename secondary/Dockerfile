FROM node
WORKDIR /app

COPY package.json .

RUN npm i
COPY . .
RUN npm run build
COPY . .

## EXPOSE [Port you mentioned in the vite.config file]
EXPOSE 8080:8080
# Run preview with vite config
CMD ["npm", "run", "preview"]