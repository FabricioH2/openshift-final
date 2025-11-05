# Usa la imagen base
FROM fabricioph2/frontend-base:1.0 AS build

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

# Crea un usuario y grupo sin privilegios
RUN addgroup -S appgroup && adduser -S appuser -G appgroup

# Cambia la propiedad de los archivos a ese usuario
RUN chown -R appuser:appgroup /usr/share/nginx/html

# Cambia al usuario no root
USER appuser

EXPOSE 80
