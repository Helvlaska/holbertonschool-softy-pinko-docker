# Utilisation de la dernière version de nginx
FROM nginx:1.28.0

# Copier les fichiers/dossiers de l'hôte vers l'image
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

# Expose le port utilisé par Nginx
EXPOSE 9000

# Lancer Nginx en mode premier plan
CMD ["nginx", "-g", "daemon off;"]
