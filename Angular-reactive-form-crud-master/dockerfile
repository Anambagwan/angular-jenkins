FROM node:latest as angular

WORKDIR /app
COPY . . 
RUN npm install

RUN npm run build --prod

FROM nginx:alpine

COPY --from=angular /app/dist/data-profile /usr/share/nginx/html

