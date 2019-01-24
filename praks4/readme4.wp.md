# Lõin võtme
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/ssl/private/apache-selfsigned.key -out /etc/ssl/certs/apache-selfsigned.crt

# Kopeerisin fiali sisu
nano /etc/apache2/conf-available/ssl-params.conf

# Tegin failist varukoopia
cp /etc/apache2/sites-available/default-ssl.conf /etc/apache2/sites-available/default-ssl.conf.bak

# default-ssl.conf-is ServerName'i oma ip'ks, mis on 172.23.13.37

# 000-default.conf failis lisasin ümbersuunamiseks "/" "https://172.23.13.37/"
