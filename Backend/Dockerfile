FROM node:17.4.0-alpine
ENV NODE_ENV=production

EXPOSE 5000

WORKDIR /app
# copy only package.json to use cache
COPY package*.json ./
RUN npm install --production
COPY . .
CMD [ "node", "server.js" ]

