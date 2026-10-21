# Etapa 1: Construcción de Angular
FROM node:20-alpine AS builder
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build --configuration=production

# Etapa 2: Servidor Web Nginx
FROM nginx:alpine
# Limpiamos el directorio por defecto de Nginx
RUN rm -rf /usr/share/nginx/html/*
# Copiamos los archivos compilados de Angular al servidor Nginx
COPY --from=builder /app/dist/angular/browser /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]