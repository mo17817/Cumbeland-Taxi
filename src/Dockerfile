#Develop Stage
FROM node:13.14-alpine as develop-stage 
WORKDIR /Users/abdeahmed/dev/git/demo/Cumbeland-Taxi
COPY package*.json ./
RUN yarn global add @quasar/cli
COPY . .

#Building Stage 
FROM develop-stage as build-stage
RUN yarn
RUN quasar build

#First stage installs all dependencies in Node container
#Second Stage BUILDS application in the created Node Container 
#Third Stage serves the artifacts with NginX

#Prouction Stage 
FROM nginx:1.17.5-alpine as production-stage
COPY --from=build-stage /Users/abdeahmed/dev/git/demo/Cumbeland-Taxi/dist/spa /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
