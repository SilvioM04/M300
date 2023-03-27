# Basisimage auswählen
FROM ubuntu:latest

# Arbeitsverzeichnis erstellen
WORKDIR /app

# Apache Webserver, curl und SSL-Tools installieren
RUN apt-get update && \
    apt-get install -y apache2 curl openssl && \
    rm -rf /var/lib/apt/lists/*

# SSL-Zertifikat erstellen
RUN openssl req -x509 -nodes -days 365 -newkey rsa:2048 \
    -keyout /etc/ssl/private/apache-selfsigned.key \
    -out /etc/ssl/certs/apache-selfsigned.crt \
    -subj "/C=US/ST=State/L=City/O=Organization/CN=localhost"

# Apache-Konfiguration aktualisieren
COPY ./apache-ssl.conf ./default-ssl.conf
RUN a2enmod ssl && \
    a2ensite default-ssl && \
    sed -i 's/AllowOverride None/AllowOverride All/' /etc/apache2/apache2.conf

# Index.html File hinzufügen
COPY ./index.html /var/www/html/

# Exponiere Port 443 für HTTPS-Verbindungen
EXPOSE 443

# Startbefehl definieren
CMD ["apachectl", "-D", "FOREGROUND"]
