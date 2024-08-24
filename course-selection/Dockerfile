FROM node:20-alpine as build
WORKDIR /app
COPY package.json 
package-lock.json ./
Run npm install
COPY . .
RUN npm run build
FROM nginx:1.23-alpine
COPY --from=build /app/build /usr/share/nginx/html
EXPOSE 8080
CMD ["nginx", "-g", "daemon off;"]
