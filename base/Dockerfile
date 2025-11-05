# 1. Imagen base: Usamos la imagen oficial de Nginx.
#    Esta es una imagen pequeña y optimizada para servir archivos estáticos.
FROM nginx:alpine

# 2. Copia de los archivos del frontend:
#    El directorio por defecto donde Nginx sirve archivos es /usr/share/nginx/html.
#    Asume que los archivos de tu frontend (HTML, CSS, JS, etc.)
#    están en una carpeta llamada 'dist' (típico de builds de React, Angular, Vue).
#    ¡Asegúrate de cambiar 'dist' por el nombre de tu carpeta de build si es diferente!


# 3. Exponer el puerto:
#    El puerto por defecto que usa Nginx es el 80.
EXPOSE 80

# 4. Comando de inicio (opcional pero recomendado):
#    El comando por defecto en la imagen de Nginx ya inicia el servidor,
#    pero esta línea asegura que se use el comando principal en primer plano.
# CMD ["nginx", "-g", "daemon off;"]