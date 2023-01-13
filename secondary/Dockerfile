FROM node
WORKDIR /app

COPY package.json .

RUN npm i
COPY . .
RUN npm run build
# 

# Run preview with vite config
CMD ["npm", "run", "preview"]