# Usa la imagen base
FROM fabricioph2/frontend-base:1.0

WORKDIR /app

# Copia y prepara dependencias
COPY package*.json ./
RUN npm ci

# Copia código y compila
COPY . .
RUN npm run build

# Etapa 2: runtime con NGINX
FROM nginx:1.25-alpine
COPY --from=build /app/dist /usr/share/nginx/html

EXPOSE 80
