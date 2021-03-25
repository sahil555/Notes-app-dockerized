FROM node:alpine as frontend

WORKDIR /frontend

COPY ./package.json .
RUN npm install --silent

COPY . .
RUN NODE_ENV=production npm run build

FROM nginx
EXPOSE 3000
COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
COPY --from=frontend /frontend/build /usr/share/nginx/html
