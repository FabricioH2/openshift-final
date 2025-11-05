# Usa la imagen base
FROM fabricioph2/frontend-base:1.0 

COPY public/ /usr/share/nginx/html/

# 3. Exponer el Puerto
# Nginx corre por defecto en el puerto 80 dentro del contenedor.
EXPOSE 80

# Opcional: Si necesitas alguna configuración específica de Nginx,
# puedes copiar un archivo de configuración personalizado aquí.
# COPY nginx.conf /etc/nginx/nginx.conf