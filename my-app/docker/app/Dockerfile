FROM node:14
WORKDIR /app
COPY my-app/package*.json /app/
RUN npm install
COPY my-app/ /app/
EXPOSE 3000
CMD [ "npm", "start" ]


# # Stage 0, "build-stage", based on Node.js, to build and compile the frontend
# FROM node:14 as build-stage
# WORKDIR /app
# COPY my-app/package*.json /app/
# RUN npm install
# COPY my-app/ /app/
# RUN npm run build
# # Stage 1, based on Nginx, to have only the compiled app, ready for production with Nginx
# FROM nginx:1.21.0
# COPY --from=build-stage /app/build/ /usr/share/nginx/html
# # Copy the default nginx.conf provided by tiangolo/node-frontend
# # COPY client/nginx/default.conf /etc/nginx/conf.d/default.conf
