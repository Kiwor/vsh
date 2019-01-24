# Wordpress human-firendly-urls
# laadisin alla Wordpressi pakki
wget http://wordpress.org/latest.zip

# Unzippisin arhiivi
unzip latest.zip

# Seadsin omaniku
chown -R www-data:www0data /var/www/html/wordpress

# Seadsin ules oigused
chmod -R 755 /var/www/html/wordpress

# Lõin kausta wordpress/wp-content/... alla
mkdir -p /var/www/html/wordpress/wp-content/uploads

# Ning seadis sellele vastava omaniku
chown -R www-data:wwwdata /var/www/html/wordpress/wp-content/uploads

# MySQL-is
CREATE DATABASE wordpress;

CREATE USER wp_user@localhost IDENTIFIED BY 'qwerty';

GRANT ALL PRIVILEGES ON wordpress.* TO wp_user@localhost;

FLUSH PRIVILEGES;

exit
