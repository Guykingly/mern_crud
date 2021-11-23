FROM node:14 as build-stage
WORKDIR /app
# RUN npm install -g nodemon
COPY backend/package*.json /app/
RUN npm install
COPY backend/ /app/
EXPOSE 4000
CMD ["node", "index.js"]
