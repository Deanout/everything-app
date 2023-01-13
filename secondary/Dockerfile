FROM node
WORKDIR /app

COPY package.json .

RUN npm i
COPY . .
RUN npm run build
# 

## EXPOSE [Port you mentioned in the vite.config file]
EXPOSE 4173
# Run preview with vite config
CMD ["npm", "run", "preview"]