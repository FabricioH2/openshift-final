# Imagen base común para todos los frontends
FROM node:20-alpine AS base

# Variables comunes
ENV NODE_ENV=production
WORKDIR /app

# Instala dependencias comunes del sistema (si las hay)
RUN apk add --no-cache curl bash

# Copia el package.json si quieres tener dependencias básicas comunes
# COPY package*.json ./
# RUN npm ci --omit=dev

# Esta imagen no contiene el código aún
# Se usará como base para otras imágenes (multi-stage)
