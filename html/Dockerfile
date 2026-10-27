# Imagen base Nginx con Alpine, fijada mediante SHA256
# para garantizar que usamos siempre la misma imagen.
FROM nginxinc/nginx-unprivileged:stable-alpine@sha256:f5116ed4606f3eb015dd4a8e28cb9b351476dc0ad4bc6e9f93b19cec130cdf03

# Copiamos nuestra pagina HTML al servidor web.
COPY index.html /usr/share/nginx/html/index.html

# Ejecutamos la aplicacion con un usuario sin privilegios.
USER 101

# Puerto utilizado por la aplicacion.
EXPOSE 8080

# Iniciamos Nginx en primer plano usando el formato exec.
CMD ["nginx", "-g", "daemon off;"]
