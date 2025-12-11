# Utilise l'image Ubuntu officielle
FROM ubuntu:22.04

# Empêche les prompts interactifs pendant l'installation
ENV DEBIAN_FRONTEND=noninteractive

# Mise à jour + installation de nginx + nettoyage
RUN apt-get update && \
    apt-get install -y nginx && \
    rm -rf /var/lib/apt/lists/*

# Suppression de la config par défaut
RUN rm /etc/nginx/sites-enabled/default

# Copie de notre configuration de reverse proxy
COPY reverse-proxy.conf /etc/nginx/conf.d/reverse-proxy.conf

# Nginx tourne en foreground (important pour Docker)
CMD ["nginx", "-g", "daemon off;"]

# Expose le port HTTP
EXPOSE 80
