
FROM debian:latest

RUN apt-get update && \
    apt-get install -y apache2 curl && \
    curl -sL https://deb.nodesource.com/setup_20.x | bash - && \
    apt-get install -y nodejs && \
    npm install -g @angular/cli


WORKDIR /usr/src/app/DatosB

COPY DatosB/package*.json ./

RUN npm install && npm cache clean --force

COPY DatosB/ .

RUN npx -p @angular/cli@latest ng build --output-path /usr/src/app/DatosB/dist/datos-b

RUN cp -r /usr/src/app/DatosB/dist/datos-b/browser/* /var/www/html

EXPOSE 80 


RUN echo "ServerName localhost" >> /etc/apache2/apache2.conf

CMD ["apachectl", "-D", "FOREGROUND"]
