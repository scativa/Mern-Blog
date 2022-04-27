FROM node:17.4.0-alpine as build
ENV NODE_ENV=development
EXPOSE 3000
WORKDIR /app
# copy only package.json to use cache
COPY package*.json ./
RUN npm install
COPY . .
RUN [ "npm", "run", "build"]

FROM nginx:alpine
COPY --from=build /app/build /usr/share/nginx/html
RUN rm /etc/nginx/conf.d/default.conf
COPY nginx/nginx.conf /etc/nginx/conf.d
CMD ["nginx", "-g", "daemon off;"]